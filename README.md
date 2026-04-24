# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **2719** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1018 | [Browse →](./aiml/) |
| 📦 **Misc** | 439 | [Browse →](./misc/) |
| 🎨 **Frontend** | 297 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 252 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 171 | [Browse →](./backend/) |
| 🔧 **DevTools** | 136 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 108 | [Browse →](./crypto/) |
| 📊 **Data** | 77 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 62 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 40 | [Browse →](./payments/) |
| 📱 **Mobile** | 35 | [Browse →](./mobile/) |
| 🔐 **Security** | 31 | [Browse →](./security/) |
| 📈 **Trading** | 30 | [Browse →](./trading/) |
| ✨ **Design** | 11 | [Browse →](./design/) |
| 🎯 **Product** | 10 | [Browse →](./product/) |
| 🏷️ **Marketing** | 2 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [doocs/md](./aiml/doocs-md.md) | ⭐ 12.4k | AI/ML |
| 2 | [argoproj/argo-workflows](./aiml/argoproj-argo-workflows.md) | ⭐ 16.6k | AI/ML |
| 3 | [koodo-reader/koodo-reader](./aiml/koodo-reader-koodo-reader.md) | ⭐ 26.7k | AI/ML |
| 4 | [vectordotdev/vector](./aiml/vectordotdev-vector.md) | ⭐ 21.7k | AI/ML |
| 5 | [owncast/owncast](./misc/owncast-owncast.md) | ⭐ 11.2k | Misc |
| 6 | [YouMind-OpenLab/awesome-nano-banana-pro-prompts](./aiml/youmind-openlab-awesome-nano-banana-pro-prompts.md) | ⭐ 11.5k | AI/ML |
| 7 | [wilsonfreitas/awesome-quant](./trading/wilsonfreitas-awesome-quant.md) | ⭐ 25.8k | Trading |
| 8 | [ray-project/ray](./aiml/ray-project-ray.md) | ⭐ 42.3k | AI/ML |
| 9 | [firebase/firebase-js-sdk](./aiml/firebase-firebase-js-sdk.md) | ⭐ 5.1k | AI/ML |
| 10 | [frappe/frappe](./aiml/frappe-frappe.md) | ⭐ 10k | AI/ML |

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
