# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **14499** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 5449 | [Browse →](./aiml/) |
| 📦 **Misc** | 2933 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1414 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1081 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 888 | [Browse →](./backend/) |
| 🔧 **DevTools** | 866 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 508 | [Browse →](./crypto/) |
| 📊 **Data** | 331 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 314 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 190 | [Browse →](./mobile/) |
| 💳 **Payments** | 156 | [Browse →](./payments/) |
| 📈 **Trading** | 147 | [Browse →](./trading/) |
| 🔐 **Security** | 120 | [Browse →](./security/) |
| ✨ **Design** | 45 | [Browse →](./design/) |
| 🎯 **Product** | 29 | [Browse →](./product/) |
| 🏷️ **Marketing** | 28 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [Yin-Hongwei/music-website](./frontend/yin-hongwei-music-website.md) | ⭐ 6.7k | Frontend |
| 2 | [grpc/grpc-go](./backend/grpc-grpc-go.md) | ⭐ 22.9k | Backend |
| 3 | [ophub/amlogic-s9xxx-armbian](./aiml/ophub-amlogic-s9xxx-armbian.md) | ⭐ 9.1k | AI/ML |
| 4 | [apache/dolphinscheduler](./orchestration/apache-dolphinscheduler.md) | ⭐ 14.3k | Orchestration |
| 5 | [kubernetes/kube-state-metrics](./aiml/kubernetes-kube-state-metrics.md) | ⭐ 6.1k | AI/ML |
| 6 | [remoteintech/remote-jobs](./aiml/remoteintech-remote-jobs.md) | ⭐ 40.3k | AI/ML |
| 7 | [krayin/laravel-crm](./frontend/krayin-laravel-crm.md) | ⭐ 22.4k | Frontend |
| 8 | [meilisearch/meilisearch](./aiml/meilisearch-meilisearch.md) | ⭐ 57.4k | AI/ML |
| 9 | [argoproj/argo-cd](./devopsinfra/argoproj-argo-cd.md) | ⭐ 22.8k | DevOps & Infra |
| 10 | [enricoros/big-AGI](./aiml/enricoros-big-agi.md) | ⭐ 6.9k | AI/ML |

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
