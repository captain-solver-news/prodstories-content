# AGENTS.md

## Writing posts

- We write content for [prodstories.com](https://prodstories.com).
- Read `.agents/product-marketing.md` for product context before writing.
- Be a skeptic when asked to describe our experience:
  - Evaluate whether the experience is worth a post.
  - Worth it → write it.
  - Not worth it → suggest what to learn or try next instead.
- Ask for anything needed for a high-quality article: GitHub repo links, commits, screenshots, proofs.
- Always write in English.

## Payload CMS (MCP)

- Posts live in the Payload CMS of `prodstories-blog`; access it through the `payload` MCP server.
- Server config: `.mcp.json`; endpoint `<PAYLOAD_URL>/api/mcp`.
- Full setup: `README.md` → "Payload CMS (MCP)".

### Connect

1. Check that the `payload` server is connected in your MCP status.
2. Not connected → ask the user to:
   - Export `PAYLOAD_URL` (no trailing slash) and `PAYLOAD_MCP_API_KEY` in `~/.zshrc`.
   - Create the key in `<PAYLOAD_URL>/admin` → **MCP API Keys** with the needed permissions.
   - Restart the agent from a terminal in this directory.
3. Agent does not read `.mcp.json` → register the same server in its own MCP config:
   - Transport: HTTP
   - URL: `<PAYLOAD_URL>/api/mcp`
   - Header: `Authorization: Bearer <PAYLOAD_MCP_API_KEY>`

### Rules

- Never write the API key or URL into tracked files.
- `PAYLOAD_URL` may point to production; confirm with the user before every create or update.
- No deletes.
- `body` is Lexical rich text JSON: read the post first, edit the node tree, send the full `body` back.
