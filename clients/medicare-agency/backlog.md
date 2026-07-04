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
| 2026-07-04 | **Add a Google Ads marketing campaign to the project** | open — scoped | Meta playbook already exists (`medicare-leads-saas/docs/2-hands-build/ad-playbook.md`); conversion hooks pre-wired both ends. Remaining work: (1) Google Medicare advertiser certification, (2) write the Google-search layer of the playbook (keywords, ad groups, RSA copy EN/ES, negatives) passing [[clients/medicare-agency/tone]], (3) plug real `AW-` ID + conversion label into the existing hooks, (4) test lead end-to-end before spend. |
| 2026-07-04 | Verify whether Bubble still serves production users | open | Check production DNS, Bubble logs, Stripe/webhooks, form endpoints, CRM writes, analytics. Blocks "Bubble retired" quarterly goal. |
| 2026-07-04 | Decide fate of `edlando-medicare-saas` (archive?) | open | Dormant since 2026-02-04; archiving removes repo ambiguity. "edlando" = Edlando Insurance (resolved 2026-07-04), so archiving is safe once operator confirms. |
| 2026-07-04 | End-to-end lead-intake verification (form/call/ad → DB → follow-up → status) | open | Quarterly goal; prerequisite for the weekly report numbers. |
| 2026-07-04 | Public-facing copy compliance audit | open | Sweep landing page + SaaS copy against the tone.md never-use list. |
