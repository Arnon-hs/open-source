# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **3408** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1302 | [Browse →](./aiml/) |
| 📦 **Misc** | 534 | [Browse →](./misc/) |
| 🎨 **Frontend** | 369 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 310 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 211 | [Browse →](./backend/) |
| 🔧 **DevTools** | 180 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 136 | [Browse →](./crypto/) |
| 📊 **Data** | 92 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 80 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 47 | [Browse →](./payments/) |
| 📱 **Mobile** | 46 | [Browse →](./mobile/) |
| 🔐 **Security** | 36 | [Browse →](./security/) |
| 📈 **Trading** | 36 | [Browse →](./trading/) |
| ✨ **Design** | 13 | [Browse →](./design/) |
| 🎯 **Product** | 11 | [Browse →](./product/) |
| 🏷️ **Marketing** | 5 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [trufflesecurity/trufflehog](./security/trufflesecurity-trufflehog.md) | ⭐ 25.9k | Security |
| 2 | [redox-os/redox](./misc/redox-os-redox.md) | ⭐ 16.3k | Misc |
| 3 | [influxdata/telegraf](./aiml/influxdata-telegraf.md) | ⭐ 16.8k | AI/ML |
| 4 | [duplicati/duplicati](./aiml/duplicati-duplicati.md) | ⭐ 14.5k | AI/ML |
| 5 | [photoprism/photoprism](./aiml/photoprism-photoprism.md) | ⭐ 39.6k | AI/ML |
| 6 | [mlflow/mlflow](./orchestration/mlflow-mlflow.md) | ⭐ 25.5k | Orchestration |
| 7 | [modelscope/ms-swift](./aiml/modelscope-ms-swift.md) | ⭐ 13.9k | AI/ML |
| 8 | [redisson/redisson](./frontend/redisson-redisson.md) | ⭐ 24.3k | Frontend |
| 9 | [openemr/openemr](./misc/openemr-openemr.md) | ⭐ 5.1k | Misc |
| 10 | [WhiskeySockets/Baileys](./aiml/whiskeysockets-baileys.md) | ⭐ 9.1k | AI/ML |

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
