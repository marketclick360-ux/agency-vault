---
date: 2026-07-04
updated: 2026-07-04
type: tools
client: medicare-agency
tags: [tools, medicare-agency, internal]
ai-first: true
---

## For future Claude
The Medicare Agency's stack. Record WHERE each credential lives — NEVER the
value. All entries as of 2026-07-04, sourced from repo READMEs and session
records.

## Stack

| Tool | Used for | Credentials live in |
|---|---|---|
| Vercel | Hosting: leads dashboard (`marketclick360`), SaaS apps | Vercel account (Janet Murillo's projects) |
| Supabase | Auth + Postgres for leads dashboard and `medicare-leads-saas` | Vercel env vars (`NEXT_PUBLIC_SUPABASE_URL`, `NEXT_PUBLIC_SUPABASE_ANON_KEY`) |
| Node lead-capture backend | `medicare-landing-page` submissions → NDJSON files | `ADMIN_TOKEN` / `ADMIN_USER`+`ADMIN_PASS` env vars on its host; production host TBD |
| Resend or webhook (optional) | Lead email notifications from the landing-page backend | `NOTIFY_EMAIL_PROVIDER` env config; whether enabled in production TBD |
| Bubble (legacy) | Original SaaS being migrated away from | TBD — is the Bubble app still live/serving users? |
| GitHub (`marketclick360-ux`) | All source repos | Operator's GitHub account |

## Repos

- `marketclick360` (`app/`) — leads dashboard (private repo)
- `medicare-landing-page` — landing page + capture backend
- `medicare-leads-saas` — Next.js 15 SaaS migration
- `edlando-medicare-saas` — earlier(?) SaaS migration (relationship TBD)
- `medicare-plan-search` — plan search app
