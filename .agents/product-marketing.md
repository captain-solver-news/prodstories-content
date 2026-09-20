# ProdStories — Product Marketing Context

> Shared context for every agent skill in this repo (`content-strategy`, `copywriting`,
> `seo-audit`, `ai-seo`, `social`, …). Read this before asking the user anything.
> Last reviewed: 2026-09-20.

---

## 1. What ProdStories Is

**ProdStories is a technical blog written by four working developers who publish what
they actually built, broke, and fixed — in public, while it is still messy.**

Not a tutorial farm, not a news aggregator, not an agency blog with a demo CTA.
Every piece is first-hand: the code shipped, the tool evaluated, the decision regretted.

**One-liner:** *Engineering stories from four developers building in public.*

**Audience language:** English only. All content is written for an English-speaking,
global developer audience. No localized versions planned.

---

## 2. Why We Exist (Goals)

Ranked. Everything in the editorial calendar serves these, in this order:

1. **Traffic and audience (primary).** Grow organic search traffic and a returning
   readership. Success at 12 months: a compounding organic search baseline and a
   body of work strong enough that readers return to the blog directly.
2. **Personal brand and hiring (secondary).** The four authors become recognizable
   engineers. Success looks like: inbound offers, speaking or podcast invitations,
   contributor interest, credibility in the agentic-dev community.

**Explicit non-goals:** selling services, selling a SaaS product, sponsorship revenue,
and **email — no newsletter, no list, no email capture of any kind.** Nothing should be
written *primarily* to convert, and no post should end with a subscribe prompt.

**What this implies for content:** we optimize for *reach and reputation*, not leads.
Decision-stage and pricing-style content is irrelevant to us. A shareable post that
earns 500 qualified readers beats a keyword-stuffed post that earns 2,000 bounces.

---

## 3. Ideal Reader (ICP)

**Technical solo builders** — engineers who build and run their own products alone or
in a pair. Their background is engineering, not growth hacking: they came to product
work through code and they judge everything by whether it holds up in a real codebase.

*Not* the hustle-culture "indie hacker" archetype — no growth tricks, no MRR-screenshot
culture, no ship-it-broken-and-tweet-about-it. We write for the person who wants to
understand how the thing works before shipping it.

| | |
|---|---|
| **Role** | Solo developer running their own product, technical founder, freelance engineer with side projects, two-person team |
| **Seniority** | Mid to senior — can read code, does not need "what is an API" |
| **Stack overlap** | TypeScript/JavaScript first; Next.js, Node/Nest, Python; Postgres, Mongo, Firebase; heavy AI-tool users |
| **Constraint** | Time and money. One person doing product, code, design, and marketing |
| **Motivation** | Make sound technical decisions without a team to argue them with, and avoid rabbit holes someone else already mapped |

**What they want from us:**
- Honest verdicts on AI tools and agentic workflows — *does this actually save time, or is it a demo trick?*
- The reasoning behind a technical decision, not just the final config — trade-offs, what we rejected, why
- Concrete "here's what it cost us and what broke" accounts, with numbers
- Techniques they can read, understand, and adapt into their own repo the same evening
- A second engineering opinion, since they have no colleague to review the decision

**What they ignore:** enterprise architecture and team-process content (no team to apply
it to), growth-hack and "$0 to $10k MRR" material, vendor-sponsored posts, listicles
with no first-hand use, and tutorials that hand over code with no explanation.

**Where they are:** Hacker News, Lobsters, `r/webdev`, `r/node`, `r/nextjs`,
`r/LocalLLaMA`, `r/ExperiencedDevs`, dev.to, X/Twitter engineering circles,
niche Discords (Next.js, Claude/agent tooling).
These would be our **borrowed** channels — see §9.

---

## 4. Our Differentiation

Three things competitors structurally cannot copy:

1. **First-hand only.** We never write about a tool we haven't run in a real repo.
   Every post carries evidence: screenshots, diffs, timings, failures, costs.
