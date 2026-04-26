# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **6770** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2595 | [Browse →](./aiml/) |
| 📦 **Misc** | 1205 | [Browse →](./misc/) |
| 🎨 **Frontend** | 670 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 602 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 391 | [Browse →](./backend/) |
| 🔧 **DevTools** | 388 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 235 | [Browse →](./crypto/) |
| 📊 **Data** | 156 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 138 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 102 | [Browse →](./mobile/) |
| 💳 **Payments** | 94 | [Browse →](./payments/) |
| 📈 **Trading** | 70 | [Browse →](./trading/) |
| 🔐 **Security** | 69 | [Browse →](./security/) |
| ✨ **Design** | 26 | [Browse →](./design/) |
| 🎯 **Product** | 20 | [Browse →](./product/) |
| 🏷️ **Marketing** | 9 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [apache/casbin](./aiml/apache-casbin.md) | ⭐ 20k | AI/ML |
| 2 | [Dash-Industry-Forum/dash.js](./devtools/dash-industry-forum-dash.js.md) | ⭐ 5.5k | DevTools |
| 3 | [AccumulateMore/CV](./aiml/accumulatemore-cv.md) | ⭐ 20.3k | AI/ML |
| 4 | [PaddlePaddle/PaddleOCR](./aiml/paddlepaddle-paddleocr.md) | ⭐ 76.6k | AI/ML |
| 5 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 6 | [shanraisshan/claude-code-best-practice](./orchestration/shanraisshan-claude-code-best-practice.md) | ⭐ 48.1k | Orchestration |
| 7 | [RustPython/RustPython](./misc/rustpython-rustpython.md) | ⭐ 22k | Misc |
| 8 | [Canner/WrenAI](./aiml/canner-wrenai.md) | ⭐ 15k | AI/ML |
| 9 | [Tencent/WeKnora](./aiml/tencent-weknora.md) | ⭐ 14k | AI/ML |
| 10 | [onyx-dot-app/onyx](./aiml/onyx-dot-app-onyx.md) | ⭐ 28.5k | AI/ML |

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
