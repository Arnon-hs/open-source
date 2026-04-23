# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **1112** |
| 📁 **Categories** | **15** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 417 | [Browse →](./aiml/) |
| 📦 **Misc** | 205 | [Browse →](./misc/) |
| 🎨 **Frontend** | 123 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 94 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 63 | [Browse →](./backend/) |
| 🔧 **DevTools** | 44 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 43 | [Browse →](./crypto/) |
| 📊 **Data** | 33 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 27 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 22 | [Browse →](./mobile/) |
| 💳 **Payments** | 13 | [Browse →](./payments/) |
| 📈 **Trading** | 13 | [Browse →](./trading/) |
| 🔐 **Security** | 9 | [Browse →](./security/) |
| 🎯 **Product** | 5 | [Browse →](./product/) |
| ✨ **Design** | 1 | [Browse →](./design/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [freeCodeCamp/devdocs](./backend/freecodecamp-devdocs.md) | ⭐ 38.8k | Backend |
| 2 | [docmost/docmost](./misc/docmost-docmost.md) | ⭐ 19.9k | Misc |
| 3 | [XIU2/TrackersListCollection](./aiml/xiu2-trackerslistcollection.md) | ⭐ 31.1k | AI/ML |
| 4 | [vxcontrol/pentagi](./orchestration/vxcontrol-pentagi.md) | ⭐ 15.4k | Orchestration |
| 5 | [bluewave-labs/Checkmate](./frontend/bluewave-labs-checkmate.md) | ⭐ 9.7k | Frontend |
| 6 | [code-yeongyu/oh-my-openagent](./orchestration/code-yeongyu-oh-my-openagent.md) | ⭐ 53.5k | Orchestration |
| 7 | [affaan-m/everything-claude-code](./aiml/affaan-m-everything-claude-code.md) | ⭐ 164.4k | AI/ML |
| 8 | [ComposioHQ/composio](./aiml/composiohq-composio.md) | ⭐ 27.9k | AI/ML |
| 9 | [krzyzanowskim/CryptoSwift](./crypto/krzyzanowskim-cryptoswift.md) | ⭐ 10.5k | Crypto |
| 10 | [iOfficeAI/AionUi](./aiml/iofficeai-aionui.md) | ⭐ 22.4k | AI/ML |

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
