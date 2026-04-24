# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **3879** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1484 | [Browse →](./aiml/) |
| 📦 **Misc** | 612 | [Browse →](./misc/) |
| 🎨 **Frontend** | 408 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 359 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 235 | [Browse →](./backend/) |
| 🔧 **DevTools** | 217 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 156 | [Browse →](./crypto/) |
| 📊 **Data** | 100 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 87 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 55 | [Browse →](./mobile/) |
| 💳 **Payments** | 54 | [Browse →](./payments/) |
| 📈 **Trading** | 41 | [Browse →](./trading/) |
| 🔐 **Security** | 39 | [Browse →](./security/) |
| ✨ **Design** | 15 | [Browse →](./design/) |
| 🎯 **Product** | 12 | [Browse →](./product/) |
| 🏷️ **Marketing** | 5 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [shadps4-emu/shadPS4](./frontend/shadps4-emu-shadps4.md) | ⭐ 30.9k | Frontend |
| 2 | [DioxusLabs/dioxus](./aiml/dioxuslabs-dioxus.md) | ⭐ 35.8k | AI/ML |
| 3 | [influxdata/telegraf](./aiml/influxdata-telegraf.md) | ⭐ 16.8k | AI/ML |
| 4 | [rundeck/rundeck](./orchestration/rundeck-rundeck.md) | ⭐ 6.1k | Orchestration |
| 5 | [birobirobiro/awesome-shadcn-ui](./frontend/birobirobiro-awesome-shadcn-ui.md) | ⭐ 19.4k | Frontend |
| 6 | [GoogleChrome/lighthouse](./devtools/googlechrome-lighthouse.md) | ⭐ 30.1k | DevTools |
| 7 | [catboost/catboost](./aiml/catboost-catboost.md) | ⭐ 8.9k | AI/ML |
| 8 | [dapr/dapr](./orchestration/dapr-dapr.md) | ⭐ 25.7k | Orchestration |
| 9 | [lutzroeder/netron](./aiml/lutzroeder-netron.md) | ⭐ 32.8k | AI/ML |
| 10 | [haifengl/smile](./aiml/haifengl-smile.md) | ⭐ 6.4k | AI/ML |

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
