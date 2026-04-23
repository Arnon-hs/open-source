# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **1879** |
| 📁 **Categories** | **15** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 706 | [Browse →](./aiml/) |
| 📦 **Misc** | 312 | [Browse →](./misc/) |
| 🎨 **Frontend** | 210 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 169 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 112 | [Browse →](./backend/) |
| 🔧 **DevTools** | 91 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 77 | [Browse →](./crypto/) |
| 📊 **Data** | 56 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 45 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 29 | [Browse →](./mobile/) |
| 💳 **Payments** | 23 | [Browse →](./payments/) |
| 📈 **Trading** | 21 | [Browse →](./trading/) |
| 🔐 **Security** | 17 | [Browse →](./security/) |
| 🎯 **Product** | 8 | [Browse →](./product/) |
| ✨ **Design** | 3 | [Browse →](./design/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [fmtlib/fmt](./misc/fmtlib-fmt.md) | ⭐ 23.4k | Misc |
| 2 | [mrousavy/react-native-vision-camera](./aiml/mrousavy-react-native-vision-camera.md) | ⭐ 9.3k | AI/ML |
| 3 | [apache/beam](./data/apache-beam.md) | ⭐ 8.6k | Data |
| 4 | [ClickHouse/ClickHouse](./aiml/clickhouse-clickhouse.md) | ⭐ 47k | AI/ML |
| 5 | [VectifyAI/PageIndex](./aiml/vectifyai-pageindex.md) | ⭐ 25.7k | AI/ML |
| 6 | [MemoriLabs/Memori](./orchestration/memorilabs-memori.md) | ⭐ 13.7k | Orchestration |
| 7 | [charmbracelet/bubbletea](./frontend/charmbracelet-bubbletea.md) | ⭐ 41.8k | Frontend |
| 8 | [nocobase/nocobase](./aiml/nocobase-nocobase.md) | ⭐ 22.2k | AI/ML |
| 9 | [comet-ml/opik](./orchestration/comet-ml-opik.md) | ⭐ 19k | Orchestration |
| 10 | [dgtlmoon/changedetection.io](./backend/dgtlmoon-changedetection.io.md) | ⭐ 31.2k | Backend |

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
