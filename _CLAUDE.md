# Claude Operating Manual - MarketClick360 Agency Vault

> Read this file before doing anything in this vault.
> It overrides the agency-client-vault skill where they differ.

## Vault identity
- **Owner:** MarketClick360 (solo AI agent agency)
- **Purpose:** per-client knowledge that makes every agency agent work
- **Privacy:** PRIVATE repo. Client data never leaves it. No secret values, ever.
- **Last updated:** 2026-07-04

## Operating rules
1. Load progressively: CRITICAL_FACTS.md -> index.md -> the one client in play.
2. Search before creating. Never claim absence without an exhaustive search.
3. Notes follow the agency-client-vault skill's note-rules.md (AI-first:
   preamble, frontmatter, dated claims, wikilinks, confidence, bi-temporal
   timeline for changing facts).
4. Two-Output rule: client insight in conversation = answer + vault write.
5. Rewrite, don't append (except Logs/ and timeline: arrays). Add a
   ## History line when replacing a fact.
6. Propagate every write (see the skill's propagation table) and update
   index.md + Logs/2026-07-04.md.
7. Never delete: archive with _archived_ prefix + status: archived.

## Folder map
| Folder | Purpose |
|---|---|
| agency/ | Agency-level identity, decisions, time log |
| clients/<slug>/ | One folder per client - facts, people, tone, tools, backlog, decisions, meetings, reports |
| Logs/ | Daily operation log (append-only) |
| templates/ | Blank note templates |
