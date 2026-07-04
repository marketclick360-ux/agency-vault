---
date: 2026-07-04
updated: 2026-07-04
type: backlog
client: medicare-agency
tags: [backlog, medicare-agency]
ai-first: true
---

## For future Claude
Every request the Medicare Agency makes gets logged here with a date - the
backlog itself becomes upgrade evidence at renewal time.

| Date | Request | Status | Notes |
|---|---|---|---|
| 2026-07-04 | Identify the canonical SaaS repo | done 2026-07-04 | Resolved: `medicare-leads-saas` (see [[clients/medicare-agency/facts]]) |
| 2026-07-04 | **Add a Google Ads marketing campaign to the project** | in progress | Google-search layer WRITTEN 2026-07-04 (ad-playbook § Google Ads: G2 certification steps, security checklist, TPMO/compliance gates, campaigns, EN/ES keywords + negatives + RSA copy, conversion wiring, launch gate); `NEXT_PUBLIC_GADS_SEND_TO` conversion support added to `lib/track.ts` (PR #42). Operator-side remaining: (1) G2 certification in Google Ads, (2) plug real `AW-` ID + label into Vercel env vars, (3) TPMO disclaimer w/ real counts on landing pages, (4) test lead end-to-end — then launch per the gate. |
| 2026-07-04 | Verify whether Bubble still serves production users | open | Check production DNS, Bubble logs, Stripe/webhooks, form endpoints, CRM writes, analytics. Blocks "Bubble retired" quarterly goal. |
| 2026-07-04 | Decide fate of `edlando-medicare-saas` (archive?) | open | Dormant since 2026-02-04; archiving removes repo ambiguity. "edlando" = Edlando Insurance (resolved 2026-07-04), so archiving is safe once operator confirms. |
| 2026-07-04 | End-to-end lead-intake verification (form/call/ad → DB → follow-up → status) | open | Quarterly goal; prerequisite for the weekly report numbers. |
| 2026-07-04 | Public-facing copy compliance audit | open | Sweep landing page + SaaS copy against the tone.md never-use list. |
