# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **4419** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1798 | [Browse →](./aiml/) |
| 📦 **Misc** | 723 | [Browse →](./misc/) |
| 🧩 **Orchestration** | 437 | [Browse →](./orchestration/) |
| 🎨 **Frontend** | 431 | [Browse →](./frontend/) |
| 🔧 **DevTools** | 235 | [Browse →](./devtools/) |
| ⚙️ **Backend** | 224 | [Browse →](./backend/) |
| ⛓️ **Crypto** | 167 | [Browse →](./crypto/) |
| 📊 **Data** | 95 | [Browse →](./data/) |
| 💳 **Payments** | 86 | [Browse →](./payments/) |
| 📈 **Trading** | 59 | [Browse →](./trading/) |
| 🚀 **DevOps & Infra** | 52 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 49 | [Browse →](./mobile/) |
| 🔐 **Security** | 36 | [Browse →](./security/) |
| ✨ **Design** | 12 | [Browse →](./design/) |
| 🎯 **Product** | 10 | [Browse →](./product/) |
| 🏷️ **Marketing** | 5 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [TeamNewPipe/NewPipe](./mobile/teamnewpipe-newpipe.md) | ⭐ 38k | Mobile |
| 2 | [ai-collection/ai-collection](./aiml/ai-collection-ai-collection.md) | ⭐ 8.9k | AI/ML |
| 3 | [RustPython/RustPython](./misc/rustpython-rustpython.md) | ⭐ 22k | Misc |
| 4 | [alibaba/spring-cloud-alibaba](./frontend/alibaba-spring-cloud-alibaba.md) | ⭐ 29.1k | Frontend |
| 5 | [Anionex/banana-slides](./aiml/anionex-banana-slides.md) | ⭐ 14.4k | AI/ML |
| 6 | [tw93/Pake](./misc/tw93-pake.md) | ⭐ 48.6k | Misc |
| 7 | [huggingface/datasets](./aiml/huggingface-datasets.md) | ⭐ 21.5k | AI/ML |
| 8 | [curl/curl](./aiml/curl-curl.md) | ⭐ 41.8k | AI/ML |
| 9 | [vnotex/vnote](./aiml/vnotex-vnote.md) | ⭐ 12.8k | AI/ML |
| 10 | [MODSetter/SurfSense](./orchestration/modsetter-surfsense.md) | ⭐ 14.2k | Orchestration |

## 🚀 How it works

```mermaid
graph LR
  A[GitHub · HN · Reddit · PH] --> B[RepoScout]
  B --> C[Score · Dedupe · Categorize]
  C --> D[LLM Summarize]
  D --> E[PostgreSQL DB]
  D --> F[This Catalog]
```

1. **Discover** — 4 sources pulled in parallel
2. **Score** — weighted: stars, forks, recency, topics, source trust
3. **Categorize** — rule-based + LLM-assisted tagging
4. **Summarize** — concise bilingual (EN/RU) summaries via LLM
5. **Sync** — markdown committed here, metadata upserted to PostgreSQL

## 🛠️ Self-host

```bash
git clone https://github.com/kirbudilov01/reposearchengine
cp .env.example .env
# Set LLM_PROVIDER, CATALOG_REPO_PATH, DATABASE_URL, ...
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
