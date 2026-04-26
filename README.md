# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **6861** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2631 | [Browse →](./aiml/) |
| 📦 **Misc** | 1231 | [Browse →](./misc/) |
| 🎨 **Frontend** | 684 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 606 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 395 | [Browse →](./backend/) |
| 🔧 **DevTools** | 388 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 238 | [Browse →](./crypto/) |
| 📊 **Data** | 157 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 139 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 103 | [Browse →](./mobile/) |
| 💳 **Payments** | 94 | [Browse →](./payments/) |
| 📈 **Trading** | 71 | [Browse →](./trading/) |
| 🔐 **Security** | 69 | [Browse →](./security/) |
| ✨ **Design** | 26 | [Browse →](./design/) |
| 🎯 **Product** | 20 | [Browse →](./product/) |
| 🏷️ **Marketing** | 9 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [Dash-Industry-Forum/dash.js](./devtools/dash-industry-forum-dash.js.md) | ⭐ 5.5k | DevTools |
| 2 | [AccumulateMore/CV](./aiml/accumulatemore-cv.md) | ⭐ 20.3k | AI/ML |
| 3 | [istio/istio](./frontend/istio-istio.md) | ⭐ 38.2k | Frontend |
| 4 | [bluenviron/mediamtx](./backend/bluenviron-mediamtx.md) | ⭐ 18.6k | Backend |
| 5 | [debezium/debezium](./data/debezium-debezium.md) | ⭐ 12.7k | Data |
| 6 | [PaddlePaddle/PaddleOCR](./aiml/paddlepaddle-paddleocr.md) | ⭐ 76.6k | AI/ML |
| 7 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 8 | [payloadcms/payload](./frontend/payloadcms-payload.md) | ⭐ 42k | Frontend |
| 9 | [pingcap/tidb](./orchestration/pingcap-tidb.md) | ⭐ 40k | Orchestration |
| 10 | [shanraisshan/claude-code-best-practice](./orchestration/shanraisshan-claude-code-best-practice.md) | ⭐ 48.1k | Orchestration |

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
