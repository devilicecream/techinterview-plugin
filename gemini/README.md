# TechInterview.live — Gemini CLI Extension

Connects **Gemini CLI** to your [techinterview.live](https://techinterview.live) account. The extension includes the `techinterview` MCP server and the `GEMINI.md` "Grill the EM" interview architect instructions.

## Install

```bash
gemini extensions install https://github.com/devilicecream/techinterview-plugin
```

The extension manifest and `GEMINI.md` are in this `gemini/` folder.


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

## Credits

One credit covers one live interview session. Creating questions and challenges is free. If you are out of credits, check your techinterview.live account.

## Links & Support
- **Platform**: [https://techinterview.live](https://techinterview.live)
- **Privacy Policy**: [https://techinterview.live/privacy](https://techinterview.live/privacy)
- **Terms of Service**: [https://techinterview.live/terms](https://techinterview.live/terms)
- **Support**: [walter@techinterview.live](mailto:walter@techinterview.live)
