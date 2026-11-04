# TechInterview.live — Official MCP Plugin (`techinterview-plugin`)

Connect **OpenAI Codex**, **ChatGPT**, **Claude**, **Claude Code**, and **Gemini CLI** to your [techinterview.live](https://techinterview.live) account via OAuth 2.1 PKCE.

Designed for Engineering Managers, Hiring Managers, and Tech Leads to:
- **Grill the EM (`grill-interview-architect` Skill)**: Socratic 2–3 turn discovery that turns real production failure modes into calibrated `Junior`, `Mid`, or `Senior` coding and system design challenges—never generic LeetCode trivia.
- **Build Your Question & Challenge Library for Free (`0 Credits`)**: Create and edit collaborative coding questions (`Monaco`) and system design architecture diagrams (`Mermaid` → `Excalidraw` canvas) with private interviewer rubrics.
- **Assemble Multi-Question Challenges (`0 Credits`)**: Combine existing and newly created questions into ordered interview loops for personal or team workspaces.
- **Launch Live Interview Sessions (`1 Credit`)**: Start live candidate sessions (`https://techinterview.live/r/<hash>`) using your credits, or generate a hosted Stripe Checkout link on demand when topping up.

---

## Quick Start

### 1. OpenAI Codex (`0.166.0+`)

#### Option A — Direct Remote MCP Command
```bash
codex mcp add techinterview --url https://api.techinterview.live/mcp
codex mcp login techinterview
```

#### Option B — `~/.codex/config.toml`
```toml
[mcp_servers.techinterview]
url = "https://api.techinterview.live/mcp"
```
Then authenticate with `codex mcp login techinterview`.

---

### 2. Claude Code

#### Option A — Install Full Plugin (MCP Server + `grill-interview-architect` Skill)
```bash
/plugin marketplace add devilicecream/techinterview-plugin
/plugin install techinterview-live@techinterview-marketplace
```

#### Option B — Direct Remote MCP Command
```bash
claude mcp add --transport http techinterview https://api.techinterview.live/mcp
```
Then run `/mcp` inside Claude Code to complete the browser OAuth 2.1 login.

---

### 3. Claude.ai & Claude Desktop (Connectors)
1. Open **Settings → Connectors → Add custom connector**.
2. Enter:
   - **Name**: `TechInterview.live`
   - **Remote MCP Server URL**: `https://api.techinterview.live/mcp`
3. Click **Connect** and authorize your `techinterview.live` account via Google or GitHub.

---

### 4. ChatGPT (Connectors)
1. Open **Settings → Connectors → Create / Add custom MCP connector**.
2. Enter:
   - **Name**: `TechInterview.live`
   - **MCP Server URL**: `https://api.techinterview.live/mcp`
   - **Authentication**: `OAuth` (auto-discovered via `https://api.techinterview.live/.well-known/oauth-protected-resource`).

---

### 5. Gemini CLI
Install directly as a Gemini CLI Extension (includes both the `techinterview` MCP server and `GEMINI.md` Interview Architect instructions):
```bash
gemini extensions install https://github.com/devilicecream/techinterview-plugin
```

---

## Included Tools & Prompts

### MCP Prompts
| Prompt | Description |
|---|---|
| `design-interview-question` | Interactively grill the EM to design a calibrated coding or system design question. |
| `design-interview-challenge` | Interactively grill the EM to design a multi-question Challenge loop. |

### MCP Tools
| Tool | Cost | Description |
|---|---|---|
| `get_account_and_credits` | Free | View profile, organizations, credit balance, and Stripe credit bundles. |
| `prepare_interview_design_brief` | Free | Load the "Grill the EM" Socratic rubric, platform rules, and existing library summary. |
| `list_questions` | Free | List interview questions in your personal or organization workspace. |
| `get_question` | Free | Inspect a question's `description_md`, starter `content`, and `interviewer_notes`. |
| `create_interview_question` | **Free (`0 credits`)** | Save a new `codeshare` (Monaco) or `diagram` (Mermaid → Excalidraw) question. |
| `update_interview_question` | **Free (`0 credits`)** | Update an existing question's description, starter code/diagram, or notes. |
| `list_challenges` | Free | List multi-question Challenges. |
| `get_challenge` | Free | Inspect a Challenge and its ordered sequence of questions. |
| `create_challenge` | **Free (`0 credits`)** | Create a Challenge from existing `question_ids` and/or inline `new_questions`. |
| `update_challenge` | **Free (`0 credits`)** | Rename a Challenge or reorder/replace its `question_ids`. |
| `create_interview_session` | **Paid (`1 credit`)** | Provision a live candidate session (`/r/<hash>`), or return a Stripe Checkout URL if credits are `0`. |
| `buy_credits_checkout_link` | Free | Generate a hosted Stripe Checkout link (`https://checkout.stripe.com/...`) to purchase credits. |

---

## Links & Support
- **Platform**: [https://techinterview.live](https://techinterview.live)
- **Privacy Policy**: [https://techinterview.live/privacy](https://techinterview.live/privacy)
- **Terms of Service**: [https://techinterview.live/terms](https://techinterview.live/terms)
- **Support**: [walter@techinterview.live](mailto:walter@techinterview.live)
