# 05 — The Living Page Wedge: "Brando Pulse"

*Round-2 research, July 2026: 6 web-research sweeps (living-page/CRO category history, low-traffic learning signals, ad-creative evolution, GEO-drift evidence, self-learning agent architectures, breakout marketing mechanics), an adversarial review, 3 independently designed wedges, and a judged synthesis. This doc supersedes the retention-hook question left open in doc 02.*

## 1. The question

Can Brando's wedge be a **smart marketing agent with real ongoing utility** — a living landing page (and assets) that evolves with feedback, Hermes-style self-learning — and what marketing angle makes it break out?

## 2. The hard evaluation: the naive version is a graveyard

**The math kills conversion-driven "self-evolving pages" at our market tier.** Detecting a 10–20% relative lift on a 2–3% baseline needs 1,000–2,000+ conversions *per variant* (~60,000 visitors/variant); even Unbounce's bandit needs ~500 visitors and ~50 conversions/month before routing is reliable. Brando's €199–499/mo customer has ~800 visits and 15 conversions a month. Below ~500 conversions/month, "self-learning from your own visitors" is statistical noise with a changelog.

**Everyone who built this for the mid-market is dead or absorbed:**
- **Intellimize** (category creator, 2016) — couldn't survive standalone; absorbed by Webflow (2024), now a $299+/mo add-on locked to Webflow hosting.
- **Mutiny** (best-funded, Sequoia) — publicly **killed its personalization SaaS in April 2026**; the CEO's stated reason: the model "put the execution burden on humans" and no injected AI could fix it. Relaunched as an agent generating assets from *CRM data* (a non-traffic signal).
- **Coframe** (the "living UI" originator) — alive and growing, but ~$2.5M ARR after 3 years despite Khosla money and Replit/Dropbox logos, had to acquire a GTM company and go enterprise sales-led. The loop only pencils out where hourly Bayesian updates have traffic to chew on.
- **Icon.com** ("AI CMO") — bankrupt March 2026 after fabricated-growth hype. **Sentient Ascend** — divested; heir Evolv AI shrank to ~24 heads.

**Ads are worse:** Meta's Andromeda/Advantage+ ($10B AI-creative run-rate; Zuckerberg's stated end-2026 goal: "connect your bank account, no creative, no targeting needed"), Google PMax, and TikTok Symphony absorbed both generation and optimization with per-impression feedback no third party gets. AdCreative.ai exited at ~1–3x revenue; Pencil absorbed; Omneky crowdfunding. At $10–50/day an SMB gets 2–10 conversions/week — a weekly ad-evolution loop is mathematically fake. **Do not build the wedge on ads.**

