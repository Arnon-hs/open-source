# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **5055** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1969 | [Browse →](./aiml/) |
| 📦 **Misc** | 804 | [Browse →](./misc/) |
| 🎨 **Frontend** | 500 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 482 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 300 | [Browse →](./backend/) |
| 🔧 **DevTools** | 279 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 181 | [Browse →](./crypto/) |
| 📊 **Data** | 125 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 117 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 74 | [Browse →](./payments/) |
| 📱 **Mobile** | 72 | [Browse →](./mobile/) |
| 📈 **Trading** | 55 | [Browse →](./trading/) |
| 🔐 **Security** | 53 | [Browse →](./security/) |
| ✨ **Design** | 22 | [Browse →](./design/) |
| 🎯 **Product** | 16 | [Browse →](./product/) |
| 🏷️ **Marketing** | 6 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [VoltAgent/awesome-agent-skills](./orchestration/voltagent-awesome-agent-skills.md) | ⭐ 18.7k | Orchestration |
| 2 | [js-org/js.org](./aiml/js-org-js.org.md) | ⭐ 5.7k | AI/ML |
| 3 | [Data-Centric-AI-Community/ydata-profiling](./aiml/data-centric-ai-community-ydata-profiling.md) | ⭐ 13.5k | AI/ML |
| 4 | [TanStack/query](./frontend/tanstack-query.md) | ⭐ 49.2k | Frontend |
| 5 | [ansible/awx](./frontend/ansible-awx.md) | ⭐ 15.4k | Frontend |
| 6 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 7 | [recharts/recharts](./crypto/recharts-recharts.md) | ⭐ 27k | Crypto |
| 8 | [google/langextract](./aiml/google-langextract.md) | ⭐ 35.8k | AI/ML |
| 9 | [langchain-ai/open-swe](./orchestration/langchain-ai-open-swe.md) | ⭐ 9.6k | Orchestration |
| 10 | [farion1231/cc-switch](./aiml/farion1231-cc-switch.md) | ⭐ 51k | AI/ML |

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
