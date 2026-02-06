# VoxClaw 🎙️

**Voice-enabled autonomous agent calls**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## Overview

VoxClaw is a **standalone library** that enables AI agents to make real phone calls and have autonomous conversations to complete business tasks.

```
Your AI Agent → VoxClaw → Real Phone Call → Structured Data Back
```

## Multi-Platform Support

VoxClaw is designed to integrate with multiple agent frameworks:

| Platform | Adapter | Status |
|----------|---------|--------|
| [OpenClaw](https://github.com/openclaw/openclaw) | `@voxclaw/adapter-openclaw` | 🚧 Planned |
| [Aden Hive](https://github.com/adenhq/hive) | `@voxclaw/adapter-hive` | 🚧 Planned |

## Use Cases

- 📞 **Call businesses** to get information
- 📅 **Make appointments** and bookings
- ✅ **Verify data** with customer service
- 🔀 **Navigate phone trees** (IVR)
- 📋 **Follow up** on pending requests

## Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                      VoxClaw Core                           │
│           (Standalone library - TypeScript)                 │
│                                                             │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐ │
│  │   Twilio    │  │  Deepgram   │  │  Conversation Mgr   │ │
│  │   Client    │  │ Voice Agent │  │  (State, Prompts)   │ │
│  └─────────────┘  └─────────────┘  └─────────────────────┘ │
└─────────────────────────────────────────────────────────────┘
           ↑                                    ↑
           │                                    │
┌──────────────────────┐          ┌──────────────────────────┐
│  OpenClaw Adapter    │          │   Aden Hive Adapter      │
│  (Skill)             │          │   (MCP Tool)             │
└──────────────────────┘          └──────────────────────────┘
```

## Packages

| Package | Description |
|---------|-------------|
| `@voxclaw/core` | Core library - telephony, voice agent, conversation |
| `@voxclaw/adapter-openclaw` | OpenClaw skill integration |
| `@voxclaw/adapter-hive` | Aden Hive MCP tool integration |

## Tech Stack

| Component | Technology |
|-----------|------------|
| Telephony | Twilio Voice |
| Conversation | Deepgram Voice Agent API |
| LLM | Claude 3.5 Sonnet |
| TTS | Deepgram Aura |
| Runtime | Node.js / TypeScript |
| Monorepo | Turborepo |

## Cost Estimate

~$0.10 USD per minute of call time

## Status

🚧 **Under Development**

### Roadmap

- [ ] Phase 1: Core library - basic outbound calls
- [ ] Phase 2: Dynamic LLM-powered conversation
- [ ] Phase 3: OpenClaw adapter
- [ ] Phase 4: Aden Hive adapter
- [ ] Phase 5: Inbound call support

## Getting Started

Coming soon.

```bash
# Install (planned)
npm install @voxclaw/core

# With OpenClaw
npm install @voxclaw/adapter-openclaw

# With Aden Hive
pip install voxclaw-hive
```

## Contributing

We welcome contributions! Check out our [contributing guide](CONTRIBUTING.md).

## Related Projects

- [OpenClaw](https://github.com/openclaw/openclaw) - Personal AI assistant
- [Aden Hive](https://github.com/adenhq/hive) - Autonomous business process framework
- [Deepgram](https://deepgram.com) - Voice AI platform
- [Twilio](https://twilio.com) - Cloud communications

## License

MIT
