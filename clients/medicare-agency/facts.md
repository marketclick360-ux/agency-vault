---
date: 2026-07-04
updated: 2026-07-04
type: client-facts
client: medicare-agency
status: active
tier: internal
industry: "Medicare / insurance lead generation"
main-contact: "operator (marketclick360@gmail.com)"
tags: [client-facts, medicare-agency, internal]
ai-first: true
timeline:
  - fact: "Enrolled as vault client #1 (internal dogfood client)"
    from: 2026-07-04
    until: present
    learned: 2026-07-04
    source: "operator instruction in vault-setup session"
---

## For future Claude
Company facts for the Medicare Agency, the operator's own Medicare
lead-generation business. Everything below is sourced from the org's repos
and the 2026-07-04 sessions; claims the operator has not yet confirmed are
marked with confidence. Top matter holds CURRENT state; `timeline:` holds
changed facts with provenance.

## Facts

### The business
- Medicare lead-generation business run by the operator; "Janet" (Janet
  Murillo) is associated with the Vercel account hosting the deployments
  (as of 2026-07, Vercel bot comments on `marketclick360` PRs) and is the end
  user of the Hermes bot and AgentOS (as of 2026-07-04, Hermes handoff doc).
- Revenue model, lead volume, and unit economics: TBD — operator to supply.

### Product surface (as of 2026-07-04, from the repos)
- **Leads dashboard** — `marketclick360` repo `app/`: Next.js App Router +
  Supabase (auth + Postgres), pages `/dashboard` and `/leads` with CSV
  import; auto-deploys to Vercel on push to main. Build was broken by an
  unclosed `<div>` and fixed 2026-07-04 (source: buildout session record).
- **Landing page + lead capture** — `medicare-landing-page`: static pages
  (`index.html`, `questionnaire.html`, `quick-intake.html`) + a Node backend
  (default port 8787) saving to NDJSON files (`leads.ndjson`,
  `checklists.ndjson`, `failed-submissions.ndjson`), admin auth via
  ADMIN_TOKEN or Basic auth, optional email notifications (Resend/webhook)
  (source: repo README).
- **Lead-gen SaaS, Bubble→Next.js migration** — `medicare-leads-saas`
  (Next.js 15 + Supabase + Vercel) and `edlando-medicare-saas`; both READMEs
  describe a "migration from Bubble" (as of 2026-07-04). Which repo is
  canonical and the migration's completion state: TBD (confidence:
  speculation that medicare-leads-saas is the newer one, based on Next.js 15).
- **Plan search** — `medicare-plan-search`: Next.js app, stock
  create-next-app README, purpose per name is Medicare plan search; feature
  state TBD.

### Open questions for the operator
- Which SaaS repo is canonical — `medicare-leads-saas` or `edlando-medicare-saas`? What does "edlando" refer to?
- Where do leads come from today (paid ads? organic? partners?) and roughly how many per month?
- What does "done" look like this quarter for this business?
- Compliance posture: what CMS marketing rules do we already follow?
