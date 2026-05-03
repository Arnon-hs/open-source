# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **15504** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 5784 | [Browse →](./aiml/) |
| 📦 **Misc** | 3202 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1516 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1143 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 947 | [Browse →](./backend/) |
| 🔧 **DevTools** | 924 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 528 | [Browse →](./crypto/) |
| 📊 **Data** | 353 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 332 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 211 | [Browse →](./mobile/) |
| 💳 **Payments** | 165 | [Browse →](./payments/) |
| 📈 **Trading** | 160 | [Browse →](./trading/) |
| 🔐 **Security** | 127 | [Browse →](./security/) |
| ✨ **Design** | 51 | [Browse →](./design/) |
| 🏷️ **Marketing** | 31 | [Browse →](./marketing/) |
| 🎯 **Product** | 30 | [Browse →](./product/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [Laravel-Lang/lang](./payments/laravel-lang-lang.md) | ⭐ 7.8k | Payments |
| 2 | [ShareX/ShareX](./product/sharex-sharex.md) | ⭐ 37k | Product |
| 3 | [beekeeper-studio/beekeeper-studio](./backend/beekeeper-studio-beekeeper-studio.md) | ⭐ 22.7k | Backend |
| 4 | [getmaxun/maxun](./aiml/getmaxun-maxun.md) | ⭐ 15.5k | AI/ML |
| 5 | [stashapp/stash](./misc/stashapp-stash.md) | ⭐ 12.3k | Misc |
| 6 | [v2rayA/v2rayA](./frontend/v2raya-v2raya.md) | ⭐ 15k | Frontend |
| 7 | [YouMind-OpenLab/awesome-nano-banana-pro-prompts](./aiml/youmind-openlab-awesome-nano-banana-pro-prompts.md) | ⭐ 11.8k | AI/ML |
| 8 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 9 | [apache/thrift](./backend/apache-thrift.md) | ⭐ 10.9k | Backend |
| 10 | [PaddlePaddle/PaddleOCR](./aiml/paddlepaddle-paddleocr.md) | ⭐ 77k | AI/ML |

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
