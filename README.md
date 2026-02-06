# Phonon 🎙️

**Voice-enabled autonomous agent calls**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> *Phonon: A quantum of sound energy - the voice particle for AI agents*

---

## Overview

Phonon is a **standalone library** that enables AI agents to make real phone calls and have autonomous conversations to complete business tasks.

```
Your AI Agent → Phonon → Real Phone Call → Structured Data Back
```

## Multi-Platform Support

Phonon is designed to integrate with multiple agent frameworks:

| Platform | Adapter | Status |
|----------|---------|--------|
| [OpenClaw](https://github.com/openclaw/openclaw) | `@phonon/adapter-openclaw` | 🚧 Planned |
| [Aden Hive](https://github.com/adenhq/hive) | `@phonon/adapter-hive` | 🚧 Planned |

## Use Cases

- 📞 **Call businesses** to get information
- 📅 **Make appointments** and bookings
- ✅ **Verify data** with customer service
- 🔀 **Navigate phone trees** (IVR)
- 📋 **Follow up** on pending requests

## Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                      Phonon Core                            │
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
| `@phonon/core` | Core library - telephony, voice agent, conversation |
| `@phonon/adapter-openclaw` | OpenClaw skill integration |
| `@phonon/adapter-hive` | Aden Hive MCP tool integration |

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
npm install @phonon/core

# With OpenClaw
npm install @phonon/adapter-openclaw

# With Aden Hive
pip install phonon-hive
```

## Why "Phonon"?

In physics, a **phonon** is a quantum of vibrational/sound energy - the smallest unit of sound in a material. Just as phonons carry sound through matter, Phonon carries voice through AI systems.

## Contributing

We welcome contributions! Check out our [contributing guide](CONTRIBUTING.md).

## Links

- 🌐 Website: [phonon.sh](https://phonon.sh) *(coming soon)*
- 📦 NPM: `@phonon/core` *(coming soon)*
- 🐙 GitHub: [github.com/rcontrerasv/phonon](https://github.com/rcontrerasv/phonon)

## Related Projects

- [OpenClaw](https://github.com/openclaw/openclaw) - Personal AI assistant
- [Aden Hive](https://github.com/adenhq/hive) - Autonomous business process framework
- [Deepgram](https://deepgram.com) - Voice AI platform
- [Twilio](https://twilio.com) - Cloud communications

## License

MIT
