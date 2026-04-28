# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **9943** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 3837 | [Browse →](./aiml/) |
| 📦 **Misc** | 1860 | [Browse →](./misc/) |
| 🎨 **Frontend** | 988 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 818 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 588 | [Browse →](./backend/) |
| 🔧 **DevTools** | 569 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 354 | [Browse →](./crypto/) |
| 📊 **Data** | 215 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 202 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 130 | [Browse →](./mobile/) |
| 💳 **Payments** | 117 | [Browse →](./payments/) |
| 📈 **Trading** | 99 | [Browse →](./trading/) |
| 🔐 **Security** | 91 | [Browse →](./security/) |
| ✨ **Design** | 33 | [Browse →](./design/) |
| 🎯 **Product** | 24 | [Browse →](./product/) |
| 🏷️ **Marketing** | 18 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [locustio/locust](./aiml/locustio-locust.md) | ⭐ 27.7k | AI/ML |
| 2 | [alirezarezvani/claude-skills](./orchestration/alirezarezvani-claude-skills.md) | ⭐ 13k | Orchestration |
| 3 | [snowplow/snowplow](./data/snowplow-snowplow.md) | ⭐ 7k | Data |
| 4 | [lightningnetwork/lnd](./crypto/lightningnetwork-lnd.md) | ⭐ 8.1k | Crypto |
| 5 | [juicedata/juicefs](./aiml/juicedata-juicefs.md) | ⭐ 13.5k | AI/ML |
| 6 | [future-architect/vuls](./aiml/future-architect-vuls.md) | ⭐ 12.1k | AI/ML |
| 7 | [TanStack/table](./frontend/tanstack-table.md) | ⭐ 27.9k | Frontend |
| 8 | [ultralytics/ultralytics](./devtools/ultralytics-ultralytics.md) | ⭐ 56.5k | DevTools |
| 9 | [stride3d/stride](./misc/stride3d-stride.md) | ⭐ 7.6k | Misc |
| 10 | [louislam/uptime-kuma](./frontend/louislam-uptime-kuma.md) | ⭐ 86k | Frontend |

## 🚀 How it works

```mermaid
graph LR
  A[GitHub · HN · Reddit · PH] --> B[RepoScout]
  B --> C[Score · Dedupe · Categorize]
  C --> D[LLM Summarize]
  D --> E[Supabase DB]
  D --> F[This Catalog]
```

1. **Discover** — 4 sources pulled in parallel
2. **Score** — weighted: stars, forks, recency, topics, source trust
3. **Categorize** — rule-based + LLM-assisted tagging
4. **Summarize** — concise bilingual (EN/RU) summaries via LLM
5. **Sync** — markdown committed here, metadata upserted to Supabase

## 🛠️ Self-host

```bash
git clone https://github.com/kirbudilov01/reposearchengine
cp .env.example .env
# Set LLM_PROVIDER, CATALOG_REPO_PATH, SUPABASE_URL, ...
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
