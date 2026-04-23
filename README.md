# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **1478** |
| 📁 **Categories** | **15** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 571 | [Browse →](./aiml/) |
| 📦 **Misc** | 249 | [Browse →](./misc/) |
| 🎨 **Frontend** | 156 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 138 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 81 | [Browse →](./backend/) |
| 🔧 **DevTools** | 66 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 55 | [Browse →](./crypto/) |
| 📊 **Data** | 41 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 35 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 26 | [Browse →](./mobile/) |
| 💳 **Payments** | 21 | [Browse →](./payments/) |
| 📈 **Trading** | 18 | [Browse →](./trading/) |
| 🔐 **Security** | 13 | [Browse →](./security/) |
| 🎯 **Product** | 6 | [Browse →](./product/) |
| ✨ **Design** | 2 | [Browse →](./design/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [ghostfolio/ghostfolio](./trading/ghostfolio-ghostfolio.md) | ⭐ 8.2k | Trading |
| 2 | [Qiskit/qiskit](./trading/qiskit-qiskit.md) | ⭐ 7.3k | Trading |
| 3 | [FreeCAD/FreeCAD](./misc/freecad-freecad.md) | ⭐ 30.5k | Misc |
| 4 | [mouredev/roadmap-retos-programacion](./frontend/mouredev-roadmap-retos-programacion.md) | ⭐ 8.2k | Frontend |
| 5 | [opf/openproject](./product/opf-openproject.md) | ⭐ 14.9k | Product |
| 6 | [elie222/inbox-zero](./aiml/elie222-inbox-zero.md) | ⭐ 10.5k | AI/ML |
| 7 | [curl/curl](./aiml/curl-curl.md) | ⭐ 41.4k | AI/ML |
| 8 | [monero-project/monero](./crypto/monero-project-monero.md) | ⭐ 10.5k | Crypto |
| 9 | [NousResearch/hermes-agent](./aiml/nousresearch-hermes-agent.md) | ⭐ 112k | AI/ML |
| 10 | [bpftrace/bpftrace](./misc/bpftrace-bpftrace.md) | ⭐ 10.1k | Misc |

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
