# 03 — Product & Distribution Architecture

## 1. Pipeline

```
INPUT: url | description  (+ country, business model — inferred, user-confirmable)
   │
   ├─ 1. COMPETITOR PANEL (5–7 leaders, editable list — human confirmation is both
   │     a feature agencies want and the legal aggregation safeguard)
   │     sources: AnswerMonk visibility scores ("brands AI actually recommends")
   │              + lookalike APIs (Exa/Ocean.io/Similarweb) + user edits
   │
   ├─ 2. EVIDENCE ENGINE
   │     logged-out headless screenshots (robots.txt / EU-TDM-opt-out respecting)
   │     Brandfetch token pulls · multi-engine LLM vision + copy analysis
   │     → per-competitor brand-DNA cards → CATEGORY-CONVENTIONS SYNTHESIS
   │       (abstract descriptors only — layout archetypes, palette ranges,
   │        tone dimensions, proof-point patterns; tiered floor/signal/differentiator
   │        exactly like AnswerMonk's CategoryKnowledgeGraph)
   │
   ├─ 3. THREE BRAND DIRECTIONS  (generation receives ONLY the abstractions
   │     + the user's own positioning inputs — never competitor assets)
   │     tokens · type pairings · executable voice constraints · copy patterns
   │     per landing section · positioning rationale citing the evidence
   │     · type-lockup wordmark concepts (logo direction brief, not finished marks)
   │
   ├─ 4. DISTINCTIVENESS GATE  (per studied competitor: color distance, font diff,
   │     tagline embedding similarity, logo geometry) — auto-reject near-matches;
   │     the score ships in the report
   │
   └─ 5. DELIVERABLE: white-labelable web report + download row
         DESIGN.md · tokens.json (DTCG) · shadcn globals.css · Lovable Knowledge
         file · AEO annex · copy-prompt buttons ("Open in v0 / Lovable / Claude Code")
```

**Do NOT build a page builder.** Lovable ($6.6B, ~8M users), Framer, Bolt, v0, and Wix commoditized generation. Brando is the upstream "brand brain" whose output makes all of them better — their tens of millions of users are TAM, not competition.

## 2. AnswerMonk asset-reuse map

| Brando needs | Already exists in AnswerMonk | Gap to build |
|---|---|---|
| Crawl a site | `server/crawler.ts` (puppeteer-core) | Screenshot capture (~1 line) + archive |
| Understand the business | `url-analyzer`, Claude business classification | Country/business-model inference confirm UI |
| Find segment leaders | `segment-analysis/comparison-targets`, GEO visibility scores, geographic-precision prompt engine | Lookalike-API blend + editable panel UI |
| Category norms | `brand-intelligence/knowledge-graph.ts` — CategoryKnowledgeGraph with winners, winner wedges, attribute norms tiered floor/signal/differentiator | Add VISUAL attributes (palette, type, layout archetypes, imagery style) to the messaging attributes it already tracks |
| Brand narrative | `brandsmith` (voice archetype, positioning, messaging frameworks + BrandSection schema) | Extend to executable voice constraints + per-section copy patterns |
| Multi-engine AI | OpenAI + Anthropic + Gemini pipeline | Vision-model teardown prompts |
| AEO substance | The entire GEO scoring/citation stack | Generator side: JSON-LD, entity kit, SSR instructions |
| Distribution | Existing customers, answermonk.ai credibility, newsletter | Brando landing page + Stripe |

This is why the concierge test costs ~zero: the pipeline exists; only the packaging is manual.

## 3. Output formats (the format war is settled — superset the winners)

- **Canonical: one LLM-readable markdown brand book**, DESIGN.md-compatible (YAML front-matter tokens + prose rationale — the pattern Google Labs open-sourced in 2026). Works today in Claude Code, Cursor, Lovable (Knowledge file), v0, Stitch, Copilot with zero plan gating. Extended with the sections the spec lacks: voice/tone constraints, per-section copy patterns, logo usage, AEO blocks.
- **Everything else mechanically derived from it:** DTCG v2025.10 `tokens.json` (Figma native import / Tokens Studio / Style Dictionary v5), shadcn `globals.css` with OKLCH vars + Tailwind v4 `@theme` block, an HTML style-guide page that doubles as preview and html.to.design Figma import.
- **Figma strategy in order of effort:** native DTCG JSON import → documented Tokens Studio path → Figma MCP write-to-canvas recipe → (later) small plugin. **Never build on the Variables REST API — write access is Enterprise-only and excludes the entire ICP.**
- **Voice ships as executable system-prompt constraints, not adjectives:** tone sliders, always/never lexicon, sentence-length rules, golden samples and anti-samples per section (hero, CTA, pricing, FAQ). This visual+verbal bundle in one agent-ready file is the clearest format whitespace.
- Premium later: each generated brand hosted as a shadcn registry consumable via MCP in v0/Cursor — the 2026-native equivalent of delivering a Figma library.

## 4. AEO scope (honest, verifiable — this protects AnswerMonk's credibility too)

**Ship as substance:**
1. **SSR/static-HTML requirement in the handoff spec** — no major AI crawler (GPTBot, ClaudeBot, PerplexityBot) executes JavaScript; default Lovable/v0 CSR output is invisible to AI engines. Include explicit SSR instructions + a "what GPTBot sees" rendered-HTML diff in the report.
2. **Pre-filled JSON-LD @graph** (Organization + Product/Service + FAQPage) with entity-consistent naming; meta/OG; sitemap directives.
3. **Entity kit as a first-class deliverable:** canonical brand name/description, sameAs links, consistent boilerplate for site, directories, and profiles — one of the few GEO practices with broad practitioner consensus.
4. **Princeton-validated copy rules baked into the copy engine:** direct answer in the first 40–60 words of each section, statistics, quotable expert-voice lines, citations, fluent authoritative prose (KDD GEO paper: 30–40% citation-visibility lift). Skip the proven-useless tactics (keyword stuffing, padding).
5. **Off-page action checklist** (G2/directories/Reddit/PR canonical descriptions) — which funnels straight into AnswerMonk monitoring.

