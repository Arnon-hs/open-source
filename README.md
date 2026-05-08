# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **2819** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1106 | [Browse →](./aiml/) |
| 📦 **Misc** | 446 | [Browse →](./misc/) |
| 🧩 **Orchestration** | 280 | [Browse →](./orchestration/) |
| 🎨 **Frontend** | 275 | [Browse →](./frontend/) |
| ⚙️ **Backend** | 150 | [Browse →](./backend/) |
| 🔧 **DevTools** | 149 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 119 | [Browse →](./crypto/) |
| 📊 **Data** | 70 | [Browse →](./data/) |
| 💳 **Payments** | 65 | [Browse →](./payments/) |
| 📈 **Trading** | 46 | [Browse →](./trading/) |
| 🚀 **DevOps & Infra** | 40 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 34 | [Browse →](./mobile/) |
| 🔐 **Security** | 21 | [Browse →](./security/) |
| 🎯 **Product** | 8 | [Browse →](./product/) |
| ✨ **Design** | 8 | [Browse →](./design/) |
| 🏷️ **Marketing** | 2 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 34.2k | Payments |
| 2 | [lichess-org/lila](./backend/lichess-org-lila.md) | ⭐ 18.2k | Backend |
| 3 | [is-a-dev/register](./aiml/is-a-dev-register.md) | ⭐ 10.2k | AI/ML |
| 4 | [dream-num/univer](./aiml/dream-num-univer.md) | ⭐ 12.9k | AI/ML |
| 5 | [microsoft/mcp-for-beginners](./orchestration/microsoft-mcp-for-beginners.md) | ⭐ 16k | Orchestration |
| 6 | [JoeanAmier/XHS-Downloader](./backend/joeanamier-xhs-downloader.md) | ⭐ 11.1k | Backend |
| 7 | [usememos/memos](./frontend/usememos-memos.md) | ⭐ 59.4k | Frontend |
| 8 | [siteboon/claudecodeui](./aiml/siteboon-claudecodeui.md) | ⭐ 10.7k | AI/ML |
| 9 | [docusealco/docuseal](./aiml/docusealco-docuseal.md) | ⭐ 15.8k | AI/ML |
| 10 | [vxcontrol/pentagi](./orchestration/vxcontrol-pentagi.md) | ⭐ 16.6k | Orchestration |

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
