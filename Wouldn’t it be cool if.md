This note serves as a final resting place for ideas I've had but realisticly won't have time to build.

# A Better E-Reader

There are too many e-readers to name. I've used Instapaper and Pocket extensively over the last 15 years.

Problems I see with current readers:
 - Overly focused on long-form content (Omnivore, Eleven reader)
 - Not good at reading short form content while driving or performing other hands-free tasks. A good reader will work exactly like a music player, but for test-to-speech articles (auto play, back/next/pause controls, etc..). Instapaper and Pocket fail here.

# A Retrospective Tool

Tools like Metroretro and whatever god-awful thing Atlassian built already exist. I think there is room for competition (and apetite for alternatives) in this space.

# An IRC-Based Customer Support Widget
IRC is *very* dead and won't be coming back to life soon, even if [IRC v3](https://ircv3.net/) addresses many of the concerns that led to its demise. One thing that IRC does better than many of its modern equivalents (such as XMPP, Matrix, Slack, Discord) is extensibility. It's way easier to write IRC integrations.

The idea: Use IRC-over-websockets (supported by many modern servers) as a drop-in replacement to customer support widgets.

Similar project: https://cactus.chat/ (Web comments over Matrix)

# Human-in-the-loop Prompt Eval Tool

While building [Koala Cards](https://koala.cards/) there have been several times where I perform human-intensive prompt evals and double-blind testing of tasks that do not have a definitively correct answer (think: essay grading and speaking exercise feedback).

What I would love to see: an app that lets authors input a spreadsheet of test data, plus the ability to build prompts using handlebars templates to apply said data against a prompt. The user can then perform blind thumbs up / thumbs down evaluation against the output of several candidate prompts to select the best performing prompt.

# A Spaced Repetition App for Children's Reading Needs

Learning phonics is mostly memorization and repetition over a wide range of reading material. Related article: https://www.lesswrong.com/posts/2PLBhCbByRMaEKimo/spaced-repetition-for-teaching-two-year-olds-how-to-read

# Form Builder

I've needed a GUI form builder for a number of things in the past and have had issues with all of them. There is room for alternatives in this space. TODO: Evaluate tools like n8n for similar automation needs.

# Dumb Incubator Conversion Kit

I raise poultry as a hobby. As a nerd with a history in hardware automation, I could see a kit that enabled the user to convert a "dumb" incubator into a smart incubator.

Components:

 - Control unit: WiFi enabled control box with solid state relays.
	 - Humidifier plug
	 - Heating element plug
	 - Egg turner plug
	 - Sensor egg: a bluetooth low energy module that communicates back to the control box from within the incubator. Monitors things like:
		 - Last successful egg turn
		 - humidity level
		 - temperature
		 - O2/CO2 levels