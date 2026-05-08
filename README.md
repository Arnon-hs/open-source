# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **2659** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1035 | [Browse →](./aiml/) |
| 📦 **Misc** | 427 | [Browse →](./misc/) |
| 🧩 **Orchestration** | 267 | [Browse →](./orchestration/) |
| 🎨 **Frontend** | 263 | [Browse →](./frontend/) |
| 🔧 **DevTools** | 141 | [Browse →](./devtools/) |
| ⚙️ **Backend** | 138 | [Browse →](./backend/) |
| ⛓️ **Crypto** | 112 | [Browse →](./crypto/) |
| 📊 **Data** | 66 | [Browse →](./data/) |
| 💳 **Payments** | 61 | [Browse →](./payments/) |
| 📈 **Trading** | 44 | [Browse →](./trading/) |
| 🚀 **DevOps & Infra** | 38 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 31 | [Browse →](./mobile/) |
| 🔐 **Security** | 20 | [Browse →](./security/) |
| 🎯 **Product** | 8 | [Browse →](./product/) |
| ✨ **Design** | 6 | [Browse →](./design/) |
| 🏷️ **Marketing** | 2 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [vxcontrol/pentagi](./orchestration/vxcontrol-pentagi.md) | ⭐ 16.6k | Orchestration |
| 2 | [open-webui/open-webui](./aiml/open-webui-open-webui.md) | ⭐ 136.1k | AI/ML |
| 3 | [cvat-ai/cvat](./aiml/cvat-ai-cvat.md) | ⭐ 15.8k | AI/ML |
| 4 | [recharts/recharts](./crypto/recharts-recharts.md) | ⭐ 27.1k | Crypto |
| 5 | [godotengine/godot-docs](./misc/godotengine-godot-docs.md) | ⭐ 5.3k | Misc |
| 6 | [twentyhq/twenty](./aiml/twentyhq-twenty.md) | ⭐ 45.6k | AI/ML |
| 7 | [puppeteer/puppeteer](./backend/puppeteer-puppeteer.md) | ⭐ 94.3k | Backend |
| 8 | [cython/cython](./data/cython-cython.md) | ⭐ 10.7k | Data |
| 9 | [PowerShell/PowerShell](./misc/powershell-powershell.md) | ⭐ 53.3k | Misc |
| 10 | [knadh/listmonk](./payments/knadh-listmonk.md) | ⭐ 20k | Payments |

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
