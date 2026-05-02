# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **14371** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 5413 | [Browse →](./aiml/) |
| 📦 **Misc** | 2905 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1398 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1073 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 878 | [Browse →](./backend/) |
| 🔧 **DevTools** | 855 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 504 | [Browse →](./crypto/) |
| 📊 **Data** | 329 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 313 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 181 | [Browse →](./mobile/) |
| 💳 **Payments** | 156 | [Browse →](./payments/) |
| 📈 **Trading** | 146 | [Browse →](./trading/) |
| 🔐 **Security** | 119 | [Browse →](./security/) |
| ✨ **Design** | 44 | [Browse →](./design/) |
| 🎯 **Product** | 29 | [Browse →](./product/) |
| 🏷️ **Marketing** | 28 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [miurla/morphic](./aiml/miurla-morphic.md) | ⭐ 8.8k | AI/ML |
| 2 | [streamlink/streamlink](./aiml/streamlink-streamlink.md) | ⭐ 11.4k | AI/ML |
| 3 | [unionlabs/union](./crypto/unionlabs-union.md) | ⭐ 74.1k | Crypto |
| 4 | [WhiskeySockets/Baileys](./aiml/whiskeysockets-baileys.md) | ⭐ 9.2k | AI/ML |
| 5 | [getsentry/sentry-javascript](./frontend/getsentry-sentry-javascript.md) | ⭐ 8.6k | Frontend |
| 6 | [yamadashy/repomix](./aiml/yamadashy-repomix.md) | ⭐ 24.2k | AI/ML |
| 7 | [ether/etherpad](./misc/ether-etherpad.md) | ⭐ 18.3k | Misc |
| 8 | [argoproj/argo-cd](./devopsinfra/argoproj-argo-cd.md) | ⭐ 22.8k | DevOps & Infra |
| 9 | [zephyrproject-rtos/zephyr](./misc/zephyrproject-rtos-zephyr.md) | ⭐ 15.1k | Misc |
| 10 | [warmcat/libwebsockets](./backend/warmcat-libwebsockets.md) | ⭐ 5.3k | Backend |

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
