<p align="center">
  <a href="https://vitrus.dev"><img src="https://raw.githubusercontent.com/Vitrus-Dev/vitrus/main/.github/assets/banner.png" alt="Vitrus — web analytics you can check" width="100%"></a>
</p>

<p align="center">
  <a href="https://vitrus.dev/demo"><b>Live demo</b></a> ·
  <a href="https://vitrus.dev">Website</a> ·
  <a href="https://vitrus.dev/docs">Docs</a> ·
  <a href="https://vitrus.dev/docs/mcp">Use with ChatGPT / Claude</a> ·
  <a href="https://github.com/Vitrus-Dev/vitrus">Source</a>
</p>

---

**Don't trust the dashboard. Check it.**

Vitrus is cookie-free web analytics where every number opens the query that produced it — the SQL, its
parameters, the window and the rows. The weekly AI summary is checked against that same evidence: a
sentence whose number isn't in it is dropped before you read it.

- **AI traffic, told apart** — people that ChatGPT, Claude or Perplexity send you; crawlers that only read
  your pages; agents that sign their requests (Web Bot Auth). Never added together.
- **Ask your AI** — connect ChatGPT, Claude, Cursor or Claude Code over MCP (OAuth, read-only, 15 tools).
  Every answer carries its query, so the assistant cites instead of guessing. Listed in the official MCP
  Registry as `dev.vitrus/analytics`.
- **Everything else you expect** — real-time, a 3D globe, sessions, funnels, journeys, goals, revenue,
  retention, Web Vitals, errors, opt-in masked replay, Search Console.
- **No cookies, no consent banner.** A 2.6 KB script. Do Not Track honoured.

### Open source

**[vitrus](https://github.com/Vitrus-Dev/vitrus)** — Apache-2.0, zero runtime dependencies, one process and
one SQLite file. Self-host it for free:

```bash
git clone https://github.com/Vitrus-Dev/vitrus && cd vitrus
bun install && bun run build:tracker
alias vitrus="bun $PWD/packages/cli/src/cli.ts"
vitrus init && vitrus site add "My site" example.com
VITRUS_PASSWORD="a long secret" vitrus start
```

Or use the hosted version at **[app.vitrus.dev](https://app.vitrus.dev)** — free plan, paid plans from $12/month.
The self-hosted dashboard is simpler than the hosted one today; the queries behind every view are in the
open-source core.
