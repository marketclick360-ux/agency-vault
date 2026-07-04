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
- Medicare lead-generation business run by the operator; "Janet" (Janet
  Murillo) is associated with the Vercel account hosting the deployments
  (as of 2026-07, Vercel bot comments on `marketclick360` PRs) and is the end
  user of the Hermes bot and AgentOS (as of 2026-07-04, Hermes handoff doc).
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
  high). Meaning of "edlando": TBD — possibly a person/codename ("Ed Lando"?);
  do not state as fact. Candidate action: archive the repo to remove ambiguity.
- **Bubble migration status: UNKNOWN.** Both READMEs describe a "migration
  from Bubble." Assume Bubble may still serve real users until verified via:
  production domain DNS, Bubble app logs, Stripe/webhook destinations, form
  submission endpoints, CRM write paths, analytics. Tracked in backlog.

### Leads (as of 2026-07-04, operator)
- **Lead source plan: Google Ads** (stated by operator 2026-07-04). A Google
  Ads marketing campaign is a requested build — see [[clients/medicare-agency/backlog]].
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
- 2026-07-04: Initial version had canonical repo TBD. Resolved same day to
  `medicare-leads-saas` after direct comparison of both repos; lead-source
  plan (Google Ads), quarterly definition of done, tone/compliance, and
  people guidance supplied by operator.