2. **We publish the failures.** The "what went wrong" section is mandatory, not
   decorative. This is the part readers share.
3. **Our quality bar is itself a product.** We are building an in-house **Reviewer
   skill** — an independent AI arbiter that scores every article against E-E-A-T
   before publication. No competing dev blog submits itself to an automated,
   disclosed quality audit. This is our proof of trustworthiness *and* a recurring
   content subject.

**Positioning statement:**
> For engineers building their own products without a team to consult, ProdStories is
> a developer blog where four working engineers publish what actually happened when
> they used the tool — the reasoning, the numbers, and the parts that failed — with
> every article independently scored for expertise before it ships.

---

## 5. The Team (E-E-A-T Backbone)

Four developers. Real names and bylines on every post — no house account, no ghostwriting.

**Shared stack (our credible surface area):**
NestJS · Next.js · TypeScript · Python · PostgreSQL · MongoDB · Firebase · Git

**Hard rule:** never claim expertise we don't have. Where we're learning (see the
Game Development pillar), we say so explicitly — a disclosed beginner is trustworthy;
an undisclosed one is not, and our own Reviewer skill will flag it.

---

## 6. Content Pillars

Three pillars, each with subcategories. Subcategories are the real unit of planning —
a pillar with no subcategories produces random posts.

### Pillar 1 — AI Agents & Agentic Engineering
*Our sharpest wedge. Highest interest among technical solo builders, highest shareability,
strongest overlap with what we're genuinely doing daily.*

- **Agent skills & tooling** — writing, structuring, versioning, and evaluating skills
- **AI-assisted workflows** — design, code review, docs, QA in a real dev loop
- **LLM evaluation & quality** — evals, scoring rubrics, E-E-A-T, measuring "is it good"
- **Building agents on our stack** — Nest/Python/Postgres backends for agentic systems
- **Tool teardowns** — honest verdicts on AI dev tools we actually ran

### Pillar 2 — Web Development
*Our deepest expertise and our search-traffic foundation.*

- **Next.js & frontend** — App Router, rendering, performance, real migrations
- **NestJS & backend** — API design, architecture, auth, background jobs
- **Databases** — Postgres vs Mongo decisions, Firebase in practice, schema modeling
- **TypeScript & DevEx** — types that earn their keep, tooling, Git workflow
- **Ship logs** — how a specific feature of ours was actually built

### Pillar 3 — Game Development (Learning in Public)
*No prior expertise — this is explicitly a learning series, labeled as such.*

- **Devlog series** — sequential, honest, "week N of not knowing what we're doing"
- **Web-first game tech** — PixiJS, Cocos, Phaser, Three.js, WebGL, Canvas: the bridge from our
  actual JS/TS expertise into gamedev, so we're never fully outside our competence
- **What transfers from web dev** — and what absolutely does not
- **Tooling & assets on a budget** — including AI-generated art/audio experiments

**Why this shape:** pillars 1 and 2 carry search and authority; pillar 3 carries
narrative and return visits. A learning series is the one format where inexperience
is an asset — but only while it's honestly framed.

### Cross-cutting lens: Build in Public
Not a pillar — a **lens applied across all three**. "How we built ProdStories itself"
posts live inside the relevant pillar, tagged as a series.

⚠️ **Note on the two planned articles:** both the *Google Stitch Web Design Case* and
the *Reviewer Skill* post are build-in-public/meta pieces. They are excellent
shareable launch material and perfect brand-setting first posts — but meta content
earns near-zero search traffic. Pair each with at least one searchable post in the
same subcategory, or the blog's search baseline never starts compounding.

---

## 7. Voice & Tone

