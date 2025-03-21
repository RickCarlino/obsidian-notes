
```typescript
  openai
    .chat
    .completions
    .create({
      model: "gpt-4o-audio-preview",
      messages: [
        {
          role: "user",
          content: [
            {
              type: "input_audio",
              input_audio: {
                data: base64Data,
                format: "wav",
              },
            },
          ],
        },
      ],
    })
```
