# 04 — Research Appendix

*July 2026. Evidence base behind docs 01–03: 8 parallel research sweeps (~40 tools verified on their own sites), 1 adversarial review, 3 independently designed wedges, 1 judging pass.*

## A. Brand generators & brand-intelligence tools

| Tool | Pricing | What it does | Gap vs Brando |
|---|---|---|---|
| Looka | $20/$65 one-time; $96–129/yr Brand Kit | Questionnaire → logo + 300+ templates + guidelines + AI site | No competitor analysis; assets not systems; "templated" reputation |
| Brandmark | $25/$65/$175 one-time | Logo + style guide + social kit; chat UI at chat.brandmark.io | Same; chat input is table stakes |
| Tailor Brands | from $3.99/mo | Logo + site + LLC formation bundle; 30M+ businesses claimed | Volume/low-price game; subscription-billing backlash |
| LogoAI | $29/$59/$99 one-time | Full kit in <10 min; 8.0/10 in Apr 2026 testing | Closest asset-level comp at $99; zero strategy |
| Canva Brand Kit + Magic Studio | ~$15/mo Pro | Brand-aware generation via Canva Design Model; MCP puts Brand Kits inside ChatGPT | A container/applier, not a creator; keeps users in Canva. Main absorption threat (12–18 mo) |
| uBrand | $29/mo Pro; **$149/mo Agency** | End-to-end AI branding, multi-client agency tier | Proves agencies pay monthly for client-brand tooling |
| Lovart | ~$43–90/mo | "AI design agent," 40 assets/prompt, 800k beta users | Wins raw generation — reason generation can't be Brando's moat |
| Branding5 | subs + AppSumo LTDs | Competitor analysis (100+ points) → brand strategy reports | Text only; complaints: "generic AI tone," forced single-direction pre-payment |
| IdeaProof | freemium | Archetype/UVP/voice for pre-launch | Strategy text only |
| Inspo AI | $12–39/mo; $199 lifetime | Brand Scanner: full brand DNA from any URL; moodboards; 150k references | User-picked competitors; extracts, never synthesizes. **Fast-follow threat #1** |
| Ad Legends Visual DNA | free–$399/mo | Extracts complete brand identity from a URL (OKLCH, type scales) | Single-URL extraction only |
| aibrandkits.com | **$9 lifetime** | DESIGN.md + tokens.json + css-variables + agent prompts for Cursor/Claude Code/v0/Lovable | Validates Brando's output format — and sets its price floor. No research, no voice depth |
| Competely | $9–99/mo | Sourced 100+ data-point competitor comparisons incl. taglines/UVP/messaging; ~300 paying customers | Zero visual/design output. **Fast-follow threat #2** |
| Osum | $150–2,500/mo | Instant SWOT/personas from a URL | Proves WTP for automated competitive research |
| Crayon / Klue / Kompyte | $16k–100k+/yr | Enterprise CI monitoring | Different buyer + JTBD — do not compete here |
| Relume | $18–58/user/mo | Sitemap → wireframe → Style Guide; Figma/Webflow/React export; **$1.8M ARR bootstrapped, 1M+ users** | No competitor grounding. Proves agency time-compression revenue. **Fast-follow threat #3** |
| brand.ai | enterprise | 150-dimension machine-readable "Brand Foundation" | Where the "brand-as-data" market is heading; enterprise-only |
| Mobbin / Land-book / Landingfolio / Refero | ~$10–12/mo | Screenshot galleries for manual best-of-crop research | The manual workflow Brando automates |
| Foreplay Spyder / MagicBrief | $49–175/mo | Auto-captures competitors' ads, hooks, landing pages | Proves agencies pay monthly for automated competitive creative-watching |
| Brandfetch | free tier; usage-based | API: any domain → logos, colors, fonts, tokens | Commodity plumbing — buy, don't build |
| Ocean.io / Clay / Similarweb / Semrush | credit/subscription | Country/industry-filtered lookalike discovery | Commodity plumbing for Step 1 |

## B. AI site builders (the ingestion targets)