- **First person plural.** "We tried", "we broke it", "we'd do it differently."
- **Evidence over adjectives.** Numbers, screenshots, diffs, commit links, costs.
- **Failures stay in.** The dead end is the value, not an embarrassment to trim.
- **No hype, no hedging.** Give a verdict. "Don't use this for X" is allowed.
- **Plain, direct English.** All four authors are non-native speakers writing for a
  native audience: prefer short sentences and concrete nouns over clever idiom.
  Consistency of voice across four bylines matters more than individual flair.
- **Never:** "In today's fast-paced world", "game-changer", "unlock the power of",
  "dive deep", AI-slop transitions, invented statistics.

---

## 8. Current State & Resources

| | |
|---|---|
| **Existing content** | None. Launching from zero. |
| **Domain authority** | Zero — no backlinks, no history |
| **Team** | 4 developers, all writing |
| **Target cadence** | 8+ posts/month (~2/month per author) |
| **Formats available** | Written posts, code repos, screenshots/diagrams; video and podcast not yet |
| **Budget** | Effectively zero — time is the only resource |
| **CMS / platform** | TODO — see `references/headless-cms.md` |
| **Analytics / GSC** | TODO — needed before any keyword prioritization is real |

**Cadence reality check:** 8+/month from zero authority is aggressive. Protect quality
by batching: the Reviewer skill must gate publication, and a slipped week is better
than a thin post — a new domain has no reputation to absorb weak content.

---

## 9. Distribution (ORB)

**Current plan — deliberately narrow:**

- **Owned:** the blog itself. The only asset we control. No email list, by decision —
  which means search rankings and direct return visits are the *entire* owned layer,
  and both depend on the archive being worth coming back to.
- **Rented:** **LinkedIn and X.** We post a link to each new article on both. LinkedIn
  also carries the hiring/personal-brand goal; X reaches the build-in-public crowd.
- **Borrowed:** none planned yet.

Every post ships with its LinkedIn and X posts written *before* publishing — the link
share is part of the piece, not an afterthought. Write pull quotes and a standalone
hook line into the draft so there is something to post besides the title.

⚠️ **Consequence to watch.** With no email list, we have no way to reach a reader twice
except by them choosing to come back or an algorithm choosing to show us. For the first
~6 months a zero-authority domain gets almost nothing from Google, so LinkedIn and X
carry essentially all early traffic. If growth stalls, the cheapest unlock is the
borrowed layer — a Hacker News, Lobsters, or subreddit post costs nothing but the
writing we already did, and reaches people who have never heard of us.

---

## 10. Competitive Landscape

**Direct (independent engineering writing):** personal engineering blogs, dev.to and
Lobsters top authors, small-team build-in-public blogs with real technical depth.
**Indirect (owns the searches we want):** LogRocket, Smashing Magazine, freeCodeCamp,
vendor blogs (Vercel, Supabase, Anthropic), and the AI-generated tutorial glut.

**Structural gap we exploit:** the big publications are commissioned and generic —
technically correct, experientially hollow. Nobody writing at their scale can say
"we ran this for three weeks and here's the bill." Our moat is specificity, not volume.

**TODO:** name 3–5 concrete competitor blogs to track and audit quarterly.

---

## 11. Voice of Customer — NOT YET COLLECTED

⚠️ **This section is empty and it is the single biggest gap in this document.**
Customer Impact carries 40% of the weight in `content-strategy`'s prioritization
scoring. With no real reader language here, that 40% is guesswork.

**How to fill it without having an audience yet:**
1. Mine 20–30 Hacker News / Lobsters / Reddit threads in our pillars; copy the
   exact phrasing people use for their frustrations, verbatim.
2. Collect recurring questions from those threads into a raw list.
3. After launch, add: search queries from GSC, blog comments, and replies to our
   LinkedIn and X posts.

Paste raw quotes below as they're gathered — verbatim, never paraphrased.

> _(empty)_

---

## 12. Open Questions

- Which author owns which pillar?
- Domain and CMS decision
- Is there any adjacent product we might build later that content should warm up?
- Publication name/handle consistency across platforms (for `ai-seo` brand consistency)
