# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **2699** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1052 | [Browse →](./aiml/) |
| 📦 **Misc** | 432 | [Browse →](./misc/) |
| 🧩 **Orchestration** | 269 | [Browse →](./orchestration/) |
| 🎨 **Frontend** | 266 | [Browse →](./frontend/) |
| 🔧 **DevTools** | 142 | [Browse →](./devtools/) |
| ⚙️ **Backend** | 141 | [Browse →](./backend/) |
| ⛓️ **Crypto** | 114 | [Browse →](./crypto/) |
| 📊 **Data** | 68 | [Browse →](./data/) |
| 💳 **Payments** | 61 | [Browse →](./payments/) |
| 📈 **Trading** | 46 | [Browse →](./trading/) |
| 🚀 **DevOps & Infra** | 39 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 31 | [Browse →](./mobile/) |
| 🔐 **Security** | 21 | [Browse →](./security/) |
| 🎯 **Product** | 8 | [Browse →](./product/) |
| ✨ **Design** | 7 | [Browse →](./design/) |
| 🏷️ **Marketing** | 2 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [siteboon/claudecodeui](./aiml/siteboon-claudecodeui.md) | ⭐ 10.7k | AI/ML |
| 2 | [docusealco/docuseal](./aiml/docusealco-docuseal.md) | ⭐ 15.8k | AI/ML |
| 3 | [vxcontrol/pentagi](./orchestration/vxcontrol-pentagi.md) | ⭐ 16.6k | Orchestration |
| 4 | [open-webui/open-webui](./aiml/open-webui-open-webui.md) | ⭐ 136.1k | AI/ML |
| 5 | [cvat-ai/cvat](./aiml/cvat-ai-cvat.md) | ⭐ 15.8k | AI/ML |
| 6 | [recharts/recharts](./crypto/recharts-recharts.md) | ⭐ 27.1k | Crypto |
| 7 | [godotengine/godot-docs](./misc/godotengine-godot-docs.md) | ⭐ 5.3k | Misc |
| 8 | [twentyhq/twenty](./aiml/twentyhq-twenty.md) | ⭐ 45.6k | AI/ML |
| 9 | [puppeteer/puppeteer](./backend/puppeteer-puppeteer.md) | ⭐ 94.3k | Backend |
| 10 | [cython/cython](./data/cython-cython.md) | ⭐ 10.7k | Data |

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
