---
date: 2026-07-04
updated: 2026-07-04
type: client-facts
client: medicare-agency
status: active
tier: internal
industry: "Medicare / insurance lead generation"
main-contact: "operator (marketclick360@gmail.com)"
canonical-repo: "medicare-leads-saas"
tags: [client-facts, medicare-agency, internal]
ai-first: true
timeline:
  - fact: "Enrolled as vault client #1 (internal dogfood client)"
    from: 2026-07-04
    until: present
    learned: 2026-07-04
    source: "operator instruction in vault-setup session"
  - fact: "Canonical production repo: medicare-leads-saas"
    from: 2026-02-02
    until: present
    learned: 2026-07-04
    source: "repo comparison, vault-setup session (see Product surface)"
---

## For future Claude
Company facts for the Medicare Agency, the operator's own Medicare
lead-generation business. Claims carry dates, sources, and confidence.
Top matter holds CURRENT state; `timeline:` holds changed facts with
provenance.

## Facts

### The business
- **Business name: Edlando Insurance** — domains edlandoins.com and
  edlando.com, Facebook page facebook.com/edlandoinsurance (as of 2022-01,
  "Janeth M - Activos y Accesos" Drive doc from vendor Marketing Rockstars;
  edlando.com confirmed current by ad-playbook URLs as of 2026-07-04).
  This resolves the "edlando" question: the old repo was named after the
  business.
- Operator: Janet (Janet Murillo), bilingual (EN/ES) licensed agent —
  contact 281-250-0687, marketclick360@gmail.com (as of 2022-01 Drive doc;
  license lines/states to confirm). Licensed in FL/TX/OR per the
  ad-playbook targeting sheet (as of 2026-07-04, confidence: medium).
- Past vendor: Marketing Rockstars (Andrea Argüelles Barragán,
  andy@marketing-rockstars.com) ran a Spanish life-insurance Facebook
  campaign circa 2022-01 (source: same Drive doc).
- Revenue model and unit economics: TBD — operator to supply.

### Canonical repo — RESOLVED 2026-07-04 (confidence: high)
- **`medicare-leads-saas` is the canonical production repo.** Evidence from
  direct repo inspection (as of 2026-07-04): active development 2026-02-02
  through 2026-07-03 with 41 merged PRs (qualifier flows, email nurture
  sequences EN/ES, lead magnets, coaching program, growth plan); Next.js
  16.0.7 + Supabase 2.45 + `vercel.json` (daily keep-alive cron) + `supabase/`
  migrations + `middleware.ts` + `docs/` operating system & owner's manual.
- **`edlando-medicare-saas` is an abandoned early scaffold** — three days of
  commits (2026-02-02 → 2026-02-04, landing page + BlazeSync intake + Cal
  booking), Next.js 14, no vercel.json, dormant for 5 months (confidence:
  high). Meaning of "edlando": RESOLVED 2026-07-04 — the business name,
  Edlando Insurance (see The business above). Candidate action: archive the
  repo to remove ambiguity.
- **Bubble migration status: UNKNOWN.** Both READMEs describe a "migration
  from Bubble." Assume Bubble may still serve real users until verified via:
  production domain DNS, Bubble app logs, Stripe/webhook destinations, form
  submission endpoints, CRM write paths, analytics. Tracked in backlog.

### Leads (as of 2026-07-04, operator)
- **Lead source plan: Google Ads** (stated by operator 2026-07-04). A Google
  Ads marketing campaign is a requested build — see [[clients/medicare-agency/backlog]].
- **An ad playbook already exists**: `medicare-leads-saas/docs/2-hands-build/ad-playbook.md`
  ("Edlando Ad Playbook", as of 2026-07-04) — Meta (FB/IG)-first: launch
  order (Spanish D-SNP El Paso + Hidalgo first, then T65 ES/PT/EN), full ad
  copy, targeting, $20-30/day budgets, UTM-tagged links to edlando.com
  landing pages, A/B headline switch, compliance notes. Google Ads is NOT
  yet covered beyond "get Medicare advertiser certification before running
  search ads."
- **Conversion plumbing is already wired on both ends** (as of 2026-07-04):
  SaaS `Analytics.tsx` accepts a Google Ads `AW-` tag via
  `NEXT_PUBLIC_GTAG_ID` and `lib/track.ts` fires `generate_lead`; the
  landing page captures GCLID + UTM, exposes `GOOGLE_ADS_ID` /
  `GOOGLE_ADS_CONVERSION_LABEL` hooks, and fires conversions on
  thank-you.html. Real IDs not yet plugged in (placeholders).
- Current volume: UNKNOWN — do not estimate. Truth source when measuring:
  last 90 days of lead records grouped by source, campaign, created_at,
  status, converted.
- Other candidate sources (unverified): organic/local referrals,
  partner/upline/downline referrals, landing-page forms, call campaigns,
  purchased/affiliate leads.

### Definition of done this quarter (stated by operator, 2026-07-04)
One clear production system, one canonical repo, a verified lead pipeline,
and compliant senior-facing messaging. Concretely:
- [x] Canonical GitHub repo identified and documented (2026-07-04, this note)
- [ ] Bubble fully retired OR explicitly documented as production-critical
- [ ] Lead intake works end-to-end: form/call/ad → CRM/database → follow-up → status tracking
- [ ] Weekly report exists: leads by source, cost if known, contact rate, booked appointments, closed policies/revenue if available
- [x] tone.md, people.md, and compliance checklist created (2026-07-04)
- [ ] No public-facing Medicare copy makes unverifiable promises or misleading claims (audit pending)

## History
- 2026-07-04 (later): "edlando" resolved to the business name Edlando
  Insurance via 2022 Drive doc; existing Meta ad playbook and pre-wired
  Google Ads conversion hooks discovered and documented.
- 2026-07-04: Initial version had canonical repo TBD. Resolved same day to
  `medicare-leads-saas` after direct comparison of both repos; lead-source
  plan (Google Ads), quarterly definition of done, tone/compliance, and
  people guidance supplied by operator.
