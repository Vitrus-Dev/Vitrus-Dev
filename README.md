<p align="center">
  <a href="https://vitrus.dev"><img src="https://raw.githubusercontent.com/Vitrus-Dev/vitrus/main/.github/assets/banner.png" alt="Vitrus — open-source analytics for every app you ship. One panel you can check." width="100%"></a>
</p>

<p align="center">
  <a href="https://vitrus.dev/demo"><b>Live demo</b></a> ·
  <a href="https://vitrus.dev">Website</a> ·
  <a href="https://vitrus.dev/docs">Docs</a> ·
  <a href="https://vitrus.dev/docs/mcp">Use with ChatGPT / Claude</a> ·
  <a href="https://github.com/Vitrus-Dev/vitrus">Source</a>
</p>

---

**Open-source analytics for every app you ship. One panel you can check.**

Vitrus is cookie-free web and product analytics for websites, iOS and Android apps where every number opens the query that produced it — the SQL, its
parameters, the window and the rows. The weekly AI summary is checked against that same evidence: a
sentence whose number isn't in it is dropped before you read it.

- **All your apps, one panel** — add `vitrus.identify(user.id)` and see who is new, who came back, who you
  lost and who started paying, for every app side by side; open an app for each user, under a made-up name.
  The id is hashed in the browser before it is sent — no email or name is stored.
- **Heatmaps** — where people click and how far they scroll, per device, drawn from your own session
  recordings; nothing extra is collected.
- **AI traffic, told apart** — people that ChatGPT, Claude or Perplexity send you; crawlers that only read
  your pages; agents that sign their requests (Web Bot Auth). Never added together.
- **Ask your AI** — connect ChatGPT, Claude, Cursor or Claude Code over MCP (OAuth, read-only, 17 tools).
  Every answer carries its query, so the assistant cites instead of guessing. Listed in the official MCP
  Registry as `dev.vitrus/analytics`.
- **Everything else you expect** — real-time, a 3D globe, sessions, funnels, journeys, goals, revenue,
  retention, Web Vitals, errors, opt-in masked replay, Search Console.
- **No cookies, no consent banner.** A 3.0 KB script. Do Not Track honoured.

### Open source

**[vitrus](https://github.com/Vitrus-Dev/vitrus)** — Apache-2.0, zero runtime dependencies, one process and
one SQLite file. Self-host it for free:

```bash
bun install -g @vitrus-dev/cli
vitrus init && vitrus site add "My site" example.com
VITRUS_PASSWORD="a long secret" vitrus start
```

Or use the hosted version at **[app.vitrus.dev](https://app.vitrus.dev)** — free plan, paid plans from $12/month.
The self-hosted dashboard is simpler than the hosted one today; the queries behind every view are in the
open-source core.
