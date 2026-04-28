# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **9740** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 3752 | [Browse →](./aiml/) |
| 📦 **Misc** | 1823 | [Browse →](./misc/) |
| 🎨 **Frontend** | 972 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 804 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 574 | [Browse →](./backend/) |
| 🔧 **DevTools** | 557 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 346 | [Browse →](./crypto/) |
| 📊 **Data** | 211 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 196 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 127 | [Browse →](./mobile/) |
| 💳 **Payments** | 116 | [Browse →](./payments/) |
| 📈 **Trading** | 98 | [Browse →](./trading/) |
| 🔐 **Security** | 90 | [Browse →](./security/) |
| ✨ **Design** | 32 | [Browse →](./design/) |
| 🎯 **Product** | 24 | [Browse →](./product/) |
| 🏷️ **Marketing** | 18 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [locustio/locust](./aiml/locustio-locust.md) | ⭐ 27.7k | AI/ML |
| 2 | [alirezarezvani/claude-skills](./orchestration/alirezarezvani-claude-skills.md) | ⭐ 13k | Orchestration |
| 3 | [prettier/prettier](./aiml/prettier-prettier.md) | ⭐ 51.8k | AI/ML |
| 4 | [temporalio/temporal](./orchestration/temporalio-temporal.md) | ⭐ 19.9k | Orchestration |
| 5 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 6 | [grafana/k6](./devtools/grafana-k6.md) | ⭐ 30.5k | DevTools |
| 7 | [ultralytics/ultralytics](./devtools/ultralytics-ultralytics.md) | ⭐ 56.5k | DevTools |
| 8 | [stride3d/stride](./misc/stride3d-stride.md) | ⭐ 7.6k | Misc |
| 9 | [bluewave-labs/Checkmate](./frontend/bluewave-labs-checkmate.md) | ⭐ 9.7k | Frontend |
| 10 | [MISP/MISP](./trading/misp-misp.md) | ⭐ 6.3k | Trading |

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
