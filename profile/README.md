<p align="center">
  <img src="https://raw.githubusercontent.com/openvole/openvole/main/assets/vole.png" alt="OpenVole" width="150">
</p>

<h1 align="center">OpenVole</h1>

<p align="center">
  <strong>Microkernel AI agent framework. The smallest possible thing that other useful things can be built on top of.</strong>
</p>

---

## Repositories

| Repo | Purpose | npm |
|------|---------|-----|
| [openvole](https://github.com/openvole/openvole) | Agent core — loop, registries, CLI, sandbox | [![npm](https://img.shields.io/npm/v/openvole)](https://www.npmjs.com/package/openvole) |
| [pawhub](https://github.com/openvole/pawhub) | Official paws — 28 plugins for LLM, channels, tools, infra | [![npm](https://img.shields.io/npm/v/@openvole/paw-brain)](https://www.npmjs.com/package/@openvole/paw-brain) |

## Quick Start

```bash
mkdir my-agent && cd my-agent
npm init -y
npm install openvole @openvole/paw-brain @openvole/paw-memory @openvole/paw-dashboard
npx vole init
npx vole start
```

Set your LLM provider in `.env`:

```
BRAIN_PROVIDER=gemini
GEMINI_API_KEY=your-key
```

## Architecture

```
Core (agent loop) → Paws (plugins) → Skills (behavioral recipes)
```

- **Core** is LLM-ignorant — it runs the loop, nothing else
- **Paws** connect to the world — LLMs, Telegram, shell, browser, desktop
- **Skills** describe behavior — markdown files, no code

## Paws (28)

**Brain**: paw-brain (Anthropic, OpenAI, Gemini, xAI, Ollama)
**Channels**: Telegram, Slack, Discord, WhatsApp, Teams, Voice Call
**Tools**: Browser, Shell, Filesystem, MCP, Email, GitHub, Calendar, Computer, TTS, STT
**Infra**: Memory, Session, Compact, Dashboard

## Links

- [Documentation](https://openvole.github.io/openvole/)
- [Changelog](https://github.com/openvole/openvole/blob/main/docs/changelog.md)
- [Contributing](https://github.com/openvole/openvole/blob/main/CONTRIBUTING.md)

## License

MIT
