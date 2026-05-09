# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **3499** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1395 | [Browse →](./aiml/) |
| 📦 **Misc** | 548 | [Browse →](./misc/) |
| 🧩 **Orchestration** | 355 | [Browse →](./orchestration/) |
| 🎨 **Frontend** | 348 | [Browse →](./frontend/) |
| ⚙️ **Backend** | 186 | [Browse →](./backend/) |
| 🔧 **DevTools** | 178 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 136 | [Browse →](./crypto/) |
| 📊 **Data** | 81 | [Browse →](./data/) |
| 💳 **Payments** | 80 | [Browse →](./payments/) |
| 📈 **Trading** | 53 | [Browse →](./trading/) |
| 🚀 **DevOps & Infra** | 47 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 40 | [Browse →](./mobile/) |
| 🔐 **Security** | 31 | [Browse →](./security/) |
| ✨ **Design** | 10 | [Browse →](./design/) |
| 🎯 **Product** | 9 | [Browse →](./product/) |
| 🏷️ **Marketing** | 2 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [JustArchiNET/ArchiSteamFarm](./backend/justarchinet-archisteamfarm.md) | ⭐ 13.3k | Backend |
| 2 | [winsiderss/systeminformer](./security/winsiderss-systeminformer.md) | ⭐ 14.5k | Security |
| 3 | [projectcalico/calico](./devopsinfra/projectcalico-calico.md) | ⭐ 7.2k | DevOps & Infra |
| 4 | [influxdata/influxdb](./frontend/influxdata-influxdb.md) | ⭐ 31.5k | Frontend |
| 5 | [nukeop/nuclear](./aiml/nukeop-nuclear.md) | ⭐ 17.5k | AI/ML |
| 6 | [kedro-org/kedro](./aiml/kedro-org-kedro.md) | ⭐ 10.9k | AI/ML |
| 7 | [payloadcms/payload](./frontend/payloadcms-payload.md) | ⭐ 42.3k | Frontend |
| 8 | [Lissy93/dashy](./frontend/lissy93-dashy.md) | ⭐ 25k | Frontend |
| 9 | [gfx-rs/wgpu](./backend/gfx-rs-wgpu.md) | ⭐ 17.1k | Backend |
| 10 | [reactos/reactos](./frontend/reactos-reactos.md) | ⭐ 17.5k | Frontend |

## 🚀 How it works

```mermaid
graph LR
  A[GitHub · HN · Reddit · PH] --> B[RepoScout]
  B --> C[Score · Dedupe · Categorize]
  C --> D[LLM Summarize]
  D --> E[PostgreSQL DB]
  D --> F[This Catalog]
```

1. **Discover** — 4 sources pulled in parallel
2. **Score** — weighted: stars, forks, recency, topics, source trust
3. **Categorize** — rule-based + LLM-assisted tagging
4. **Summarize** — concise bilingual (EN/RU) summaries via LLM
5. **Sync** — markdown committed here, metadata upserted to PostgreSQL

## 🛠️ Self-host

```bash
git clone https://github.com/kirbudilov01/reposearchengine
cp .env.example .env
# Set LLM_PROVIDER, CATALOG_REPO_PATH, DATABASE_URL, ...
npm install && npm start
```

Supports local LLMs (Ollama) and cloud providers (OpenAI · Anthropic · OpenRouter).

## 📦 Data format

- [`index.json`](./index.json) — full catalog sorted by score
- `<category>/README.md` — category index with ranked table
- `<category>/<owner>-<name>.md` — per-repo card with stats, topics, summary

## 📜 License

MIT (metadata). Each linked repository retains its own license.

---

<sub>🤖 Maintained automatically by RepoScout · Built with Claude Code</sub>
