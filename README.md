# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **15193** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 5669 | [Browse →](./aiml/) |
| 📦 **Misc** | 3134 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1483 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1126 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 929 | [Browse →](./backend/) |
| 🔧 **DevTools** | 907 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 521 | [Browse →](./crypto/) |
| 📊 **Data** | 345 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 324 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 205 | [Browse →](./mobile/) |
| 💳 **Payments** | 162 | [Browse →](./payments/) |
| 📈 **Trading** | 155 | [Browse →](./trading/) |
| 🔐 **Security** | 124 | [Browse →](./security/) |
| ✨ **Design** | 49 | [Browse →](./design/) |
| 🏷️ **Marketing** | 31 | [Browse →](./marketing/) |
| 🎯 **Product** | 29 | [Browse →](./product/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [2dust/v2rayNG](./devtools/2dust-v2rayng.md) | ⭐ 55.3k | DevTools |
| 2 | [pathwaycom/pathway](./aiml/pathwaycom-pathway.md) | ⭐ 63.4k | AI/ML |
| 3 | [promptfoo/promptfoo](./aiml/promptfoo-promptfoo.md) | ⭐ 20.8k | AI/ML |
| 4 | [eosphoros-ai/DB-GPT](./aiml/eosphoros-ai-db-gpt.md) | ⭐ 18.6k | AI/ML |
| 5 | [gogf/gf](./backend/gogf-gf.md) | ⭐ 13.1k | Backend |
| 6 | [mikel-brostrom/boxmot](./misc/mikel-brostrom-boxmot.md) | ⭐ 8.1k | Misc |
| 7 | [matomo-org/matomo](./frontend/matomo-org-matomo.md) | ⭐ 21.5k | Frontend |
| 8 | [supabase/supabase](./aiml/supabase-supabase.md) | ⭐ 101.8k | AI/ML |
| 9 | [grpc/grpc-go](./backend/grpc-grpc-go.md) | ⭐ 22.9k | Backend |
| 10 | [ophub/amlogic-s9xxx-armbian](./aiml/ophub-amlogic-s9xxx-armbian.md) | ⭐ 9.1k | AI/ML |

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
