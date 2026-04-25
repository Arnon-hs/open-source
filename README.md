# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **4168** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1600 | [Browse →](./aiml/) |
| 📦 **Misc** | 656 | [Browse →](./misc/) |
| 🎨 **Frontend** | 423 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 395 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 254 | [Browse →](./backend/) |
| 🔧 **DevTools** | 233 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 163 | [Browse →](./crypto/) |
| 📊 **Data** | 109 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 95 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 58 | [Browse →](./payments/) |
| 📱 **Mobile** | 57 | [Browse →](./mobile/) |
| 📈 **Trading** | 46 | [Browse →](./trading/) |
| 🔐 **Security** | 45 | [Browse →](./security/) |
| ✨ **Design** | 15 | [Browse →](./design/) |
| 🎯 **Product** | 14 | [Browse →](./product/) |
| 🏷️ **Marketing** | 5 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [apache/spark](./data/apache-spark.md) | ⭐ 43.2k | Data |
| 2 | [opf/openproject](./product/opf-openproject.md) | ⭐ 14.9k | Product |
| 3 | [freeCodeCamp/freeCodeCamp](./frontend/freecodecamp-freecodecamp.md) | ⭐ 443.5k | Frontend |
| 4 | [supermemoryai/supermemory](./orchestration/supermemoryai-supermemory.md) | ⭐ 22.2k | Orchestration |
| 5 | [jenkinsci/jenkins](./backend/jenkinsci-jenkins.md) | ⭐ 25.2k | Backend |
| 6 | [tailcallhq/forgecode](./orchestration/tailcallhq-forgecode.md) | ⭐ 6.9k | Orchestration |
| 7 | [justcallmekoko/ESP32Marauder](./aiml/justcallmekoko-esp32marauder.md) | ⭐ 10.6k | AI/ML |
| 8 | [mickael-kerjean/filestash](./data/mickael-kerjean-filestash.md) | ⭐ 14.1k | Data |
| 9 | [tw93/Mole](./aiml/tw93-mole.md) | ⭐ 49.1k | AI/ML |
| 10 | [lutzroeder/netron](./aiml/lutzroeder-netron.md) | ⭐ 32.8k | AI/ML |

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
