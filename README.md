# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **5291** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2061 | [Browse →](./aiml/) |
| 📦 **Misc** | 851 | [Browse →](./misc/) |
| 🎨 **Frontend** | 518 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 504 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 310 | [Browse →](./backend/) |
| 🔧 **DevTools** | 295 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 192 | [Browse →](./crypto/) |
| 📊 **Data** | 130 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 120 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 78 | [Browse →](./payments/) |
| 📱 **Mobile** | 75 | [Browse →](./mobile/) |
| 📈 **Trading** | 58 | [Browse →](./trading/) |
| 🔐 **Security** | 54 | [Browse →](./security/) |
| ✨ **Design** | 22 | [Browse →](./design/) |
| 🎯 **Product** | 17 | [Browse →](./product/) |
| 🏷️ **Marketing** | 6 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [laramies/theHarvester](./aiml/laramies-theharvester.md) | ⭐ 16.1k | AI/ML |
| 2 | [novuhq/novu](./aiml/novuhq-novu.md) | ⭐ 38.9k | AI/ML |
| 3 | [apache/hudi](./data/apache-hudi.md) | ⭐ 6.1k | Data |
| 4 | [wilsonfreitas/awesome-quant](./trading/wilsonfreitas-awesome-quant.md) | ⭐ 25.8k | Trading |
| 5 | [cvxpy/cvxpy](./misc/cvxpy-cvxpy.md) | ⭐ 6.2k | Misc |
| 6 | [enricoros/big-AGI](./aiml/enricoros-big-agi.md) | ⭐ 6.9k | AI/ML |
| 7 | [apache/datafusion](./data/apache-datafusion.md) | ⭐ 8.6k | Data |
| 8 | [clockworklabs/SpacetimeDB](./backend/clockworklabs-spacetimedb.md) | ⭐ 24.6k | Backend |
| 9 | [vercel/ai](./aiml/vercel-ai.md) | ⭐ 23.8k | AI/ML |
| 10 | [m1k1o/neko](./frontend/m1k1o-neko.md) | ⭐ 20.7k | Frontend |

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
