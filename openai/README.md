# TechInterview.live — OpenAI Codex / ChatGPT Plugin

Connects **OpenAI Codex** and **ChatGPT** to your [techinterview.live](https://techinterview.live) account via OAuth 2.1 PKCE. Includes the `techinterview` MCP server and the `grill-interview-architect` skill.

Designed for Engineering Managers, Hiring Managers, and Tech Leads to:
- **Grill the EM (`grill-interview-architect` skill)**: Socratic discovery that turns real production failure modes into calibrated `Junior`, `Mid`, or `Senior` coding and system design challenges.
- **Build your question and challenge library (free)**: Create coding questions (`Monaco`) and system design questions (`Mermaid` to `Excalidraw`) with private interviewer rubrics, and assemble them into multi-question challenges.
- **Launch live interview sessions (`1 credit` each)**: Start candidate sessions (`https://techinterview.live/r/<hash>`).

## Install

### OpenAI Codex (`0.166.0+`)

Direct remote MCP command:

```bash
codex mcp add techinterview --url https://api.techinterview.live/mcp
codex mcp login techinterview
```

Or add it to `~/.codex/config.toml`:

```toml
[mcp_servers.techinterview]
url = "https://api.techinterview.live/mcp"
```

Then authenticate with `codex mcp login techinterview`.

### ChatGPT (Connectors)

1. Open **Settings → Connectors → Create / Add custom MCP connector**.
2. Enter:
   - **Name**: `TechInterview.live`
   - **MCP Server URL**: `https://api.techinterview.live/mcp`
   - **Authentication**: `OAuth` (auto-discovered via `https://api.techinterview.live/.well-known/oauth-protected-resource`).

## MCP Tools

| Tool | Cost | Description |
|---|---|---|
| `get_account_and_credits` | Free | View profile, organizations, and credit balance. |
| `prepare_interview_design_brief` | Free | Load the "Grill the EM" rubric, platform rules, and existing library summary. |
| `list_questions` | Free | List interview questions in your personal or organization workspace. |
| `get_question` | Free | Inspect a question's `description_md`, starter `content`, and `interviewer_notes`. |
| `create_interview_question` | Free (`0 credits`) | Save a new `codeshare` (Monaco) or `diagram` (Mermaid to Excalidraw) question. |
| `update_interview_question` | Free (`0 credits`) | Update an existing question's description, starter code/diagram, or notes. |
| `list_challenges` | Free | List multi-question Challenges. |
| `get_challenge` | Free | Inspect a Challenge and its ordered sequence of questions. |
| `create_challenge` | Free (`0 credits`) | Create a Challenge from existing `question_ids` and/or inline `new_questions`. |
| `update_challenge` | Free (`0 credits`) | Rename a Challenge or reorder/replace its `question_ids`. |
| `create_interview_session` | Paid (`1 credit`) | Provision a live candidate session (`/r/<hash>`). With 0 credits it returns an error explaining you are out of credits and pointing to your account page. |

## Links & Support
- **Platform**: [https://techinterview.live](https://techinterview.live)
- **Privacy Policy**: [https://techinterview.live/privacy](https://techinterview.live/privacy)
- **Terms of Service**: [https://techinterview.live/terms](https://techinterview.live/terms)
- **Support**: [walter@techinterview.live](mailto:walter@techinterview.live)

## Building the directory submission ZIP

The OpenAI plugin directory takes a flat ZIP in the portable format. Review data (test cases, demo video, commerce declaration, release notes) lives in `plugin.json` under `extensions.com.openai`. From this folder:

```bash
zip -X ../techinterview-live-openai.zip plugin.json mcp.json skills/grill-interview-architect/SKILL.md assets/logo.png
```

Reviewer demo credentials go in the dashboard's Review details, never in the ZIP.
