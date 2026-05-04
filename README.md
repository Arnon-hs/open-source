# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **16296** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 6055 | [Browse →](./aiml/) |
| 📦 **Misc** | 3412 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1608 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1179 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 1000 | [Browse →](./backend/) |
| 🔧 **DevTools** | 956 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 546 | [Browse →](./crypto/) |
| 📊 **Data** | 375 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 354 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 224 | [Browse →](./mobile/) |
| 💳 **Payments** | 168 | [Browse →](./payments/) |
| 📈 **Trading** | 167 | [Browse →](./trading/) |
| 🔐 **Security** | 135 | [Browse →](./security/) |
| ✨ **Design** | 54 | [Browse →](./design/) |
| 🎯 **Product** | 32 | [Browse →](./product/) |
| 🏷️ **Marketing** | 31 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [pola-rs/polars](./data/pola-rs-polars.md) | ⭐ 38.4k | Data |
| 2 | [arkime/arkime](./data/arkime-arkime.md) | ⭐ 7.4k | Data |
| 3 | [farion1231/cc-switch](./aiml/farion1231-cc-switch.md) | ⭐ 59k | AI/ML |
| 4 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 5 | [mastra-ai/mastra](./aiml/mastra-ai-mastra.md) | ⭐ 23.6k | AI/ML |
| 6 | [knative/docs](./aiml/knative-docs.md) | ⭐ 5k | AI/ML |
| 7 | [screenpipe/screenpipe](./aiml/screenpipe-screenpipe.md) | ⭐ 18.5k | AI/ML |
| 8 | [alam00000/bentopdf](./devopsinfra/alam00000-bentopdf.md) | ⭐ 13.1k | DevOps & Infra |
| 9 | [JustArchiNET/ArchiSteamFarm](./backend/justarchinet-archisteamfarm.md) | ⭐ 13.3k | Backend |
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
