# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **16905** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 6290 | [Browse →](./aiml/) |
| 📦 **Misc** | 3540 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1670 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1214 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 1036 | [Browse →](./backend/) |
| 🔧 **DevTools** | 988 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 567 | [Browse →](./crypto/) |
| 📊 **Data** | 388 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 369 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 235 | [Browse →](./mobile/) |
| 📈 **Trading** | 171 | [Browse →](./trading/) |
| 💳 **Payments** | 170 | [Browse →](./payments/) |
| 🔐 **Security** | 145 | [Browse →](./security/) |
| ✨ **Design** | 57 | [Browse →](./design/) |
| 🎯 **Product** | 34 | [Browse →](./product/) |
| 🏷️ **Marketing** | 31 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [cheeriojs/cheerio](./aiml/cheeriojs-cheerio.md) | ⭐ 30.3k | AI/ML |
| 2 | [strapi/strapi](./backend/strapi-strapi.md) | ⭐ 72.1k | Backend |
| 3 | [apache/beam](./data/apache-beam.md) | ⭐ 8.6k | Data |
| 4 | [zeek/zeek](./security/zeek-zeek.md) | ⭐ 7.6k | Security |
| 5 | [vectordotdev/vector](./aiml/vectordotdev-vector.md) | ⭐ 21.8k | AI/ML |
| 6 | [ray-project/ray](./aiml/ray-project-ray.md) | ⭐ 42.4k | AI/ML |
| 7 | [BasedHardware/omi](./aiml/basedhardware-omi.md) | ⭐ 12.4k | AI/ML |
| 8 | [meshery/meshery](./frontend/meshery-meshery.md) | ⭐ 10.2k | Frontend |
| 9 | [iv-org/invidious](./misc/iv-org-invidious.md) | ⭐ 19.6k | Misc |
| 10 | [Skyvern-AI/skyvern](./aiml/skyvern-ai-skyvern.md) | ⭐ 21.5k | AI/ML |

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
