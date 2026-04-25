# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **4731** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1831 | [Browse →](./aiml/) |
| 📦 **Misc** | 753 | [Browse →](./misc/) |
| 🎨 **Frontend** | 474 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 444 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 285 | [Browse →](./backend/) |
| 🔧 **DevTools** | 253 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 176 | [Browse →](./crypto/) |
| 📊 **Data** | 120 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 113 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 72 | [Browse →](./payments/) |
| 📱 **Mobile** | 65 | [Browse →](./mobile/) |
| 📈 **Trading** | 54 | [Browse →](./trading/) |
| 🔐 **Security** | 51 | [Browse →](./security/) |
| ✨ **Design** | 19 | [Browse →](./design/) |
| 🎯 **Product** | 15 | [Browse →](./product/) |
| 🏷️ **Marketing** | 6 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [harvard-edge/cs249r_book](./aiml/harvard-edge-cs249r-book.md) | ⭐ 23.8k | AI/ML |
| 2 | [janhq/jan](./aiml/janhq-jan.md) | ⭐ 42.1k | AI/ML |
| 3 | [Skyvern-AI/skyvern](./aiml/skyvern-ai-skyvern.md) | ⭐ 21.4k | AI/ML |
| 4 | [VictoriaMetrics/VictoriaMetrics](./data/victoriametrics-victoriametrics.md) | ⭐ 16.9k | Data |
| 5 | [web-platform-tests/wpt](./aiml/web-platform-tests-wpt.md) | ⭐ 5.9k | AI/ML |
| 6 | [winsiderss/systeminformer](./security/winsiderss-systeminformer.md) | ⭐ 14k | Security |
| 7 | [opendataloader-project/opendataloader-pdf](./aiml/opendataloader-project-opendataloader-pdf.md) | ⭐ 19.2k | AI/ML |
| 8 | [qdrant/qdrant](./aiml/qdrant-qdrant.md) | ⭐ 30.6k | AI/ML |
| 9 | [kornia/kornia](./aiml/kornia-kornia.md) | ⭐ 11.2k | AI/ML |
| 10 | [farion1231/cc-switch](./aiml/farion1231-cc-switch.md) | ⭐ 50.9k | AI/ML |

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