| Tool | Scale/pricing | Brand-input channel | Note |
|---|---|---|---|
| Lovable | ~$400–500M ARR, $6.6B val, 8M+ users; from ~$25/mo | Knowledge file (all plans); Design Systems (Enterprise-only); MCP connectors | SSR only for post-Apr-2026 projects — older output invisible to AI crawlers |
| v0 (Vercel) | $20–100/user/mo | **Design Systems 2.0**: globals.css, Tailwind config, shadcn registry import | Most formalized brand-input architecture |
| Bolt.new | $40M ARR in ~5 mo, 5M+ users | Figma import (Jan 2026) | |
| Framer | $2B val, 500k+ MAU | Wireframer + brand assets | 40% of a recent YC batch launched on it |
| Figma Make | bundled in seats | **Make kits** package a design system as AI context; native DTCG import | |
| Wix ASG 2.0 | $17–159/mo | Accepts **rival-site URLs as inspiration** (vibes only); auto-llms.txt globally since May 2026 | Closest to competitor-informed input; shallow |
| Webflow | $14–39/mo + AEO (Apr 2026, enterprise-only) | On-brand within your existing site | Proves closed-loop AEO demand |
| Durable / Mixo / 10Web | $7–95/mo | None — generic output | The "slop" the backlash targets |
| Relume | $18–58/mo | Style Guide export to Figma/Webflow | |
| Flint | free; **$96/mo Starter, $400/mo Pro**; customers LangChain/11x/Graphite | Brand extraction from your own URL → GEO-built landing pages; MCP into Claude | **Reference competitor** for the landing-page half; no competitor research, no measurement loop |

## C. Output-format landscape (the format war is settled)

- **DESIGN.md** — Google Labs open-sourced (2026, alpha, npm CLI): YAML front-matter tokens + prose; consumed by Claude Code, Cursor, Lovable Knowledge, v0, Stitch, Copilot. **The canonical deliverable.**
- **DTCG v2025.10** (Oct 2025, first stable) — OKLCH, groups/aliases, theming; Style Dictionary v5; Tokens Studio defaults to it; Figma rolling out native import/export. **The professional interchange layer.**
- **shadcn registry-item.json / globals.css OKLCH + Tailwind v4 @theme** — the paste-in theme economy; tweakcn (9.8k stars) is the de facto free generator.
- **Figma Variables REST API write = Enterprise-only** (Tier-3 endpoint). Plugin API works on all paid plans (4-mode limit below Enterprise). Figma MCP write-to-canvas beta: Full seats, will become usage-priced. html.to.design converts any URL to editable Figma layers (back-door import).
- **Voice-as-constraints pattern** (2025–26 consensus): tone sliders, always/never lexicon, golden samples/anti-samples per section — quantified rules, not adjectives. No product bundles this with visual tokens. **Whitespace.**
- Agencies now report clients briefing for "an identity, a token set, a component library, and a brief written for agents" instead of PDF guidelines.

## D. AEO/GEO evidence base

| Finding | Source | Implication |
|---|---|---|
| Citations/statistics/quotations/fluency lift AI citation visibility 30–41%; keyword stuffing useless | Princeton/KDD GEO paper (Aggarwal et al., 2024), 10k queries | Bake into copy engine as rules |
| **97% of llms.txt files receive zero AI-bot requests**; Google/OpenAI don't support it | Ahrefs server-log study, 137k domains, June 2026 | Generate it, never lead with it |
| **No major AI crawler executes JavaScript** (zero evidence in 500M+ GPTBot fetches) | Vercel analysis, June 2026 | SSR is the single most decisive page-level factor; default Lovable/v0 CSR output is invisible |
| Schema: +44% AI citations (BrightEdge), 3.2x (73-site study) — but mainly Google AI Overviews/Bing | vendor studies + SSRN cross-platform | Ship JSON-LD; scope the claim |
| Reddit ≈40% of AI citations; own site ~12%; G2/Capterra ≈0; top 15 domains hold ~68% of citation share; volatile (Reddit 60%→10% in 6 weeks) | Derivatex 2026 (233 recs), 5W/Lantern/Ahrefs meta-analyses (680M citations) | On-page is necessary-not-sufficient; ship off-page checklist → AnswerMonk |
| AI referrals ≈1% of B2B traffic but ~4x conversion (Seer: ChatGPT ~15.9%) | Seer et al. | Sell AEO as conversion insurance, not traffic growth |
| GEO market: Profound $1B val ($99–399/mo+), Peec >$10M ARR (€199/mo), Goodie $295–495/mo, Otterly $29–489/mo, Scrunch AXP, Athena | funding/pricing pages | Nobody generates brand assets; trackers moving toward "agentic actions" — window is open but closing |
| GEO services: $1.5k–5k audits, $3k–15k/mo retainers; 94% of CMOs increasing AI-search spend | 2026 pricing surveys | The AEO annex is monetizable substance |

## E. Demand signals & willingness to pay

