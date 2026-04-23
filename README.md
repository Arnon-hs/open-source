# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **1620** |
| 📁 **Categories** | **15** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 614 | [Browse →](./aiml/) |
| 📦 **Misc** | 273 | [Browse →](./misc/) |
| 🎨 **Frontend** | 169 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 149 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 92 | [Browse →](./backend/) |
| 🔧 **DevTools** | 77 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 69 | [Browse →](./crypto/) |
| 📊 **Data** | 46 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 38 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 27 | [Browse →](./mobile/) |
| 💳 **Payments** | 23 | [Browse →](./payments/) |
| 📈 **Trading** | 20 | [Browse →](./trading/) |
| 🔐 **Security** | 14 | [Browse →](./security/) |
| 🎯 **Product** | 6 | [Browse →](./product/) |
| ✨ **Design** | 3 | [Browse →](./design/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [TykTechnologies/tyk](./backend/tyktechnologies-tyk.md) | ⭐ 10.7k | Backend |
| 2 | [digoal/blog](./aiml/digoal-blog.md) | ⭐ 8.5k | AI/ML |
| 3 | [zephyrproject-rtos/zephyr](./misc/zephyrproject-rtos-zephyr.md) | ⭐ 15.1k | Misc |
| 4 | [cvat-ai/cvat](./aiml/cvat-ai-cvat.md) | ⭐ 15.7k | AI/ML |
| 5 | [coleam00/Archon](./aiml/coleam00-archon.md) | ⭐ 19.4k | AI/ML |
| 6 | [amruthpillai/reactive-resume](./aiml/amruthpillai-reactive-resume.md) | ⭐ 36.4k | AI/ML |
| 7 | [alibaba/nacos](./aiml/alibaba-nacos.md) | ⭐ 32.9k | AI/ML |
| 8 | [outline/outline](./frontend/outline-outline.md) | ⭐ 38.2k | Frontend |
| 9 | [keephq/keep](./aiml/keephq-keep.md) | ⭐ 11.7k | AI/ML |
| 10 | [elie222/inbox-zero](./aiml/elie222-inbox-zero.md) | ⭐ 10.5k | AI/ML |

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