**"Self-learning like Hermes" needs honest framing.** Hermes (Nous Research's Hermes Agent, Feb 2026, ~209k GitHub stars) does NOT do online learning — it's frozen weights + self-authored skill files + FTS5 cross-session memory + offline RL. That file/memory loop is exactly what's credible in production; true online learning in marketing products is theater (Gartner: >40% of agentic projects predicted cancelled by 2027; 88% of orgs deploying agents reported an incident in 2025). The honest architecture: **persistent brand memory + pooled priors + eval gates + human-approved diffs.**

## 3. The inversion that survives: swap the fitness function

All three wedge designs and the devil's advocate converged on one insight:

> **The page shouldn't learn from its visitors (it has none). It should learn from the AI engines (which can be probed at zero traffic).**

The evolution signal is **AI-recommendation share**, measured by AnswerMonk's multi-engine panel. This is:

- **Traffic-independent** — you can probe ChatGPT/Perplexity/Gemini/AI Overviews weekly whether the page has 0 or 100k visits. The statistical wall that killed Intellimize/Mutiny-class loops simply doesn't apply.
- **Evidenced on both sides.** The *problem* recurs: 40–60% of citations drift monthly (Profound: AI Overviews 59.3%, ChatGPT 54.1%); >99% of repeated runs return a different brand list; BrightEdge: #1–2 positions are cemented (0.6% movement) while challenger positions churn with **87% of changes being declines** — *a static page is a melting asset*. The *fix* works: refreshing stale pages drove +219–300% AI visits (Seer); ~76% of ChatGPT's top-cited pages were updated within 30 days; Perplexity weights freshness ~3.3x with 2–4 week feedback loops.
- **Near-free for us, expensive for everyone else.** Credible measurement demands stratified panels (30–50 intent-typed prompts × 10–30 runs × 4 engines, confidence intervals, change-point stats, 2–6 week rolling windows — never single-run reads). That's AnswerMonk's existing pipeline at ~zero marginal cost; competitors resell weaker single-shot versions at $99–500/mo, and naive entrants will ship visibly unstable dashboards. **The volatility is the moat.**
- **Unoccupied.** Continuous-action GEO agents (Profound Agents, Relixir, Athena, Goodie) mutate *blog content* into CMSs; Scrunch/Adobe serve *cloaked edge variants* (penalty-risk-adjacent); Coframe/Fibr need traffic. **Nobody evolves the brand layer — copy, positioning, structure, DESIGN.md, tokens — on the canonical page, with client-facing evidence.** Fibr already ships "LLM-to-Web"; Webflow's Chief Evangelist (the ex-Intellimize CEO) is publicly evangelizing AEO. Window: 12–18 months.

## 4. The one unproven link: the actuator — GATE EVERYTHING ON IT

The devil's advocate's sharpest surviving objection: **every documented case of page changes moving AI citations is blog/informational content. Nobody has shown that changing a landing page's brand presentation moves recommendation share.** We might build a steering wheel not connected to the wheels.

So the sequencing rule is absolute: **run the actuator experiment BEFORE building any automation** (weeks 0–8, Wizard-of-Oz, ~founder time + €1–2k):

- 10–15 real low-traffic pages (2–3 own properties + design partners via 2–3 friendly agencies).
- Manually run the full loop: weekly stratified panels → one evidence-backed Evolution PR → agency approval → deploy to canonical page → re-measure.
- **Pass:** brand-layer page changes move consideration-set membership/share-of-voice beyond the 40–60% baseline churn on ≥1 retrieval-backed engine within 4–6 weeks on ≥50% of pages; AND ≥60% of PRs approved without substantial rework (the Mutiny execution-burden check); AND ≥3 agencies convert to paid white-label.
- **Kill:** actuator moves <1/3 of pages → the honest product is teardown + monitoring; revert to the doc-02 plan and abandon the living-page framing. Approval <30% → the ritual is friction; ship quarterly refresh sprints instead.
- **If it passes, the published experiment series IS the launch asset** ("we changed 15 real brand pages; here's exactly what moved AI recommendations — and what didn't"). Publishing the losses is the trust weapon in the post-Icon/Cluely climate.

## 5. The product: Brando Pulse

**Positioning:** *the agency white-label "AI-Visibility Retainer" with an actuator* — the round-1 teardown as onboarding, a living page as the subscription.

**Exact problem statement (the customer's words):**
> "When buyers ask ChatGPT, Perplexity or Google's AI for the best [category] in [country], my client isn't in the answer — and the brands that are keep updating their pages while my client's sits frozen. I can't A/B test my way out: every CRO tool silently assumes 60,000 visitors per variant and my client has 800 a month. I sold them an audit six months ago; I have nothing recurring to sell, and nothing I can show each month that proves we're winning somewhere that matters."

**Day-one box (real utility before any evolution):** the doc-02 audit — segment's AI-recommended leaders torn down with screenshots/evidence; 3 differentiated brand directions as machine-usable design language (DESIGN.md, DTCG tokens, shadcn theme, voice rules, AEO kit); the chosen direction applied to the canonical page (answer-first blocks, comparison module, JSON-LD, agent-readable offers); baseline AI-visibility panel with confidence intervals + agent-readiness score; the Ledger initialized.

**The ongoing loop — weekly MEASURE, monthly ACT** (the cadence split is structural: it fixes attribution honesty — one change per 2–6-week window — and kills the Mutiny execution burden at 1 PR/client/month, not 4):

1. **Weekly Pulse (read-only ritual):** panel deltas with CIs, competitor-drift alerts (puppeteer diffs of the ~10 engine-recommended leaders, cross-referenced against who *gained* share), agent-readiness probes, what-moved-and-why. Retrieval-backed surfaces only (Perplexity, ChatGPT search, AI Mode); parametric answers explicitly excluded from claims.
2. **Monthly Evolution PR (one per client):** agent drafts ONE evidence-backed diff — copy blocks, comparison tables, schema, offer framing, tokens — ranked by pooled category priors + per-brand memory → automated eval gates (DTCG/DESIGN.md brand-compliance, drift audit vs approved direction, regression, one-click rollback) → **human approval gate (the product, not friction** — every surviving player kept it) → deploy to the **canonical page** (no cloaked AI-only variants — a positioning weapon vs Scrunch/Adobe) → subsequent panels score it → outcome written to per-brand Hermes-pattern memory files + pooled category priors (bootstrapped from teardowns, drift data, and engine rankings — no customer traffic needed, which defuses the Unbounce cold-start problem).
3. **Calibration extras:** monthly freshness heartbeat; trickle telemetry (Clarity, GSC CTR) reported honestly at small n; optional customer-funded €150–300 quarterly ad micro-burst as conversion ground truth (never CTR — it correlates −0.28 with sales); LLM persona simulation used strictly as a calibrated *ranking* layer, never as proof.

**Never say "self-learning."** The claim: *"a closed measure→act→re-measure loop with persistent brand memory, human-approved, with receipts."* Guardrails are marketable ("evolution without erosion").

**Explicitly NOT in the box:** conversion-lift claims (unfalsifiable at this tier = churn machine), autonomous unreviewed changes, ad generation (platform-absorbed; ship only a thin on-brand ad-asset export kit + a Meta/Google "AI settings guardrail checklist" later), cloaked variants, always-on bandits (a traffic-gated A/B add-on only for verified ≥500-conversions/mo accounts, months 6–12).

**Pricing:** €490 one-off teardown (creditable against month one — the acquisition funnel) → €199/mo Brand (1 page: weekly pulse + monthly Evolution PR + freshness + Ledger) → €399/mo Growth (deep competitor drift, agent-readiness, micro-burst orchestration) → **€990/mo Agency white-label for 5 client pages, then €149–179/page** — agencies resell as a €500–1,500/mo/client "AI-Visibility Retainer" at 60–80% margin. Sits exactly in the validated $250–500 action-tier band, undercuts $2k–5k enterprise GEO loops, matches AnswerMonk's proven €199–499 tolerance. Churn resistance lives in the *agency's* retainer economics, not our dashboard.

## 6. The breakout marketing angle

The 2024–26 evidence says market-breakers used three durable mechanics — a self-replicating public artifact (Lovable badge+remix: ~$200M ARR in ~12 months; Calendly: ~25% of signups from the badge), a competitive public scoreboard (HubSpot Website Grader: 4M sites, 40k backlinks; Profound's Index), and watch-the-agent-work evidence content (Devin demo; Clay growing 10x YoY on practitioner word of mouth). Hype-first died on the record (Icon bankrupt, Cluely admitted fabricated ARR; 54% AI fatigue; "slop" as word of the year). Static graders are commoditized — **the longitudinal version is unclaimed.**

**Positioning line:**
> **"CRO tools need 60,000 visitors to learn one thing. Your page has 600. Brando's living page learns from the AI engines instead — the first landing page with a fitness function that works at zero traffic. Static pages melt (87% of AI-citation changes are declines); ours evolves monthly, with receipts."**

Attack line: *"Anyone selling always-on optimization to a low-traffic site is selling statistical noise — here's the math."* Anti-slop stance explicit: *"an agent that makes your page LESS generic, with receipts"* — the anti-Icon.

**Launch assets, in order:**
1. **The published actuator experiment series** (weeks 0–8 output): "We changed 15 real brand pages and here's exactly what moved AI recommendations — and what didn't." Publishes losses → the most credible artifact in the 2026 climate, and it seeds public time-series with visible slope before launch.
2. **The AnswerMonk-corpus data study** for press (the Profound playbook): "We probed N segments × 4 engines for 8 weeks: X% of funded startups never appear in any AI answer; 87% of citation movement is decline."
3. **Longitudinal public segment leaderboards** — "brands AI engines actually recommend in [category]/[country], updated weekly, with movement arrows." *Claim your brand* IS the lead capture (the modern grader, longitudinal from day one); losing brands are a self-refreshing outbound list. The leaderboard pages are themselves AEO-optimized by the product — when engines cite Brando's own pages for "best X in [country]", **the marketing channel is the product proof; publicize the recursion.**
4. **The Living Page Ledger + badge:** a permanent public URL per opted-in site — week-by-week visual diffs, the agent's reasoning per change with evidence, and the AI-recommendation-share time series — with an "Evolving with Brando · v37 · improved 2d ago" badge linking back (Lovable/Calendly mechanic). **Public ledgers are founder-tier sourced; agency client ledgers are private/white-label by default** (resolves the confidentiality conflict). Design rule: publish movement, never static scores.
5. **Agencies run the Clay playbook, not the HubSpot playbook:** certify "AI-Visibility Engineers," white-label portfolio ledgers, market the agencies themselves.

**Controversy budget:** spent only on reproducible TRUE findings ("the market leader in [segment] is invisible to every AI engine — probe attached") — Cluely-grade engagement with HubSpot-grade trust. Every public claim links to a reproducible probe + methodology; takedown/verification policy from day one.

**Honest expectation:** badge K-factors run 0.1–0.3 and leaderboard SEO compounds over quarters — the *revenue* thesis rides agency sales; the public artifacts carry the *attention* thesis.

## 7. Roadmap

| Phase | Weeks/months | Work | Gate |
|---|---|---|---|
| **0. Actuator gate** | Weeks 0–8 | Wizard-of-Oz loop on 10–15 real pages; real panels, manual PRs, agency approvals; nothing irreversible built | Pass/kill criteria in §4 |
| **1. Launch** | Weeks 8–14 | Publish experiment series + data study; 20–50 segment×country leaderboards + claim-your-brand funnel; €490 teardown as entry SKU; subscription beta with 5–10 agencies; Evolution-PR pipeline + approval UI; badge loop on | ≥10 paying pages or 3 white-label agencies |
| **2. Agency engine** | Months 4–6 | White-label portal (portfolio view, client-facing ledgers, margin pricing); pooled category priors v1 feeding PR ranking; agent-readiness GA; micro-burst add-on; certification track | Reorder/renewal ≥70% at month 3 |
| **3. Compound** | Months 6–12 | Programmatic leaderboards across hundreds of segments; per-brand memory demonstrably improving PR win-rate; MCP/API so Lovable/v0/Claude Code ingest the *living* DESIGN.md; traffic-gated A/B add-on for ≥500-conv/mo accounts only; thin ad-asset export kit | — |

## 8. How this reconciles with docs 01–04

This is the round-1 plan's **second act, not a replacement**. The 7/10 white-label audit stays as the entry product and acquisition funnel; Pulse converts it from episodic to recurring — directly fixing round-1's #1 flagged weakness. Generation remains non-defensible exactly as round-1 concluded; every moat layer is measurement-side: the closed AnswerMonk loop, volatility-as-moat statistics, per-brand memory + pooled priors bootstrapped without customer traffic, leaderboard authority, agency distribution lock-in. Legal architecture (doc 03 §6) applies unchanged; honest-AEO rules apply doubly, since the weekly ritual now *is* the product.

**Honest ceiling (state it, staff it, fund it accordingly):** a €1–5M ARR agency-tooling business that makes Brando non-episodic and hardens AnswerMonk retention — a strong wedge with a real option on the category **if the actuator experiments become the industry's reference dataset**. Not a guaranteed market-breaker; the market-breaking scenario runs through the leaderboard becoming the LMArena of brand visibility.

## 9. Round-2 evidence quick-reference

| Claim | Evidence |
|---|---|
| CRO math wall | 1,000–2,000 conversions/variant for 10–20% lift; ~60k visitors/variant for 2%→2.2%; Unbounce bandit needs ~500 visits + 50 conv/mo; 16 weeks to detect a 50% lift at 500 weekly users |
| Mid-market graveyard | Intellimize→Webflow $299 add-on (2024); Mutiny killed personalization SaaS (Apr 2026, "execution burden on humans"); Coframe ~$2.5M ARR after 3 yrs, went enterprise; Sentient Ascend divested; Icon bankrupt (Mar 2026) |
| Citation volatility | Profound: 40–60% monthly drift; SE Ranking: 9.2% URL overlap on same-day reruns; SparkToro: >99% of reruns differ; external signals explain <20% of ChatGPT recommendation variance |
| Updates move citations | Seer: +219–300% AI visits from refreshes; ~76% of ChatGPT top-cited pages updated within 30 days; Perplexity freshness weight ~3.3x, 2–4 wk loops |
| Decay urgency | BrightEdge: #1–2 positions move 0.6%; 87% of citation changes are declines |
| Action-tier pricing | Profound Agents $399/mo, Athena $295, Goodie $495, Relixir, Writesonic $249+; tracking commoditized at ~$99 |
| Ads absorbed | Meta AI-creative $10B run-rate; Advantage+ default-on (+22% ROAS claim); AdCreative.ai sold ~$38.7M on €10–50M revenue; Arcads/Creatify healthy only on cost-collapse, not evolution |
| Hermes reality | Nous Hermes Agent (Feb 2026, ~209k stars): skill files + FTS5 memory on frozen weights; offline RL; no production online learning |
| Breakout mechanics | Lovable badge/remix ~$200M ARR/12mo; Calendly ~25% signups from badge; HubSpot Grader 4M sites/40k backlinks; Clay 10x YoY on word of mouth; Icon/Cluely = cautionary |
