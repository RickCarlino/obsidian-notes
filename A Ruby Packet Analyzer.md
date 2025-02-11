# Basic Version
```ruby
require 'socket'

socket = Socket.new(Socket::AF_INET, Socket::SOCK_RAW, Socket::IPPROTO_TCP)

socket.bind(Socket.sockaddr_in(0, '0.0.0.0'))

loop do
  packet, addr = socket.recvfrom(65535) # Capture raw TCP packets
  puts("\nReceived Packet from #{addr.inspect}:")
  puts(packet.slice(0, 10).unpack('B*')) # Convert packet data to hex format for analysis
end
```
# Useful Version
```ruby
require 'socket'

# Create a raw socket to capture TCP packets
sock = Socket.new(Socket::AF_INET, Socket::SOCK_RAW, Socket::IPPROTO_TCP)

# Receive packets indefinitely
loop do
  packet, sender = sock.recvfrom(65536)
  ip_header = packet[0, 20]  # First 20 bytes are the IP header
  tcp_header = packet[20, 20] # Next 20 bytes are the TCP header

  # Parse IP header
  version_ihl, tos, total_length, id, frag_off, ttl, protocol, checksum, src_ip, dest_ip =
    ip_header.unpack("C C n n n C C n N N")

  ip_version = version_ihl >> 4
  ip_header_length = (version_ihl & 15) * 4

  # Convert source and destination IP to readable format
  src_ip = [src_ip].pack("N").unpack("CCCC").join(".")
  dest_ip = [dest_ip].pack("N").unpack("CCCC").join(".")

  # Parse TCP header
  src_port, dest_port, seq_num, ack_num, offset_reserved_flags, window, checksum, urg_pointer =
    tcp_header.unpack("n n N N n n n n")

  offset = (offset_reserved_flags >> 12) * 4
  flags = offset_reserved_flags & 0x3F # Extract TCP flags

  fin = flags & 0x01
  syn = (flags & 0x02) >> 1
  rst = (flags & 0x04) >> 2
  psh = (flags & 0x08) >> 3
  ack = (flags & 0x10) >> 4
  urg = (flags & 0x20) >> 5

  # Print captured packet details
  puts "\n[+] Captured TCP Packet Length: #{total_length}"
  puts "Source IP: #{src_ip} | Destination IP: #{dest_ip}"
  puts "Source Port: #{src_port} | Destination Port: #{dest_port}"
  puts "Sequence Number: #{seq_num} | Acknowledgment Number: #{ack_num}"
  puts "Flags: SYN=#{syn}, ACK=#{ack}, FIN=#{fin}, RST=#{rst}, PSH=#{psh}, URG=#{urg}"
end

```