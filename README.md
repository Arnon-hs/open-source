# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **2500** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 926 | [Browse →](./aiml/) |
| 📦 **Misc** | 405 | [Browse →](./misc/) |
| 🎨 **Frontend** | 273 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 229 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 162 | [Browse →](./backend/) |
| 🔧 **DevTools** | 126 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 101 | [Browse →](./crypto/) |
| 📊 **Data** | 71 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 59 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 38 | [Browse →](./payments/) |
| 📱 **Mobile** | 35 | [Browse →](./mobile/) |
| 🔐 **Security** | 27 | [Browse →](./security/) |
| 📈 **Trading** | 27 | [Browse →](./trading/) |
| 🎯 **Product** | 10 | [Browse →](./product/) |
| ✨ **Design** | 9 | [Browse →](./design/) |
| 🏷️ **Marketing** | 2 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [asgeirtj/system_prompts_leaks](./aiml/asgeirtj-system-prompts-leaks.md) | ⭐ 38.8k | AI/ML |
| 2 | [apache/tvm](./misc/apache-tvm.md) | ⭐ 13.3k | Misc |
| 3 | [Anuken/Mindustry](./mobile/anuken-mindustry.md) | ⭐ 27.4k | Mobile |
| 4 | [stashapp/stash](./misc/stashapp-stash.md) | ⭐ 12.2k | Misc |
| 5 | [opf/openproject](./product/opf-openproject.md) | ⭐ 14.9k | Product |
| 6 | [dataelement/bisheng](./orchestration/dataelement-bisheng.md) | ⭐ 11.3k | Orchestration |
| 7 | [dokku/dokku](./aiml/dokku-dokku.md) | ⭐ 31.9k | AI/ML |
| 8 | [SBoudrias/Inquirer.js](./frontend/sboudrias-inquirer.js.md) | ⭐ 21.5k | Frontend |
| 9 | [zhayujie/CowAgent](./orchestration/zhayujie-cowagent.md) | ⭐ 43.7k | Orchestration |
| 10 | [cython/cython](./data/cython-cython.md) | ⭐ 10.7k | Data |

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
