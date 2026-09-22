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

