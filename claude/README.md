# TechInterview.live — Claude Plugin

Connects **Claude Code** to your [techinterview.live](https://techinterview.live) account. Includes the `techinterview` MCP server and the `grill-interview-architect` skill, which guides Claude through a short Socratic discovery before creating interview questions or challenges.

## Install

```bash
/plugin marketplace add devilicecream/techinterview-plugin
/plugin install techinterview-live@techinterview-marketplace
```

Then run `/mcp` inside Claude Code and complete the browser OAuth 2.1 login.

Alternative (MCP server only, no skill):

```bash
claude mcp add --transport http techinterview https://api.techinterview.live/mcp
```

## Usage

Ask Claude to design a question or challenge, for example:

- "Design a senior backend system design interview question."
- "Create a multi-question coding and architecture challenge."
- "Start a live interview session from my challenge library."

Creating questions and challenges is free. Each live interview session uses 1 credit. If you are out of credits, Claude will tell you and point you to your techinterview.live account.

## Links

- Platform: [https://techinterview.live](https://techinterview.live)
- Privacy Policy: [https://techinterview.live/privacy](https://techinterview.live/privacy)
- Terms of Service: [https://techinterview.live/terms](https://techinterview.live/terms)
- Support: [walter@techinterview.live](mailto:walter@techinterview.live)
