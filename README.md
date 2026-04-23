# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **1330** |
| 📁 **Categories** | **15** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 512 | [Browse →](./aiml/) |
| 📦 **Misc** | 231 | [Browse →](./misc/) |
| 🎨 **Frontend** | 138 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 120 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 76 | [Browse →](./backend/) |
| 🔧 **DevTools** | 57 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 48 | [Browse →](./crypto/) |
| 📊 **Data** | 37 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 32 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 26 | [Browse →](./mobile/) |
| 💳 **Payments** | 17 | [Browse →](./payments/) |
| 📈 **Trading** | 16 | [Browse →](./trading/) |
| 🔐 **Security** | 13 | [Browse →](./security/) |
| 🎯 **Product** | 5 | [Browse →](./product/) |
| ✨ **Design** | 2 | [Browse →](./design/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [openshift/origin](./aiml/openshift-origin.md) | ⭐ 8.6k | AI/ML |
| 2 | [lichess-org/lila](./backend/lichess-org-lila.md) | ⭐ 18.1k | Backend |
| 3 | [surrealdb/surrealdb](./backend/surrealdb-surrealdb.md) | ⭐ 31.9k | Backend |
| 4 | [docling-project/docling](./aiml/docling-project-docling.md) | ⭐ 58.4k | AI/ML |
| 5 | [langchain4j/langchain4j](./orchestration/langchain4j-langchain4j.md) | ⭐ 11.7k | Orchestration |
| 6 | [elie222/inbox-zero](./aiml/elie222-inbox-zero.md) | ⭐ 10.5k | AI/ML |
| 7 | [huggingface/transformers](./crypto/huggingface-transformers.md) | ⭐ 159.8k | Crypto |
| 8 | [rtk-ai/rtk](./aiml/rtk-ai-rtk.md) | ⭐ 32.8k | AI/ML |
| 9 | [ghostfolio/ghostfolio](./trading/ghostfolio-ghostfolio.md) | ⭐ 8.2k | Trading |
| 10 | [Qiskit/qiskit](./trading/qiskit-qiskit.md) | ⭐ 7.3k | Trading |

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