**Never:** lead with llms.txt (generate it, position it honestly — 97% of llms.txt files get zero AI-bot fetches; IDE agents read it, search crawlers don't); promise AI-visibility growth from on-page work (~40% of citations come from Reddit; own site ~12%). **Sell AEO as high-intent conversion insurance (AI referrals ~1% of traffic, ~4x conversion), measured by AnswerMonk.** The buyer overlap is GEO-literate; overclaiming damages both products.

## 5. Agent-discovery strategy ("which model gets discovered by agents")

Two distinct games, one architecture:

**Game 1 — being RECOMMENDED by assistants** ("best tool to fix my generic Lovable site"): won *off-site*. ChatGPT cites a vendor's own site ~12% of the time; G2/Capterra get ~zero AI citations; winners are year-stamped comparison-table listicles, genuine Reddit presence, and 4+ independent source mentions (2.8x citation lift). **This is AnswerMonk's exact competency — run AnswerMonk on Brando from day one and publish the case study; it markets both products.**

**Game 2 — being INVOKED by agents mid-task:** the winning form factor is a **remote MCP server wrapping a deterministic REST API**, because one MCP codebase now reaches Claude/Claude Code (Connectors Directory), ChatGPT (Apps SDK is MCP-based), Cursor/Windsurf/Zed, and Lovable (MCP-standard connectors). Precedents in this exact category: Context7 (240k weekly downloads), 21st.dev Magic, Canva's AI Connector. The invocation moment is **project-scaffold time inside coding agents** — not chat.

Form-factor priority: **SKILL.md first** (days of work, ~40 products consume it, qualifies for the curated directory, doubles as living API docs) → **remote MCP server** (two tools: `generate_brand_pack`, `get_competitor_teardown`) → web app as the canonical entity, billing, and demo theater (it will NOT be discovered by agents) → ChatGPT app as a thin MCP derivative → Figma plugin last.

Agent-legibility spec: deterministic brand-pack JSON schema (same input → same output, so agents can cache/diff); OpenAPI + MCP tools + skill generated from one source of truth; markdown content negotiation on docs; llms.txt on the docs domain (the one place it works); machine-readable pricing endpoint; instant API-key provisioning so an agent completes signup-to-output in one session; **tool descriptions written as ad copy** ("researches your segment's top brands and returns a ready-to-apply design system") — models choose tools by description alone. Monetize per-invocation with x402/Stripe agent-payable checkout so an agent can buy a pack mid-session.

**Strategic caveat (from the scoring):** this is a *channel*, not the wedge — usage concentrates in the top ~50 MCP servers, installed ≠ invoked, and default-pick placement (Supabase-in-Lovable dynamics) is gatekept by partner programs. Apply to Lovable's partner program immediately; expect nothing; instrument everything. Positioning guardrail vs Canva: Canva's MCP *applies an existing* brand kit — Brando *creates* the brand system from market evidence. "The brand layer for AI builders — upstream of Canva, Magic, and v0."

## 6. Legal architecture (non-negotiable, built-in before the Sept 2026 Andersen v. Stability trial)

1. **Aggregation, never emulation:** always a panel of 5+ leaders distilled into CATEGORY conventions as abstract descriptors; no "make my brand like [X]" path anywhere. Category conventions are unprotectable; a single competitor's distinctive combination is trade dress (Ingrid & Isabel v. Baby Be Mine), and the "trade dress database" theory survived dismissal in Andersen.
2. **Competitor assets feed ANALYSIS only** — generation receives abstractions + the user's own inputs. No training/fine-tuning on scraped competitor content. Use foundation-model vendors with output IP indemnities.
3. **Distinctiveness gate shipped as a feature** — auto-reject candidates too close to any studied competitor; display the score. It converts likelihood-of-confusion factors into a shipped control and answers the regression-to-mean critique in the same stroke.
4. **Intent-trail hygiene:** UI copy, prompts, logs, and marketing say "benchmark and differentiate," never "copy/emulate/clone." (In Ingrid & Isabel, one vendor email saying "emulate their look" carried the case past summary judgment.)
5. **Scraping on the Meta v. Bright Data safe pattern:** logged-out public pages only, no paywall/bot-wall circumvention, honest crawler UA, low volume (5–10 pages/job), robots.txt + EU/UK TDM opt-outs respected (country-matching guarantees EU targets), screenshots only inside annotated analytical reports (Kelly/Perfect 10 transformative-use pattern) — never downloadable competitor asset packs. DMCA agent registered.
6. **Logos:** prompt-only AI logos are uncopyrightable (USCO Jan 2025) but trademarkable; UK Getty v. Stability puts output trademark liability on the *platform*. Ship type-lockup wordmarks + mandatory human-editing step with an exportable "authorship record"; screen outputs against studied competitors' marks + USPTO/EUIPO/WIPO; offer trademark-clearance referral as an upsell (a genuine edge over Looka/Canva's "talk to your own attorney").
7. **ToS:** assign customers all rights Brando holds, disclaim uniqueness/non-infringement (the Looka/Canva pattern), require indemnification — then beat the incumbents commercially with the built-in similarity screening they conspicuously lack.
8. **Never surface studied brands as endorsement-adjacent marketing** — naming competitors inside a user's private report is nominative fair use; publishing "brands we can style-match" replicates the false-endorsement claim that stuck to Midjourney.
