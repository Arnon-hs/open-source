# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **9106** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 3508 | [Browse →](./aiml/) |
| 📦 **Misc** | 1682 | [Browse →](./misc/) |
| 🎨 **Frontend** | 912 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 757 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 530 | [Browse →](./backend/) |
| 🔧 **DevTools** | 525 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 330 | [Browse →](./crypto/) |
| 📊 **Data** | 196 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 183 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 123 | [Browse →](./mobile/) |
| 💳 **Payments** | 114 | [Browse →](./payments/) |
| 📈 **Trading** | 91 | [Browse →](./trading/) |
| 🔐 **Security** | 82 | [Browse →](./security/) |
| ✨ **Design** | 32 | [Browse →](./design/) |
| 🎯 **Product** | 22 | [Browse →](./product/) |
| 🏷️ **Marketing** | 19 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [electerm/electerm](./aiml/electerm-electerm.md) | ⭐ 14k | AI/ML |
| 2 | [TryGhost/Ghost](./payments/tryghost-ghost.md) | ⭐ 52.7k | Payments |
| 3 | [volcengine/OpenViking](./aiml/volcengine-openviking.md) | ⭐ 23.1k | AI/ML |
| 4 | [langchain4j/langchain4j](./orchestration/langchain4j-langchain4j.md) | ⭐ 11.8k | Orchestration |
| 5 | [deepset-ai/haystack](./orchestration/deepset-ai-haystack.md) | ⭐ 25k | Orchestration |
| 6 | [mermaid-js/mermaid](./aiml/mermaid-js-mermaid.md) | ⭐ 87.7k | AI/ML |
| 7 | [JanDeDobbeleer/oh-my-posh](./misc/jandedobbeleer-oh-my-posh.md) | ⭐ 22.3k | Misc |
| 8 | [ankidroid/Anki-Android](./mobile/ankidroid-anki-android.md) | ⭐ 11.1k | Mobile |
| 9 | [wolfpld/tracy](./misc/wolfpld-tracy.md) | ⭐ 15.7k | Misc |
| 10 | [BabylonJS/Babylon.js](./misc/babylonjs-babylon.js.md) | ⭐ 25.4k | Misc |

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