| Signal | Numbers |
|---|---|
| Roast My Landing Page | $350/roast, ~$20k/mo, 800+ founders — one person, manual |
| Roast market | Roastd $179, MakerBox $149; free AI roasts commoditizing the low end (45k+ sites) |
| Fiverr brand identity | $800–2,010 (40–60h of work); 99designs mid-tier similar; Upwork to $5k |
| Freelance landing pages | ~$350 avg Fiverr; $500–3,000 typical |
| Competitive brand audits | $2k–10k freelance (competitive analysis priced as add-on); $5k–15k boutique; $25k–50k+ enterprise; £20–30k UK high end |
| Agency pitch prep | 6–8 unbillable hours per client, reducible to ~45 min with AI; agency tooling $50–500/mo/seat |
| Slop backlash | Catalogued patterns: 34% dark themes, 27% gradients, 22% icon-card grids; tweakcn 9.8k stars; "Copy Prompt for v0/Bolt/Lovable" now a standard feature |
| PH validation | X-Design branding agent #1 PotD (Dec 2025); Competely 303 upvotes → ~300 paying |
| Pricing sentiment | Looka's $65 one-time = most-praised SKU; Tailor Brands' subscription-first = complaint magnet; IH favors per-report for episodic jobs |
| **Gap** | No verbatim "I want this product" quotes retrievable (Reddit/IH block scraping) — manual thread-mining + 10–20 interviews required |

## F. Agent-distribution evidence

- **MCP scale:** donated to Linux Foundation Dec 2025; ~9,650 servers in the official registry (LobeHub indexes 56k+); 67M server downloads in April 2026; **usage concentrates in the top ~50 servers**.
- **Precedents in Brando's category:** Context7 (240k weekly npm downloads — docs-as-context for coding agents), 21st.dev Magic (`/ui` → generated components inside Cursor), Canva AI Connector (Brand Kits inside ChatGPT's 800M users), Exa/Firecrawl (API-first, MCP-distributed).
- **ChatGPT Apps SDK is built on MCP** (one server = ChatGPT app + Claude connector + Cursor tool). GPT Store / killed plugins = the cautionary precedent for in-chat discovery.
- **Being recommended is won off-site:** vendor's own site cited 11.6% of the time; 4+ independent source mentions = 2.8x citation lift; year-stamped comparison listicles + Reddit dominate. G2/Capterra: ~zero AI citations.
- **Skills:** SKILL.md cross-vendor standard (Dec 2025), ~40 products consume it — cheapest artifact.
- **Agent-payable rails:** x402 — ~$50M volume, 165M transactions, 69k active agents by Apr 2026; Stripe MPP for fiat.
- **Tool descriptions are the new SEO:** agents choose tools by name/description alone (arXiv 2602.14878).
- llms.txt exception: AI IDEs *do* read it on developer-tool docs domains — the one place it works.

## G. Legal foundations

| Authority | Holding | Design consequence |
|---|---|---|
| Ingrid & Isabel v. Baby Be Mine (N.D. Cal. 2014); Blue Nile v. Ice.com | Website look-and-feel = protectable trade dress; a vendor email saying "emulate their look" carried intent | Aggregation-only; intent-trail hygiene everywhere |
| Andersen v. Stability/Midjourney — **trial Sept 8, 2026** | "Trade dress database" theory survived dismissal | No named-brand style-matching, ever; ship before/around the trial with clean architecture |
| Getty v. Stability (UK High Court, Nov 4, 2025) | Output-level **trademark liability on the platform**, not the user | Build mark-similarity screening; can't outsource to ToS |
| USCO Part 2 (Jan 29, 2025) | Prompt-only outputs not copyrightable; trademarkable though | Human-edit step + authorship record for logos |
| USCO Part 3 (May 9, 2025) | Training on scraped works for competing expressive output = worst fair-use pattern | Never train/fine-tune on competitor content |
| hiQ v. LinkedIn; **Meta v. Bright Data (Jan 2024)** | Logged-out scraping of public pages ≠ CFAA violation / ToS breach | Logged-out only, no bot-wall circumvention, honest UA |
| Kelly v. Arriba Soft; Perfect 10 v. Amazon | Images inside analytical/indexing use = transformative fair use | Screenshots only inside annotated reports |
| Reddit v. Anthropic (2025); EU TDM/AI Act opt-outs | robots.txt/opt-out respect is now table stakes; binding in EU/UK | Respect opt-outs; country-matching guarantees EU targets |
| Looka/Canva ToS pattern | Disclaim uniqueness/non-infringement; push risk to user; Canva: template logos not trademarkable | Copy the shield, beat it with built-in screening + clearance referral |

## H. Method

Eight parallel research agents (brand generators, site builders, teardown tools, output formats, AEO evidence, demand signals, agent distribution, legal), each running independent web searches with source verification; findings digested and handed to one adversarial reviewer instructed to refute the product, and three wedge designers with different lenses (founder-DIY, agency-leverage, agent-first); a judge scored the wedges against the risk register on demand evidence, speed to falsifiable test, defensibility, AnswerMonk fit, and distribution realism. The judge's hybrid recommendation and the devil's advocate's "survivable path" converged independently on the same plan — the strongest internal-consistency signal in the exercise.
