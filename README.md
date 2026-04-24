# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **3010** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1139 | [Browse →](./aiml/) |
| 📦 **Misc** | 470 | [Browse →](./misc/) |
| 🎨 **Frontend** | 332 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 271 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 189 | [Browse →](./backend/) |
| 🔧 **DevTools** | 155 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 119 | [Browse →](./crypto/) |
| 📊 **Data** | 89 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 71 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 42 | [Browse →](./payments/) |
| 📱 **Mobile** | 39 | [Browse →](./mobile/) |
| 🔐 **Security** | 34 | [Browse →](./security/) |
| 📈 **Trading** | 34 | [Browse →](./trading/) |
| ✨ **Design** | 12 | [Browse →](./design/) |
| 🎯 **Product** | 11 | [Browse →](./product/) |
| 🏷️ **Marketing** | 3 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [supabase/supabase](./aiml/supabase-supabase.md) | ⭐ 101.3k | AI/ML |
| 2 | [fastapi/fastapi](./frontend/fastapi-fastapi.md) | ⭐ 97.6k | Frontend |
| 3 | [Kong/insomnia](./aiml/kong-insomnia.md) | ⭐ 38.3k | AI/ML |
| 4 | [ory/kratos](./aiml/ory-kratos.md) | ⭐ 13.6k | AI/ML |
| 5 | [frappe/erpnext](./aiml/frappe-erpnext.md) | ⭐ 33.2k | AI/ML |
| 6 | [kubernetes-sigs/external-dns](./backend/kubernetes-sigs-external-dns.md) | ⭐ 8.9k | Backend |
| 7 | [open-policy-agent/opa](./aiml/open-policy-agent-opa.md) | ⭐ 11.6k | AI/ML |
| 8 | [musescore/MuseScore](./aiml/musescore-musescore.md) | ⭐ 14.5k | AI/ML |
| 9 | [qdrant/qdrant](./aiml/qdrant-qdrant.md) | ⭐ 30.6k | AI/ML |
| 10 | [future-architect/vuls](./aiml/future-architect-vuls.md) | ⭐ 12.1k | AI/ML |

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
