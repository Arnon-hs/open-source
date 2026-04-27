# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **8287** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 3194 | [Browse →](./aiml/) |
| 📦 **Misc** | 1523 | [Browse →](./misc/) |
| 🎨 **Frontend** | 841 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 704 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 479 | [Browse →](./backend/) |
| 🔧 **DevTools** | 468 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 287 | [Browse →](./crypto/) |
| 📊 **Data** | 181 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 158 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 116 | [Browse →](./mobile/) |
| 💳 **Payments** | 111 | [Browse →](./payments/) |
| 📈 **Trading** | 85 | [Browse →](./trading/) |
| 🔐 **Security** | 76 | [Browse →](./security/) |
| ✨ **Design** | 28 | [Browse →](./design/) |
| 🎯 **Product** | 21 | [Browse →](./product/) |
| 🏷️ **Marketing** | 15 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [matomo-org/matomo](./frontend/matomo-org-matomo.md) | ⭐ 21.5k | Frontend |
| 2 | [shadcn-ui/ui](./aiml/shadcn-ui-ui.md) | ⭐ 113.1k | AI/ML |
| 3 | [OpenAPITools/openapi-generator](./backend/openapitools-openapi-generator.md) | ⭐ 26.2k | Backend |
| 4 | [hibernate/hibernate-orm](./data/hibernate-hibernate-orm.md) | ⭐ 6.4k | Data |
| 5 | [ZhuLinsen/daily_stock_analysis](./trading/zhulinsen-daily-stock-analysis.md) | ⭐ 31.8k | Trading |
| 6 | [getsentry/sentry-javascript](./frontend/getsentry-sentry-javascript.md) | ⭐ 8.6k | Frontend |
| 7 | [hellodigua/ChatLab](./aiml/hellodigua-chatlab.md) | ⭐ 6.1k | AI/ML |
| 8 | [storybookjs/storybook](./aiml/storybookjs-storybook.md) | ⭐ 89.8k | AI/ML |
| 9 | [cryptomator/cryptomator](./crypto/cryptomator-cryptomator.md) | ⭐ 15k | Crypto |
| 10 | [etcd-io/etcd](./data/etcd-io-etcd.md) | ⭐ 51.6k | Data |

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
