# 02 — Wedge & Go-to-Market

Three wedges were designed independently (different lenses), stress-tested against an adversarial risk review, and scored by a judge on demand evidence, speed to falsifiable test, defensibility, AnswerMonk fit, and distribution realism.

## 1. The three wedges, scored

### 🥇 Wedge A — "Brando Pitch Kit" (agency leverage) — **7/10, primary bet**

> Turn the 6–8 unbillable hours of competitor research an agency burns before every pitch into a 15-minute, **white-label competitive brand audit** with screenshots, evidence, and 3 client-approvable brand directions — exported as files Lovable, v0, Claude Code, and Figma actually consume.

- **ICP:** solo brand/web designers and 2–15-person studios (Webflow/Framer/Relume/Lovable stack) selling $2k–15k brand + landing projects to B2B SaaS and service SMBs; fractional CMOs juggling 3–8 clients. **Beachhead: agencies already inside AnswerMonk's customer base.**
- **Why it won:** the only wedge where the job is *already a paid line item* (audits bill $2k–15k; pitch-prep tools at $12–149/mo; Relume's $1.8M ARR precedent). It is also the most insulated from the "regression to the mean" kill shot — the core purchase is the Step 1–2 **evidence artifact** (pitch ammunition), valuable even when the 3 generated directions are only client-approvable drafts. Same buyer as AnswerMonk's €199–499/mo GEO customers → direct cross-sell. Agencies pitch monthly → per-report becomes workflow revenue, not once-per-company.
- **Honest weaknesses:** white-label quality bar is one-shot (a "generic AI tone" report in a client meeting kills the account); one wrong competitor set destroys trust; positioning must read as *margin expansion*, never as automating away their billable; LTV plateaus in low hundreds/account without the monitoring hook.

### 🥈 Wedge B — "Anti-Slop Brand Pack" (founder DIY) — **5.5/10, sequenced second**

> Free **Slop Score** roast (your page scored against the top 5 brands in your segment + AI-visibility teaser) → **$99 one-time brand pack**: competitor teardown + 3 evidence-backed directions you paste straight into Lovable/v0/Claude Code.

- **ICP:** solo technical founders, pre-launch to ~$10k MRR, building in Lovable/v0/Bolt/Claude Code; no designer; acute self-diagnosed pain ("my site looks like every other purple-gradient Lovable page").
- **Why second, not first:** fastest/cheapest test and the Slop Score is a genuinely great asset regardless — but the buyer is the segment least able to pay, anchored at $9–65 by aibrandkits' $9-lifetime and free tweakcn/DESIGN.md; all demand evidence is for the free roast, none for the paid pack; a GEO-literate indie audience will A/B the pack against "just prompt Claude" within minutes and roast failures publicly.
- **Keep from day one anyway:** the free Slop Score as universal top-of-funnel for BOTH ICPs — it matches proven roast demand ($350 human roasts; $20k/mo RoastMyLandingPage), AnswerMonk's scoring DNA, and produces shareable cards + a lead list.

### 🥉 Wedge C — "Brando MCP" (agent-first) — **4.5/10, distribution channel, never the product**

> One MCP tool call — `generate_brand_pack(url|description, country?, business_model?)` — that Claude Code, Cursor, Lovable, or v0 invokes at project-scaffold time, returning DESIGN.md + DTCG tokens + shadcn globals.css + voice rules + entity/AEO kit written into the project.

- **Why it exists:** the scaffold moment inside coding agents IS the right invocation point; one remote MCP server now reaches Claude/ChatGPT-Apps/Cursor/Lovable simultaneously; Context7 (240k weekly downloads) proves agents call third-party context tools mid-task; a SKILL.md costs days to ship.
- **Why it's not the wedge:** zero evidence of *paid* conversion via this channel; MCP usage concentrates in the top ~50 of 9,650+ servers; installed ≠ invoked; the model improvising a generic Tailwind theme is a free in-context substitute; default-pick placement is gatekept by partner programs Brando must win against Canva-class players. Ship it cheap, instrument it, expect nothing.

## 2. The sequenced hybrid plan (recommended)

Framed explicitly as **AnswerMonk's second product line** — shared infra, shared customers, shared credibility.

| Phase | Action | Cost | Purpose |
|---|---|---|---|
| **Weeks 1–2** | Ship the free **Slop Score** roast (AnswerMonk crawler + LLM scoring + shareable card). Do NOT build the $99 founder SKU yet | Days | Universal top-of-funnel, lead capture for both ICPs, viral asset |
| **Weeks 1–4 (parallel)** | **Wizard-of-Oz agency test**: one-page offer — *"White-label competitive brand audit + 3 brand directions for your client, delivered in 48h — $149 intro, first 15 slots"* — Stripe link, fulfilled manually with the AnswerMonk pipeline + Claude + a report template. Sell to AnswerMonk's agency customers + 100 cold-DM'd studios/fractional CMOs (free 1-competitor teaser teardown as the door-opener) | ~Zero build | The primary monetization bet, validated with dollars |
| **Month 2–3 (conditional)** | If the agency bar clears → productize the report pipeline (see doc 03), launch **$99 self-serve founder pack** downmarket reusing the same pipeline; Slop Score conversion data collected since week 1 tells you if that market pays | 2–4 wks build | Second SKU on a validated pipeline |
| **Month 3+ (always)** | Ship **SKILL.md + thin remote MCP server** exposing the already-validated pack; list on MCP Registry/PulseMCP/Smithery/LobeHub; apply to Lovable's integration partner program; publish the "AnswerMonk-on-Brando" GEO case study | Days–2 wks | Hedge the agent-era channel; costs little, loses nothing |

**Success / kill criteria (falsifiable, dated):**

- **Agency test (14 days):** ≥10 paid orders ($1,500 collected) AND ≥3 of the first 10 buyers reorder or ask about a subscription within 30 days — the *reorder* is the real signal that this is a workflow tool. Secondary: count buyers who'd put the report in front of a client unedited (white-label trust threshold). **Kill:** <5 paid orders from 100+ qualified touches.
- **Slop Score → founder pack (when launched, 14 days):** ≥20 paid packs, ≥4% score-to-checkout conversion, ≥30% of buyers actually paste the pack into a builder within a week (tracked via copy-prompt clicks + follow-up). **Kill:** <8 sales, or people love the roast but won't pay (then the roast is AnswerMonk marketing and paid Brando founder SKU is shelved).
- **MCP (14 days after listing):** ≥300 installs, ≥100 free generations, ≥30% exporting files into a real project, ≥10 paid unlocks with ≥3 via in-agent invocation. **Kill/read:** installs high but invocations ~0 → long-tail trap, go Lovable-partner-first; invocations high but zero paid → price/packaging, not channel.
- **Global kill discipline:** if the agency test fails AND Slop-Score-to-paid <~2%, keep the free roast as AnswerMonk marketing and shelve paid Brando entirely.
- **Pre-launch validation gap to close (runs alongside):** manually mine 20+ verbatim "my Lovable site looks generic" / "roast my landing page" threads and run 10–20 problem interviews (agency owners on white-label appetite; founders on pack pricing). All current demand evidence is proxy-based.

## 3. Target market

| Priority | Segment | Why | Explicitly NOT |
|---|---|---|---|
| 1 | Agencies, studios (2–15p), freelance brand/web designers, fractional CMOs — starting with AnswerMonk's existing agency-flavored customers | Job is a billed line item; monthly pitch cadence = repeat purchase; white-label report self-distributes; warm list exists today | Enterprise PMM/CI (Crayon/Klue territory, $15k–100k, different JTBD) |
| 2 | Solo technical founders / indie hackers building with Lovable, v0, Bolt, Claude Code (US/EU B2B SaaS + services) | Acute slop pain, reachable watering holes, viral before/after format; converts to AnswerMonk monitoring | Micro-SMB "get me a logo for $20" (Tailor Brands/Looka volume game — reputationally damaged, price-anchored) |
| 3 (channel) | AI builders themselves (Lovable/v0-class) via partner integrations; agents via MCP/skills | Default-pick dynamics (Supabase-in-Lovable) are the endgame if the product proves out | Betting the funnel on GPT-Store-style in-chat discovery |

**Geo note:** country-matched competitor panels are a genuine differentiator (a UAE home-healthcare brand and a UK one have different "best of crop") and AnswerMonk's geographic-precision DNA covers exactly this. Non-US/UK markets (UAE, India, SEA) are underserved by every US-centric incumbent — a natural early niche, and one the founder's existing customer base already tilts toward.

## 4. Pricing (anchored to services, not software)

| SKU | Price | Anchor logic |
|---|---|---|
| Slop Score roast | Free | Top-of-funnel; shareable; feeds both ICPs and AnswerMonk |
| Founder brand pack | $99 one-time ($79 founding cohort) | Undercuts $350 human roasts, $800–2,010 Fiverr identity packages, $2k+ audits; deliberately above the $20–65 logo-maker anchor and $9–39/mo inspiration bracket. All 3 directions previewed low-res BEFORE the paywall (fixes Branding5's #1 complaint) |
| Pay-as-you-go report (agency, branded) | $99/report | Entry into the workflow |
| Studio | $199/mo — 5 reports, white-label, all export formats, client workspaces | Sits in the validated $99–399/mo corridor (Flint $96–400/mo, uBrand Agency $149/mo); "Made with Brando" removal is the white-label paywall |
| Agency | $399/mo — 15 reports, seats, priority regeneration, AEO annex + AnswerMonk visibility score bundled | The cross-sell bridge |
| Retention hook (later, validate separately) | +$49–99/mo segment monitoring: alerts when the category's design/copy conventions shift | Converts episodic pitches into recurring revenue; unproven — do not build until reorder behavior exists |
| Platform/wholesale (phase 3) | Metered API ~$15–25/pack; x402/Stripe agent-payable checkout | For builders embedding Brando; agents buying mid-session |

**Model rationale:** hybrid one-time + subscription matches the evidence — Looka's $65 one-time is its most-praised SKU, Tailor Brands' subscription-first model draws complaints, Indie Hackers sentiment favors per-report pricing for episodic jobs, and agencies accept monthly tiers because pitching is monthly.
