# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **2099** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 797 | [Browse →](./aiml/) |
| 📦 **Misc** | 359 | [Browse →](./misc/) |
| 🎨 **Frontend** | 215 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 201 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 107 | [Browse →](./backend/) |
| 🔧 **DevTools** | 106 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 90 | [Browse →](./crypto/) |
| 📊 **Data** | 58 | [Browse →](./data/) |
| 💳 **Payments** | 54 | [Browse →](./payments/) |
| 📈 **Trading** | 33 | [Browse →](./trading/) |
| 🚀 **DevOps & Infra** | 29 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 24 | [Browse →](./mobile/) |
| 🔐 **Security** | 13 | [Browse →](./security/) |
| 🎯 **Product** | 7 | [Browse →](./product/) |
| ✨ **Design** | 5 | [Browse →](./design/) |
| 🏷️ **Marketing** | 1 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [jeecgboot/JeecgBoot](./orchestration/jeecgboot-jeecgboot.md) | ⭐ 46.1k | Orchestration |
| 2 | [aden-hive/hive](./orchestration/aden-hive-hive.md) | ⭐ 10.3k | Orchestration |
| 3 | [volcano-sh/volcano](./aiml/volcano-sh-volcano.md) | ⭐ 5.5k | AI/ML |
| 4 | [oraios/serena](./aiml/oraios-serena.md) | ⭐ 23.9k | AI/ML |
| 5 | [louislam/uptime-kuma](./frontend/louislam-uptime-kuma.md) | ⭐ 86.4k | Frontend |
| 6 | [pwndbg/pwndbg](./misc/pwndbg-pwndbg.md) | ⭐ 10.4k | Misc |
| 7 | [skypilot-org/skypilot](./aiml/skypilot-org-skypilot.md) | ⭐ 9.9k | AI/ML |
| 8 | [cvxpy/cvxpy](./misc/cvxpy-cvxpy.md) | ⭐ 6.2k | Misc |
| 9 | [invoke-ai/InvokeAI](./aiml/invoke-ai-invokeai.md) | ⭐ 27.1k | AI/ML |
| 10 | [astral-sh/ruff](./frontend/astral-sh-ruff.md) | ⭐ 47.4k | Frontend |

## 🚀 How it works

```mermaid
graph LR
  A[GitHub · HN · Reddit · PH] --> B[RepoScout]
  B --> C[Score · Dedupe · Categorize]
  C --> D[LLM Summarize]
  D --> E[PostgreSQL DB]
  D --> F[This Catalog]
```

1. **Discover** — 4 sources pulled in parallel
2. **Score** — weighted: stars, forks, recency, topics, source trust
3. **Categorize** — rule-based + LLM-assisted tagging
4. **Summarize** — concise bilingual (EN/RU) summaries via LLM
5. **Sync** — markdown committed here, metadata upserted to PostgreSQL

## 🛠️ Self-host

```bash
git clone https://github.com/kirbudilov01/reposearchengine
cp .env.example .env
# Set LLM_PROVIDER, CATALOG_REPO_PATH, DATABASE_URL, ...
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
