# ProdStories Content Strategy

Content workspace for ProdStories. This repository holds no content of its own — it  
carries the **agent skills** that a coding agent (Claude Code, Codex, Cursor, Gemini  
CLI, OpenCode) loads when working on ProdStories content: strategy, copy, SEO, and  
distribution playbooks.

## Setup

After cloning, run:

```bash
npx skills experimental_install
```

This reads `skills-lock.json` and restores every pinned skill into `.agents/skills/`,
then creates the symlinks each agent expects. Requires Node.js (developed on v22).

Verify:

```bash
npx skills list
```

You should see 10 project skills, all resolving to `./.agents/skills/`.

## Installed skills

All 10 come from `[coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills)`.


| Stage          | Skill               | Version | What it covers                                                    |
| -------------- | ------------------- | ------- | ----------------------------------------------------------------- |
| **Plan**       | `content-strategy`  | 2.1.1   | Content pillars, topic clusters, editorial calendar, distribution |
|                | `site-architecture` | 2.0.0   | Page hierarchy, navigation, URL structure                         |
| **Create**     | `copywriting`       | 2.0.2   | Landing, pricing, feature and homepage copy                       |
| **Optimize**   | `seo-audit`         | 2.0.1   | Technical and on-page SEO diagnosis                               |
|                | `schema`            | 2.0.0   | Structured data and rich results                                  |
|                | `ai-seo`            | 2.5.0   | Getting cited by LLMs and AI search engines                       |
|                | `copy-editing`      | 2.0.0   | Seven-sweep editing of existing copy, content refresh             |
| **Distribute** | `social`            | 2.2.0   | Social posts, repurposing, short-form video                       |
| **Scale**      | `programmatic-seo`  | 2.0.0   | Templated pages generated at scale                                |
|                | `free-tools`        | 2.0.1   | Free calculators and generators as a marketing channel            |


## Managing skills

```bash
npx skills list                                        # what is installed
npx skills add coreyhaines31/marketingskills@<name>    # add one
npx skills remove <name>                               # remove one
npx skills update                                      # upgrade to latest
npx skills find <query>                                # search the ecosystem
```

These commands maintain `skills-lock.json` themselves.

## Payload CMS (MCP)

`.mcp.json` connects the AI agent to the Payload CMS of
[prodstories-blog](https://github.com/captain-solver-news/prodstories-blog) through
its MCP endpoint (`/api/mcp`, provided by `@payloadcms/plugin-mcp`). The agent can then
find, create and update posts, categories, authors, static contents and configs.

The file holds no URL or secret — both come from environment variables:


| Variable              | Value                                      |
| --------------------- | ------------------------------------------ |
| `PAYLOAD_URL`         | Site URL without a trailing slash          |
| `PAYLOAD_MCP_API_KEY` | API key from **MCP API Keys** in the admin |




### Get an API key

1. Open `<PAYLOAD_URL>/admin`. The admin is behind HTTP Basic Auth (ask the team for the
  credentials), then log in to Payload.
2. Go to **MCP API Keys** → **Create new**, enable the API key and copy it.
3. Tick the permissions the agent needs. All of them are off by default, so a key
  without ticks can do nothing. Prefer `find` + `update` on posts and leave `delete`
   off.

`/api/*` is not behind Basic Auth, so the MCP client only needs the API key.

### Configure the environment

The agent expands `${VAR}` in `.mcp.json` from the shell it was started in. Add to
`~/.zshrc`:

```bash
export PAYLOAD_URL=https://prodstories.com
export PAYLOAD_MCP_API_KEY=<api-key>
```

Point `PAYLOAD_URL` at `http://localhost:3000` to work against a local `prodstories-blog`.

Reload the shell (`source ~/.zshrc`), restart the agent in this directory, approve the
`payload` server if prompted, and check that it is connected in the agent's MCP status.

If a variable is unset, `${VAR}` stays unexpanded and the server fails to connect.
Desktop apps launched from the Dock do not read `~/.zshrc` — start the agent from a
terminal.

### Agents without `.mcp.json` support

Not every agent reads a project-level `.mcp.json`. For the others, register the same
server in the agent's own MCP config:

- Transport: HTTP
- URL: `<PAYLOAD_URL>/api/mcp`
- Header: `Authorization: Bearer <api-key>`

A server registered in the agent's own config also keeps the key out of git.
