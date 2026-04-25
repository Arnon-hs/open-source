# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **4651** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1802 | [Browse →](./aiml/) |
| 📦 **Misc** | 740 | [Browse →](./misc/) |
| 🎨 **Frontend** | 467 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 439 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 277 | [Browse →](./backend/) |
| 🔧 **DevTools** | 249 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 174 | [Browse →](./crypto/) |
| 📊 **Data** | 119 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 110 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 69 | [Browse →](./payments/) |
| 📱 **Mobile** | 65 | [Browse →](./mobile/) |
| 📈 **Trading** | 51 | [Browse →](./trading/) |
| 🔐 **Security** | 49 | [Browse →](./security/) |
| ✨ **Design** | 19 | [Browse →](./design/) |
| 🎯 **Product** | 15 | [Browse →](./product/) |
| 🏷️ **Marketing** | 6 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [NoFxAiOS/nofx](./crypto/nofxaios-nofx.md) | ⭐ 12k | Crypto |
| 2 | [astral-sh/ruff](./frontend/astral-sh-ruff.md) | ⭐ 47.2k | Frontend |
| 3 | [alibaba/nacos](./aiml/alibaba-nacos.md) | ⭐ 32.9k | AI/ML |
| 4 | [nicolargo/glances](./backend/nicolargo-glances.md) | ⭐ 32.3k | Backend |
| 5 | [oppia/oppia](./misc/oppia-oppia.md) | ⭐ 6.7k | Misc |
| 6 | [nhivp/Awesome-Embedded](./aiml/nhivp-awesome-embedded.md) | ⭐ 8.5k | AI/ML |
| 7 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 8 | [coleam00/Archon](./aiml/coleam00-archon.md) | ⭐ 19.6k | AI/ML |
| 9 | [Mintplex-Labs/anything-llm](./aiml/mintplex-labs-anything-llm.md) | ⭐ 58.9k | AI/ML |
| 10 | [juicedata/juicefs](./aiml/juicedata-juicefs.md) | ⭐ 13.5k | AI/ML |

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
