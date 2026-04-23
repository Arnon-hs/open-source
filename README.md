# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **1716** |
| 📁 **Categories** | **15** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 652 | [Browse →](./aiml/) |
| 📦 **Misc** | 286 | [Browse →](./misc/) |
| 🎨 **Frontend** | 178 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 159 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 100 | [Browse →](./backend/) |
| 🔧 **DevTools** | 83 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 73 | [Browse →](./crypto/) |
| 📊 **Data** | 49 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 41 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 27 | [Browse →](./mobile/) |
| 💳 **Payments** | 23 | [Browse →](./payments/) |
| 📈 **Trading** | 21 | [Browse →](./trading/) |
| 🔐 **Security** | 15 | [Browse →](./security/) |
| 🎯 **Product** | 6 | [Browse →](./product/) |
| ✨ **Design** | 3 | [Browse →](./design/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [Automattic/wp-calypso](./frontend/automattic-wp-calypso.md) | ⭐ 12.6k | Frontend |
| 2 | [botpress/botpress](./orchestration/botpress-botpress.md) | ⭐ 14.6k | Orchestration |
| 3 | [appsmithorg/appsmith](./frontend/appsmithorg-appsmith.md) | ⭐ 39.7k | Frontend |
| 4 | [puppeteer/puppeteer](./backend/puppeteer-puppeteer.md) | ⭐ 94.2k | Backend |
| 5 | [FreshRSS/FreshRSS](./misc/freshrss-freshrss.md) | ⭐ 14.8k | Misc |
| 6 | [elie222/inbox-zero](./aiml/elie222-inbox-zero.md) | ⭐ 10.5k | AI/ML |
| 7 | [outline/outline](./frontend/outline-outline.md) | ⭐ 38.2k | Frontend |
| 8 | [n8n-io/n8n](./aiml/n8n-io-n8n.md) | ⭐ 185.3k | AI/ML |
| 9 | [Mintplex-Labs/anything-llm](./aiml/mintplex-labs-anything-llm.md) | ⭐ 58.8k | AI/ML |
| 10 | [Skyvern-AI/skyvern](./aiml/skyvern-ai-skyvern.md) | ⭐ 21.3k | AI/ML |

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
