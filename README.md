### Hi, I'm Saad 👋

I'm a founder building **[Grona](https://grona.ai)**, an AI CRO platform that turns upstream user research into shippable site optimizations. I'm a through-and-through **vibe coder** — I turned the dial up the moment it became obvious AI coding could change the world, and now most of what I ship runs through Claude Code on engineering, marketing, and ops.

Before founding, I spent a decade on the buy side of enterprise martech at DHL (Percolate, Marketo) and Mazda (Oracle, Jivox, DY). Most of what I build now is shaped by what real enterprise buyers actually reward versus what they quietly churn off of.

---

## How I work with Claude Code in production

These practices are extracted from a production monorepo (4 product repos, marketing, sales) running Claude Code on real work every day. None of this is theoretical. It's what stopped costing me time after months of iteration.

**Hierarchical CLAUDE.md, not one massive file.** I put a CLAUDE.md at each meaningful boundary: root monorepo, each product repo, each function (marketing, sales, ops). Each one starts with a pointer to its parent so the AI can walk up the tree when it needs broader context. One giant file forces the AI to re-parse the world on every task.

**Lookup tables over flat lists.** Instead of hoping the AI finds the right doc, I give it a decision table: "If the task is X, start with file Y." This eliminates 3-4 rounds of grep before useful work begins.

**Stack declarations that close defaults.** I tell Claude what the stack is and explicitly ban the alternatives ("never use Lucide, always @untitledui"). Without the ban, the AI defaults to whatever it saw most in training, regardless of what the codebase uses.

**Pre and post-flight checklists, built from real mistakes.** I keep a per-task checklist of things the AI has gotten wrong (bare percentages without "up to", missing icon imports, wrong button variants). It catches regressions cheaply, and it grows naturally from the `feedback` memories I save when I correct it.

**Modes for ops, not just for code.** Marketing, sales, and consulting workflows run as discrete "modes" with a trigger, numbered steps, data sources, and an output path. Claude becomes a repeatable operations tool, not a one-off assistant. The same shape works for "client prep," "weekly report," "prospect research."

**Phased agent dependencies, parallel where possible.** A marketing run has 4 phases: research (sequential) → strategy (sequential) → content generation (parallel: blog, social, ads, email) → QC (sequential). Marking which phases can run concurrently and which can't prevents wasted compute and keeps quality gates intact.

**Shared knowledge base across agents.** Every agent reads from the same product overview, brand strategy, target audience, and approved claims files. The blog writer doesn't contradict the ad copywriter, because they're pulling from the same source. The QC reviewer doesn't flag content that violates rules it never saw.

---

## What I'm building

- **[Grona](https://grona.ai)** — AI CRO platform. *Grona Research* runs upstream user research from real signals (vs. ChatGPT, which can only guess from public data). *Grona Optimize* rewrites and reships variants on your existing production site (vs. Lovable, which generates greenfield).
- **[Relevic](https://relevic.com)** — operating company.
- **Chairos** — senior operator practice helping mid-market companies adopt AI without theatrics.
- **MarketingOS** — internal multi-client marketing pipeline for running brand and content work at scale.

## Stack I work in daily

Next.js · TypeScript · Tailwind · Supabase · makerkit · Inngest · Apify · Vercel AI SDK · Anthropic Claude · OpenAI

## Reach me

- Email: **admin@relevic.com**
- Web: **[grona.ai](https://grona.ai)** · **[relevic.com](https://relevic.com)**
- LinkedIn: **[in/saadsohail5](https://linkedin.com/in/saadsohail5)**
