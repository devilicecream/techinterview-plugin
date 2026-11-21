# TechInterview.live — Official Plugins

Design high-signal coding and system design interview questions, build multi-question challenges, and launch live interview sessions on [techinterview.live](https://techinterview.live).

This repository holds one folder per provider. Each folder is self-contained so it can be submitted or packaged on its own.

| Provider | Folder | Contents |
|---|---|---|
| Claude (Claude Code, Claude Desktop) | [`claude/`](./claude) | Plugin manifest, MCP config, `grill-interview-architect` skill |
| OpenAI (Codex, ChatGPT) | [`openai/`](./openai) | Plugin manifest, review metadata, MCP config, `grill-interview-architect` skill |
| Gemini CLI | [`gemini/`](./gemini) | Extension manifest and `GEMINI.md` instructions |

Also at the root:
- `server.json`: MCP registry metadata for the remote server (`https://api.techinterview.live/mcp`). It is not a plugin.
- `.claude-plugin/marketplace.json` and `.agents/plugins/marketplace.json`: marketplace listings that point at the `claude/` and `openai/` folders.

See each provider's README for install steps and tool reference.

## License

MIT. See [`LICENSE`](./LICENSE).
