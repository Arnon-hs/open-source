# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **12261** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 4680 | [Browse →](./aiml/) |
| 📦 **Misc** | 2385 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1195 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 954 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 745 | [Browse →](./backend/) |
| 🔧 **DevTools** | 731 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 435 | [Browse →](./crypto/) |
| 📊 **Data** | 272 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 264 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 150 | [Browse →](./mobile/) |
| 💳 **Payments** | 130 | [Browse →](./payments/) |
| 📈 **Trading** | 128 | [Browse →](./trading/) |
| 🔐 **Security** | 108 | [Browse →](./security/) |
| ✨ **Design** | 37 | [Browse →](./design/) |
| 🎯 **Product** | 25 | [Browse →](./product/) |
| 🏷️ **Marketing** | 22 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [apify/crawlee](./aiml/apify-crawlee.md) | ⭐ 23k | AI/ML |
| 2 | [nocodb/nocodb](./aiml/nocodb-nocodb.md) | ⭐ 62.9k | AI/ML |
| 3 | [googleapis/mcp-toolbox](./aiml/googleapis-mcp-toolbox.md) | ⭐ 14.9k | AI/ML |
| 4 | [mumble-voip/mumble](./backend/mumble-voip-mumble.md) | ⭐ 8k | Backend |
| 5 | [ArvinLovegood/go-stock](./aiml/arvinlovegood-go-stock.md) | ⭐ 5.5k | AI/ML |
| 6 | [simple-icons/simple-icons](./design/simple-icons-simple-icons.md) | ⭐ 25k | Design |
| 7 | [astral-sh/ruff](./frontend/astral-sh-ruff.md) | ⭐ 47.3k | Frontend |
| 8 | [argoproj/argo-cd](./devopsinfra/argoproj-argo-cd.md) | ⭐ 22.8k | DevOps & Infra |
| 9 | [docling-project/docling](./aiml/docling-project-docling.md) | ⭐ 58.8k | AI/ML |
| 10 | [go-acme/lego](./devtools/go-acme-lego.md) | ⭐ 9.5k | DevTools |

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
