# agency-vault 🔒

**PRIVATE** client knowledge vault for the MarketClick360 agency — per-client
facts, tone, tools, decisions, meetings, and backlogs. This is the memory that
makes every agency agent work.

## Rules of the road

- **This repo stays private.** Client data never leaves it — never into
  `marketclick360-skills` (public), the `obsidian-second-brain` fork (public),
  or any other public surface.
- **No secret values, ever.** Record *where* a credential lives, never the
  credential itself.
- **Claude sessions:** read [`_CLAUDE.md`](_CLAUDE.md) first — it is the
  operating manual. The full conventions (note rules, structure, propagation,
  scaffold) live in the `agency-client-vault` skill in
  [`marketclick360-skills`](https://github.com/marketclick360-ux/marketclick360-skills).

## Layout

| Path | Holds |
|---|---|
| `_CLAUDE.md` | Operating manual — read first |
| `CRITICAL_FACTS.md` | ~120-token always-current agency facts card |
| `index.md` | Catalog of every note — read before searching |
| `Logs/` | Daily operation log (append-only) |
| `agency/` | Agency identity (`SOUL.md`), decisions, time log |
| `clients/<slug>/` | One folder per client — card, facts, people, tone, tools, backlog, decisions, meetings, reports |
| `templates/` | Blank note templates |

## Add a client

```bash
bash <skills-repo>/claude-skills/skills/agency-client-vault/scripts/scaffold_vault.sh . "Client Name"
```

Then fill `_CLIENT.md` and `facts.md` from the intake record and add the
client to `index.md`.
