# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **2779** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1089 | [Browse →](./aiml/) |
| 📦 **Misc** | 441 | [Browse →](./misc/) |
| 🧩 **Orchestration** | 279 | [Browse →](./orchestration/) |
| 🎨 **Frontend** | 272 | [Browse →](./frontend/) |
| 🔧 **DevTools** | 147 | [Browse →](./devtools/) |
| ⚙️ **Backend** | 146 | [Browse →](./backend/) |
| ⛓️ **Crypto** | 118 | [Browse →](./crypto/) |
| 📊 **Data** | 69 | [Browse →](./data/) |
| 💳 **Payments** | 62 | [Browse →](./payments/) |
| 📈 **Trading** | 46 | [Browse →](./trading/) |
| 🚀 **DevOps & Infra** | 40 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 32 | [Browse →](./mobile/) |
| 🔐 **Security** | 21 | [Browse →](./security/) |
| 🎯 **Product** | 8 | [Browse →](./product/) |
| ✨ **Design** | 7 | [Browse →](./design/) |
| 🏷️ **Marketing** | 2 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [is-a-dev/register](./aiml/is-a-dev-register.md) | ⭐ 10.2k | AI/ML |
| 2 | [dream-num/univer](./aiml/dream-num-univer.md) | ⭐ 12.9k | AI/ML |
| 3 | [microsoft/mcp-for-beginners](./orchestration/microsoft-mcp-for-beginners.md) | ⭐ 16k | Orchestration |
| 4 | [JoeanAmier/XHS-Downloader](./backend/joeanamier-xhs-downloader.md) | ⭐ 11.1k | Backend |
| 5 | [usememos/memos](./frontend/usememos-memos.md) | ⭐ 59.4k | Frontend |
| 6 | [siteboon/claudecodeui](./aiml/siteboon-claudecodeui.md) | ⭐ 10.7k | AI/ML |
| 7 | [docusealco/docuseal](./aiml/docusealco-docuseal.md) | ⭐ 15.8k | AI/ML |
| 8 | [vxcontrol/pentagi](./orchestration/vxcontrol-pentagi.md) | ⭐ 16.6k | Orchestration |
| 9 | [open-webui/open-webui](./aiml/open-webui-open-webui.md) | ⭐ 136.1k | AI/ML |
| 10 | [cvat-ai/cvat](./aiml/cvat-ai-cvat.md) | ⭐ 15.8k | AI/ML |

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
