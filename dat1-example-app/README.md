# dat1 Example Chat App

Simple chat interface demonstrating integration with the dat1 predeployed gpt-oss-120b model. Supports both streaming and non-streaming responses.

## Setup

1. Add your dat1 API key to `.env`:
```
DAT1_API_KEY=your_key_here
```

2. Install dependencies and run:
```bash
pnpm install
pnpm dev
```

3. Open [http://localhost:3000](http://localhost:3000)

## Project Structure

```
dat1-example-app/
├── app/
│   ├── api/
│   │   ├── chat/          # Non-streaming chat endpoint
│   │   └── chat-stream/   # Streaming chat endpoint
│   ├── page.tsx           # Main chat interface
│   ├── layout.tsx         # App layout
│   └── globals.css        # Global styles
├── public/                # Static assets
└── package.json
```

## What It Does

Chat interface with two modes:
- **Streaming**: Real-time token-by-token response display
- **Non-Streaming**: Complete response returned at once

Both modes show performance metrics (prompt time, generation speed, token count).

## Use a custom deployed model

See `dat1-deploy-custom-models/llama-chat` for an example on how to deploy a custom LLM to dat1. Then use env var `DAT1_CHAT_ENDPOINT_OVERRIDE` to change the chat endpoint.