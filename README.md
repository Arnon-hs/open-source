# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **1032** |
| 📁 **Categories** | **15** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 386 | [Browse →](./aiml/) |
| 📦 **Misc** | 198 | [Browse →](./misc/) |
| 🎨 **Frontend** | 113 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 80 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 58 | [Browse →](./backend/) |
| 🔧 **DevTools** | 40 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 39 | [Browse →](./crypto/) |
| 📊 **Data** | 32 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 25 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 21 | [Browse →](./mobile/) |
| 📈 **Trading** | 13 | [Browse →](./trading/) |
| 💳 **Payments** | 12 | [Browse →](./payments/) |
| 🔐 **Security** | 9 | [Browse →](./security/) |
| 🎯 **Product** | 5 | [Browse →](./product/) |
| ✨ **Design** | 1 | [Browse →](./design/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [StarRocks/starrocks](./devtools/starrocks-starrocks.md) | ⭐ 11.6k | DevTools |
| 2 | [LMCache/LMCache](./aiml/lmcache-lmcache.md) | ⭐ 8.1k | AI/ML |
| 3 | [iced-rs/iced](./orchestration/iced-rs-iced.md) | ⭐ 30.3k | Orchestration |
| 4 | [langchain-ai/open-swe](./orchestration/langchain-ai-open-swe.md) | ⭐ 9.6k | Orchestration |
| 5 | [krzyzanowskim/CryptoSwift](./crypto/krzyzanowskim-cryptoswift.md) | ⭐ 10.5k | Crypto |
| 6 | [XIU2/TrackersListCollection](./aiml/xiu2-trackerslistcollection.md) | ⭐ 31.1k | AI/ML |
| 7 | [vxcontrol/pentagi](./orchestration/vxcontrol-pentagi.md) | ⭐ 15.4k | Orchestration |
| 8 | [caddyserver/caddy](./backend/caddyserver-caddy.md) | ⭐ 71.8k | Backend |
| 9 | [expo/expo](./frontend/expo-expo.md) | ⭐ 48.9k | Frontend |
| 10 | [nestjs/nest](./frontend/nestjs-nest.md) | ⭐ 75.3k | Frontend |

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
