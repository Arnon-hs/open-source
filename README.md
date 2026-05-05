# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **16787** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 6252 | [Browse →](./aiml/) |
| 📦 **Misc** | 3521 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1659 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1203 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 1028 | [Browse →](./backend/) |
| 🔧 **DevTools** | 976 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 565 | [Browse →](./crypto/) |
| 📊 **Data** | 384 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 367 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 229 | [Browse →](./mobile/) |
| 📈 **Trading** | 170 | [Browse →](./trading/) |
| 💳 **Payments** | 169 | [Browse →](./payments/) |
| 🔐 **Security** | 143 | [Browse →](./security/) |
| ✨ **Design** | 57 | [Browse →](./design/) |
| 🎯 **Product** | 33 | [Browse →](./product/) |
| 🏷️ **Marketing** | 31 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [cheeriojs/cheerio](./aiml/cheeriojs-cheerio.md) | ⭐ 30.3k | AI/ML |
| 2 | [mochajs/mocha](./devtools/mochajs-mocha.md) | ⭐ 22.9k | DevTools |
| 3 | [swagger-api/swagger-ui](./aiml/swagger-api-swagger-ui.md) | ⭐ 28.8k | AI/ML |
| 4 | [strapi/strapi](./backend/strapi-strapi.md) | ⭐ 72.1k | Backend |
| 5 | [zeek/zeek](./security/zeek-zeek.md) | ⭐ 7.6k | Security |
| 6 | [vectordotdev/vector](./aiml/vectordotdev-vector.md) | ⭐ 21.8k | AI/ML |
| 7 | [ray-project/ray](./aiml/ray-project-ray.md) | ⭐ 42.4k | AI/ML |
| 8 | [BasedHardware/omi](./aiml/basedhardware-omi.md) | ⭐ 12.4k | AI/ML |
| 9 | [meshery/meshery](./frontend/meshery-meshery.md) | ⭐ 10.2k | Frontend |
| 10 | [iv-org/invidious](./misc/iv-org-invidious.md) | ⭐ 19.6k | Misc |

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
