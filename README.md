<div align="center">
  <h1>Vitrus</h1>
  <p><b>Analytics for the AI agent era.</b></p>
  <p>Cookie-free web analytics where every number carries the query that produced it.</p>
  <p>
    <a href="https://vitrus.dev">vitrus.dev</a> ·
    <a href="https://vitrus.dev/docs">Docs</a> ·
    <a href="https://github.com/Vitrus-Dev/vitrus">Source</a>
  </p>
</div>

---

Two things broke in web analytics at the same time.

**Measurement broke.** AI assistants send real visitors, and most analytics tools file roughly 70% of
them as "direct" because those assistants attach no campaign tag. Meanwhile AI crawlers read your
pages every day, and most tools either discard that or count it as people.

**Trust broke.** Analytics products now write summaries. A sentence like *"conversion fell 12% because
of the theme release"* makes two claims you cannot check: a number the model may have computed itself,
and a cause it cannot possibly know.

### What we build

**[vitrus](https://github.com/Vitrus-Dev/vitrus)** — the open-source core. Apache-2.0, zero runtime
dependencies, an embedded database, and a 2.4 KB tracker.

- Every metric travels as `{ id, sql, params, window, value }`. Click a number, read the query that produced it.
- Numbers are computed by deterministic SQL. The optional AI layer may rephrase them and may not invent them — a numeric guard drops any sentence it cannot support.
- AI referrals and AI crawlers are separate channels, never summed.
- No cookies, no stored identifier, no consent banner. Do Not Track is honoured by default.

Deliberately absent: session replay and ad-platform attribution.

### Getting started

```bash
bun install -g @vitrus/cli
vitrus init && vitrus site add "My site" example.com && vitrus start
```

Or use the hosted version at **[app.vitrus.dev](https://app.vitrus.dev)** — the same engine, with no
feature held back from the open source build.
