# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **2299** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 889 | [Browse →](./aiml/) |
| 📦 **Misc** | 381 | [Browse →](./misc/) |
| 🎨 **Frontend** | 235 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 220 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 117 | [Browse →](./backend/) |
| 🔧 **DevTools** | 114 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 96 | [Browse →](./crypto/) |
| 📊 **Data** | 60 | [Browse →](./data/) |
| 💳 **Payments** | 58 | [Browse →](./payments/) |
| 📈 **Trading** | 37 | [Browse →](./trading/) |
| 🚀 **DevOps & Infra** | 31 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 27 | [Browse →](./mobile/) |
| 🔐 **Security** | 18 | [Browse →](./security/) |
| 🎯 **Product** | 8 | [Browse →](./product/) |
| ✨ **Design** | 6 | [Browse →](./design/) |
| 🏷️ **Marketing** | 2 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [karatelabs/karate](./backend/karatelabs-karate.md) | ⭐ 8.9k | Backend |
| 2 | [documenso/documenso](./security/documenso-documenso.md) | ⭐ 12.8k | Security |
| 3 | [f/prompts.chat](./aiml/f-prompts.chat.md) | ⭐ 161.8k | AI/ML |
| 4 | [modelscope/ms-swift](./aiml/modelscope-ms-swift.md) | ⭐ 14k | AI/ML |
| 5 | [micro-editor/micro](./frontend/micro-editor-micro.md) | ⭐ 28.6k | Frontend |
| 6 | [1Panel-dev/MaxKB](./orchestration/1panel-dev-maxkb.md) | ⭐ 20.9k | Orchestration |
| 7 | [zhayujie/CowAgent](./orchestration/zhayujie-cowagent.md) | ⭐ 44.2k | Orchestration |
| 8 | [HKUDS/Vibe-Trading](./trading/hkuds-vibe-trading.md) | ⭐ 5.6k | Trading |
| 9 | [apache/datafusion](./data/apache-datafusion.md) | ⭐ 8.7k | Data |
| 10 | [catboost/catboost](./aiml/catboost-catboost.md) | ⭐ 8.9k | AI/ML |

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
