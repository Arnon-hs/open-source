# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **3502** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1344 | [Browse →](./aiml/) |
| 📦 **Misc** | 548 | [Browse →](./misc/) |
| 🎨 **Frontend** | 378 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 320 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 215 | [Browse →](./backend/) |
| 🔧 **DevTools** | 184 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 139 | [Browse →](./crypto/) |
| 📊 **Data** | 95 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 81 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 48 | [Browse →](./payments/) |
| 📱 **Mobile** | 46 | [Browse →](./mobile/) |
| 🔐 **Security** | 37 | [Browse →](./security/) |
| 📈 **Trading** | 37 | [Browse →](./trading/) |
| ✨ **Design** | 13 | [Browse →](./design/) |
| 🎯 **Product** | 12 | [Browse →](./product/) |
| 🏷️ **Marketing** | 5 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [Jackett/Jackett](./aiml/jackett-jackett.md) | ⭐ 15.2k | AI/ML |
| 2 | [catboost/catboost](./aiml/catboost-catboost.md) | ⭐ 8.9k | AI/ML |
| 3 | [monero-project/monero](./crypto/monero-project-monero.md) | ⭐ 10.5k | Crypto |
| 4 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 5 | [lobehub/lobehub](./orchestration/lobehub-lobehub.md) | ⭐ 75.6k | Orchestration |
| 6 | [FlowiseAI/Flowise](./orchestration/flowiseai-flowise.md) | ⭐ 52.2k | Orchestration |
| 7 | [opendataloader-project/opendataloader-pdf](./aiml/opendataloader-project-opendataloader-pdf.md) | ⭐ 19.2k | AI/ML |
| 8 | [quantumlib/Cirq](./trading/quantumlib-cirq.md) | ⭐ 4.9k | Trading |
| 9 | [streamlink/streamlink](./aiml/streamlink-streamlink.md) | ⭐ 11.4k | AI/ML |
| 10 | [FreeCAD/FreeCAD](./misc/freecad-freecad.md) | ⭐ 30.6k | Misc |

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
