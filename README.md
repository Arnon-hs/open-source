# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **3059** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1217 | [Browse →](./aiml/) |
| 📦 **Misc** | 479 | [Browse →](./misc/) |
| 🧩 **Orchestration** | 300 | [Browse →](./orchestration/) |
| 🎨 **Frontend** | 297 | [Browse →](./frontend/) |
| ⚙️ **Backend** | 162 | [Browse →](./backend/) |
| 🔧 **DevTools** | 162 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 125 | [Browse →](./crypto/) |
| 📊 **Data** | 75 | [Browse →](./data/) |
| 💳 **Payments** | 72 | [Browse →](./payments/) |
| 📈 **Trading** | 48 | [Browse →](./trading/) |
| 🚀 **DevOps & Infra** | 42 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 37 | [Browse →](./mobile/) |
| 🔐 **Security** | 24 | [Browse →](./security/) |
| ✨ **Design** | 9 | [Browse →](./design/) |
| 🎯 **Product** | 8 | [Browse →](./product/) |
| 🏷️ **Marketing** | 2 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [kserve/kserve](./aiml/kserve-kserve.md) | ⭐ 5.4k | AI/ML |
| 2 | [alibaba/spring-ai-alibaba](./orchestration/alibaba-spring-ai-alibaba.md) | ⭐ 9.5k | Orchestration |
| 3 | [zalando/postgres-operator](./data/zalando-postgres-operator.md) | ⭐ 5.2k | Data |
| 4 | [frappe/erpnext](./aiml/frappe-erpnext.md) | ⭐ 33.7k | AI/ML |
| 5 | [webpack/webpack](./frontend/webpack-webpack.md) | ⭐ 65.8k | Frontend |
| 6 | [botpress/botpress](./orchestration/botpress-botpress.md) | ⭐ 14.7k | Orchestration |
| 7 | [warmcat/libwebsockets](./backend/warmcat-libwebsockets.md) | ⭐ 5.3k | Backend |
| 8 | [wshobson/agents](./orchestration/wshobson-agents.md) | ⭐ 35k | Orchestration |
| 9 | [alam00000/bentopdf](./devopsinfra/alam00000-bentopdf.md) | ⭐ 13.1k | DevOps & Infra |
| 10 | [mermaid-js/mermaid](./aiml/mermaid-js-mermaid.md) | ⭐ 87.9k | AI/ML |

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
