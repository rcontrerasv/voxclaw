# VoxClaw 🎙️

**Voice-enabled autonomous agent calls for OpenClaw**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## Overview

VoxClaw enables AI agents to make real phone calls and have autonomous conversations to complete business tasks.

```
OpenClaw Agent → VoxClaw → Real Phone Call → Structured Data Back
```

## Use Cases

- 📞 **Call businesses** to get information
- 📅 **Make appointments** and bookings
- ✅ **Verify data** with customer service
- 🔀 **Navigate phone trees** (IVR)
- 📋 **Follow up** on pending requests

## Architecture

```
┌─────────────────────────────────────────────────┐
│              OpenClaw Agent                     │
│  "Call Autopista and ask about requirements"   │
└─────────────────────────────────────────────────┘
                       ↓
┌─────────────────────────────────────────────────┐
│                  VoxClaw                        │
│  ┌──────────────┐  ┌──────────────────────────┐│
│  │    Twilio    │←→│ Deepgram Voice Agent API ││
│  │  (Telephony) │  │   (STT + LLM + TTS)      ││
│  └──────────────┘  └──────────────────────────┘│
└─────────────────────────────────────────────────┘
                       ↓
┌─────────────────────────────────────────────────┐
│              Structured Output                   │
│  { summary, transcript, extracted_data }        │
└─────────────────────────────────────────────────┘
```

## Tech Stack

| Component | Technology |
|-----------|------------|
| Telephony | Twilio Voice |
| Conversation | Deepgram Voice Agent API |
| LLM | Claude 3.5 Sonnet |
| TTS | Deepgram Aura |
| Runtime | Node.js / TypeScript |

## Cost Estimate

~$0.10 USD per minute of call time

## Status

🚧 **Under Development**

### Roadmap

- [ ] Phase 1: Basic outbound calls with script
- [ ] Phase 2: Dynamic LLM-powered conversation
- [ ] Phase 3: OpenClaw skill integration
- [ ] Phase 4: Inbound call support

## Getting Started

Coming soon.

## Related Projects

- [OpenClaw](https://github.com/openclaw/openclaw) - The AI agent framework
- [Deepgram](https://deepgram.com) - Voice AI platform
- [Twilio](https://twilio.com) - Cloud communications

## License

MIT
