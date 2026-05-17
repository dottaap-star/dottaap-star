### Hi, I'm Saad 👋

I'm a founder building **[Grona](https://grona.ai)**, two AI products that close the gap between marketing research and shipping on the website itself.

**Grona Research** is a Claude-powered chat with first-class access to your real marketing data: Facebook organic and ads, Instagram posts and comments, Google Ads, Similarweb traffic, and GA4. Paid media teams, SMEs, and marketing ops use it to research and benchmark their own brand and their competitors across every channel that matters, without stitching together six dashboards.

**Grona Optimize** is a Lovable-style editor, but for the **existing web** instead of greenfield. Edit your live site via chat, then either ship the change to 100% of traffic or run it as an A/B test. No new build, no migration, no rip-and-replace.

The two work together. A marketer comes in to understand their site, product positioning, and competitive landscape, then turns the insights into website changes or strategy direction for social and paid, all in one tool.

In the process of building Grona, we've cracked a handful of workflow pipelines that might be worth spinning out as standalone products one day. MarketingOS, our multi-client marketing pipeline, is the most obvious candidate. Quietly excited about what comes out of the rest. :)

I'm a through-and-through **vibe coder** who turned the dial up the moment it became obvious AI coding could change the world. Before founding, I spent a decade on the buy side of enterprise martech at DHL (Percolate, Marketo) and Mazda (Oracle, Jivox, DY). Most of what I build now is shaped by what real enterprise buyers reward versus what they quietly churn off of.

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

- **[Grona](https://grona.ai)** — Grona Research + Grona Optimize, see above
- **Chairos** — senior operator practice helping mid-market companies adopt AI without theatrics

## Stack I work in daily

Next.js · TypeScript · Tailwind · Supabase · makerkit · Inngest · Apify · Vercel AI SDK · Anthropic Claude · OpenAI

## Reach me

- Email: **admin@relevic.com**
- Web: **[grona.ai](https://grona.ai)**
- LinkedIn: **[in/saadsohail5](https://linkedin.com/in/saadsohail5)**
