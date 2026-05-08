# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **3139** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1248 | [Browse →](./aiml/) |
| 📦 **Misc** | 494 | [Browse →](./misc/) |
| 🧩 **Orchestration** | 311 | [Browse →](./orchestration/) |
| 🎨 **Frontend** | 308 | [Browse →](./frontend/) |
| ⚙️ **Backend** | 165 | [Browse →](./backend/) |
| 🔧 **DevTools** | 163 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 128 | [Browse →](./crypto/) |
| 📊 **Data** | 75 | [Browse →](./data/) |
| 💳 **Payments** | 72 | [Browse →](./payments/) |
| 📈 **Trading** | 48 | [Browse →](./trading/) |
| 🚀 **DevOps & Infra** | 44 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 38 | [Browse →](./mobile/) |
| 🔐 **Security** | 25 | [Browse →](./security/) |
| 🎯 **Product** | 9 | [Browse →](./product/) |
| ✨ **Design** | 9 | [Browse →](./design/) |
| 🏷️ **Marketing** | 2 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [kovidgoyal/kitty](./misc/kovidgoyal-kitty.md) | ⭐ 32.8k | Misc |
| 2 | [temporalio/temporal](./orchestration/temporalio-temporal.md) | ⭐ 20.1k | Orchestration |
| 3 | [weaviate/weaviate](./aiml/weaviate-weaviate.md) | ⭐ 16.2k | AI/ML |
| 4 | [alirezarezvani/claude-skills](./orchestration/alirezarezvani-claude-skills.md) | ⭐ 14.1k | Orchestration |
| 5 | [PrestaShop/PrestaShop](./frontend/prestashop-prestashop.md) | ⭐ 9.1k | Frontend |
| 6 | [armbian/build](./aiml/armbian-build.md) | ⭐ 5.2k | AI/ML |
| 7 | [kserve/kserve](./aiml/kserve-kserve.md) | ⭐ 5.4k | AI/ML |
| 8 | [alibaba/spring-ai-alibaba](./orchestration/alibaba-spring-ai-alibaba.md) | ⭐ 9.5k | Orchestration |
| 9 | [zalando/postgres-operator](./data/zalando-postgres-operator.md) | ⭐ 5.2k | Data |
| 10 | [frappe/erpnext](./aiml/frappe-erpnext.md) | ⭐ 33.7k | AI/ML |

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
