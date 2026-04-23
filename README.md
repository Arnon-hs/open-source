# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **907** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 390 | [Browse →](./aiml/) |
| 📦 **Misc** | 203 | [Browse →](./misc/) |
| 🎨 **Frontend** | 106 | [Browse →](./frontend/) |
| ⚙️ **Backend** | 55 | [Browse →](./backend/) |
| 🔧 **DevTools** | 38 | [Browse →](./devtools/) |
| 📊 **Data** | 28 | [Browse →](./data/) |
| 📱 **Mobile** | 23 | [Browse →](./mobile/) |
| 🚀 **DevOps & Infra** | 22 | [Browse →](./devopsinfra/) |
| ⛓️ **Crypto** | 13 | [Browse →](./crypto/) |
| 🔐 **Security** | 8 | [Browse →](./security/) |
| 📈 **Trading** | 6 | [Browse →](./trading/) |
| 🧩 **Orchestration** | 4 | [Browse →](./orchestration/) |
| 🎯 **Product** | 3 | [Browse →](./product/) |
| ✨ **Design** | 3 | [Browse →](./design/) |
| 💳 **Payments** | 3 | [Browse →](./payments/) |
| 🏷️ **Marketing** | 2 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [XIU2/TrackersListCollection](./aiml/xiu2-trackerslistcollection.md) | ⭐ 31.1k | AI/ML |
| 2 | [NousResearch/hermes-agent](./aiml/nousresearch-hermes-agent.md) | ⭐ 110.7k | AI/ML |
| 3 | [microsoft/mcp-for-beginners](./aiml/microsoft-mcp-for-beginners.md) | ⭐ 15.9k | AI/ML |
| 4 | [azerothcore/azerothcore-wotlk](./backend/azerothcore-azerothcore-wotlk.md) | ⭐ 8.2k | Backend |
| 5 | [vxcontrol/pentagi](./aiml/vxcontrol-pentagi.md) | ⭐ 15.4k | AI/ML |
| 6 | [kickstarter/ios-oss](./frontend/kickstarter-ios-oss.md) | ⭐ 8.6k | Frontend |
| 7 | [caddyserver/caddy](./backend/caddyserver-caddy.md) | ⭐ 71.8k | Backend |
| 8 | [expo/expo](./frontend/expo-expo.md) | ⭐ 48.9k | Frontend |
| 9 | [nestjs/nest](./frontend/nestjs-nest.md) | ⭐ 75.3k | Frontend |
| 10 | [medusajs/medusa](./frontend/medusajs-medusa.md) | ⭐ 32.7k | Frontend |

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
