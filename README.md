# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **4379** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1781 | [Browse →](./aiml/) |
| 📦 **Misc** | 714 | [Browse →](./misc/) |
| 🧩 **Orchestration** | 435 | [Browse →](./orchestration/) |
| 🎨 **Frontend** | 427 | [Browse →](./frontend/) |
| 🔧 **DevTools** | 231 | [Browse →](./devtools/) |
| ⚙️ **Backend** | 222 | [Browse →](./backend/) |
| ⛓️ **Crypto** | 167 | [Browse →](./crypto/) |
| 📊 **Data** | 95 | [Browse →](./data/) |
| 💳 **Payments** | 86 | [Browse →](./payments/) |
| 📈 **Trading** | 58 | [Browse →](./trading/) |
| 🚀 **DevOps & Infra** | 52 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 48 | [Browse →](./mobile/) |
| 🔐 **Security** | 36 | [Browse →](./security/) |
| ✨ **Design** | 12 | [Browse →](./design/) |
| 🎯 **Product** | 10 | [Browse →](./product/) |
| 🏷️ **Marketing** | 5 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [alibaba/spring-cloud-alibaba](./frontend/alibaba-spring-cloud-alibaba.md) | ⭐ 29.1k | Frontend |
| 2 | [tw93/Pake](./misc/tw93-pake.md) | ⭐ 48.6k | Misc |
| 3 | [Anionex/banana-slides](./aiml/anionex-banana-slides.md) | ⭐ 14.4k | AI/ML |
| 4 | [huggingface/datasets](./aiml/huggingface-datasets.md) | ⭐ 21.5k | AI/ML |
| 5 | [curl/curl](./aiml/curl-curl.md) | ⭐ 41.8k | AI/ML |
| 6 | [vnotex/vnote](./aiml/vnotex-vnote.md) | ⭐ 12.8k | AI/ML |
| 7 | [MODSetter/SurfSense](./orchestration/modsetter-surfsense.md) | ⭐ 14.2k | Orchestration |
| 8 | [CISOfy/lynis](./aiml/cisofy-lynis.md) | ⭐ 15.6k | AI/ML |
| 9 | [renovatebot/renovate](./devtools/renovatebot-renovate.md) | ⭐ 21.5k | DevTools |
| 10 | [sherlock-project/sherlock](./aiml/sherlock-project-sherlock.md) | ⭐ 83.1k | AI/ML |

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
