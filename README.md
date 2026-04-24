# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **3061** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1164 | [Browse →](./aiml/) |
| 📦 **Misc** | 477 | [Browse →](./misc/) |
| 🎨 **Frontend** | 336 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 274 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 191 | [Browse →](./backend/) |
| 🔧 **DevTools** | 159 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 122 | [Browse →](./crypto/) |
| 📊 **Data** | 89 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 72 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 43 | [Browse →](./payments/) |
| 📱 **Mobile** | 40 | [Browse →](./mobile/) |
| 🔐 **Security** | 34 | [Browse →](./security/) |
| 📈 **Trading** | 34 | [Browse →](./trading/) |
| ✨ **Design** | 12 | [Browse →](./design/) |
| 🎯 **Product** | 11 | [Browse →](./product/) |
| 🏷️ **Marketing** | 3 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [apache/dubbo](./backend/apache-dubbo.md) | ⭐ 41.6k | Backend |
| 2 | [fastapi/fastapi](./frontend/fastapi-fastapi.md) | ⭐ 97.6k | Frontend |
| 3 | [prometheus/alertmanager](./aiml/prometheus-alertmanager.md) | ⭐ 8.4k | AI/ML |
| 4 | [DIYgod/RSSHub](./misc/diygod-rsshub.md) | ⭐ 43.6k | Misc |
| 5 | [steven2358/awesome-generative-ai](./aiml/steven2358-awesome-generative-ai.md) | ⭐ 11.9k | AI/ML |
| 6 | [ory/kratos](./aiml/ory-kratos.md) | ⭐ 13.6k | AI/ML |
| 7 | [microsoft/ai-agents-for-beginners](./orchestration/microsoft-ai-agents-for-beginners.md) | ⭐ 59.1k | Orchestration |
| 8 | [volcengine/OpenViking](./aiml/volcengine-openviking.md) | ⭐ 23k | AI/ML |
| 9 | [biomejs/biome](./aiml/biomejs-biome.md) | ⭐ 24.5k | AI/ML |
| 10 | [MODSetter/SurfSense](./orchestration/modsetter-surfsense.md) | ⭐ 14k | Orchestration |

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
