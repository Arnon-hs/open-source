# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **14621** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 5493 | [Browse →](./aiml/) |
| 📦 **Misc** | 2966 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1425 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1088 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 896 | [Browse →](./backend/) |
| 🔧 **DevTools** | 869 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 513 | [Browse →](./crypto/) |
| 📊 **Data** | 332 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 317 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 194 | [Browse →](./mobile/) |
| 💳 **Payments** | 156 | [Browse →](./payments/) |
| 📈 **Trading** | 149 | [Browse →](./trading/) |
| 🔐 **Security** | 120 | [Browse →](./security/) |
| ✨ **Design** | 46 | [Browse →](./design/) |
| 🎯 **Product** | 29 | [Browse →](./product/) |
| 🏷️ **Marketing** | 28 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [datawhalechina/all-in-rag](./orchestration/datawhalechina-all-in-rag.md) | ⭐ 6.9k | Orchestration |
| 2 | [filamentphp/filament](./aiml/filamentphp-filament.md) | ⭐ 30.5k | AI/ML |
| 3 | [apache/dolphinscheduler](./orchestration/apache-dolphinscheduler.md) | ⭐ 14.3k | Orchestration |
| 4 | [remoteintech/remote-jobs](./aiml/remoteintech-remote-jobs.md) | ⭐ 40.3k | AI/ML |
| 5 | [hellodigua/ChatLab](./aiml/hellodigua-chatlab.md) | ⭐ 6.2k | AI/ML |
| 6 | [meilisearch/meilisearch](./aiml/meilisearch-meilisearch.md) | ⭐ 57.4k | AI/ML |
| 7 | [argoproj/argo-cd](./devopsinfra/argoproj-argo-cd.md) | ⭐ 22.8k | DevOps & Infra |
| 8 | [mlflow/mlflow](./orchestration/mlflow-mlflow.md) | ⭐ 25.7k | Orchestration |
| 9 | [immich-app/immich](./mobile/immich-app-immich.md) | ⭐ 99.5k | Mobile |
| 10 | [rapidsai/cudf](./aiml/rapidsai-cudf.md) | ⭐ 9.6k | AI/ML |

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
