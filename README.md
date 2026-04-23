# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **858** |
| 📁 **Categories** | **15** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 372 | [Browse →](./aiml/) |
| 📦 **Misc** | 201 | [Browse →](./misc/) |
| 🎨 **Frontend** | 99 | [Browse →](./frontend/) |
| ⚙️ **Backend** | 52 | [Browse →](./backend/) |
| 🔧 **DevTools** | 32 | [Browse →](./devtools/) |
| 📊 **Data** | 28 | [Browse →](./data/) |
| 📱 **Mobile** | 24 | [Browse →](./mobile/) |
| 🚀 **DevOps & Infra** | 20 | [Browse →](./devopsinfra/) |
| ⛓️ **Crypto** | 8 | [Browse →](./crypto/) |
| 🔐 **Security** | 8 | [Browse →](./security/) |
| 📈 **Trading** | 4 | [Browse →](./trading/) |
| 🎯 **Product** | 3 | [Browse →](./product/) |
| ✨ **Design** | 3 | [Browse →](./design/) |
| 🏷️ **Marketing** | 2 | [Browse →](./marketing/) |
| 💳 **Payments** | 2 | [Browse →](./payments/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [keephq/keep](./aiml/keephq-keep.md) | ⭐ 11.7k | AI/ML |
| 2 | [usememos/memos](./frontend/usememos-memos.md) | ⭐ 59.1k | Frontend |
| 3 | [nautechsystems/nautilus_trader](./crypto/nautechsystems-nautilus-trader.md) | ⭐ 22.2k | Crypto |
| 4 | [XIU2/TrackersListCollection](./aiml/xiu2-trackerslistcollection.md) | ⭐ 31.1k | AI/ML |
| 5 | [NousResearch/hermes-agent](./aiml/nousresearch-hermes-agent.md) | ⭐ 110.7k | AI/ML |
| 6 | [farion1231/cc-switch](./aiml/farion1231-cc-switch.md) | ⭐ 49.2k | AI/ML |
| 7 | [DioxusLabs/dioxus](./aiml/dioxuslabs-dioxus.md) | ⭐ 35.8k | AI/ML |
| 8 | [microsoft/mcp-for-beginners](./aiml/microsoft-mcp-for-beginners.md) | ⭐ 15.9k | AI/ML |
| 9 | [azerothcore/azerothcore-wotlk](./backend/azerothcore-azerothcore-wotlk.md) | ⭐ 8.2k | Backend |
| 10 | [vxcontrol/pentagi](./aiml/vxcontrol-pentagi.md) | ⭐ 15.4k | AI/ML |

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
