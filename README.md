# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **778** |
| 📁 **Categories** | **12** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 331 | [Browse →](./aiml/) |
| 📦 **Misc** | 190 | [Browse →](./misc/) |
| 🎨 **Frontend** | 93 | [Browse →](./frontend/) |
| ⚙️ **Backend** | 50 | [Browse →](./backend/) |
| 📊 **Data** | 29 | [Browse →](./data/) |
| 🔧 **DevTools** | 28 | [Browse →](./devtools/) |
| 📱 **Mobile** | 24 | [Browse →](./mobile/) |
| 🚀 **DevOps & Infra** | 17 | [Browse →](./devopsinfra/) |
| 🔐 **Security** | 8 | [Browse →](./security/) |
| 🎯 **Product** | 3 | [Browse →](./product/) |
| ✨ **Design** | 3 | [Browse →](./design/) |
| 🏷️ **Marketing** | 2 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [NousResearch/hermes-agent](./aiml/nousresearch-hermes-agent.md) | ⭐ 110.6k | AI/ML |
| 2 | [akkadotnet/akka.net](./frontend/akkadotnet-akka.net.md) | ⭐ 5k | Frontend |
| 3 | [apache/spark](./data/apache-spark.md) | ⭐ 43.2k | Data |
| 4 | [XIU2/TrackersListCollection](./aiml/xiu2-trackerslistcollection.md) | ⭐ 31.1k | AI/ML |
| 5 | [frappe/frappe](./aiml/frappe-frappe.md) | ⭐ 10k | AI/ML |
| 6 | [coder/coder](./aiml/coder-coder.md) | ⭐ 13k | AI/ML |
| 7 | [h2oai/h2o-3](./aiml/h2oai-h2o-3.md) | ⭐ 7.5k | AI/ML |
| 8 | [meshery/meshery](./frontend/meshery-meshery.md) | ⭐ 10.2k | Frontend |
| 9 | [matplotlib/matplotlib](./data/matplotlib-matplotlib.md) | ⭐ 22.7k | Data |
| 10 | [feast-dev/feast](./aiml/feast-dev-feast.md) | ⭐ 7k | AI/ML |

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
