# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **15776** |
| 📁 **Categories** | **22** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · OpenAI · Anthropic · Gemini · Groq · Z.AI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 4806 | [Browse →](./aiml/) |
| 📦 **Misc** | 2875 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1447 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1290 | [Browse →](./orchestration/) |
| 🏷️ **Mcp** | 862 | [Browse →](./mcp/) |
| 🔧 **DevTools** | 802 | [Browse →](./devtools/) |
| ⚙️ **Backend** | 669 | [Browse →](./backend/) |
| 🏷️ **Automation** | 569 | [Browse →](./automation/) |
| ⛓️ **Crypto** | 523 | [Browse →](./crypto/) |
| 🏷️ **Knowledgerag** | 355 | [Browse →](./knowledgerag/) |
| 📊 **Data** | 329 | [Browse →](./data/) |
| 🏷️ **Database** | 264 | [Browse →](./database/) |
| 💳 **Payments** | 209 | [Browse →](./payments/) |
| 📱 **Mobile** | 189 | [Browse →](./mobile/) |
| 📈 **Trading** | 186 | [Browse →](./trading/) |
| 🚀 **DevOps & Infra** | 115 | [Browse →](./devopsinfra/) |
| 🔐 **Security** | 99 | [Browse →](./security/) |
| ✨ **Design** | 46 | [Browse →](./design/) |
| 🏷️ **Observability** | 46 | [Browse →](./observability/) |
| 🏷️ **Education** | 46 | [Browse →](./education/) |
| 🎯 **Product** | 27 | [Browse →](./product/) |
| 🏷️ **Marketing** | 22 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [Panniantong/Agent-Reach](./mcp/panniantong-agent-reach.md) | ⭐ 44.7k | Mcp |
| 2 | [headroomlabs-ai/headroom](./orchestration/headroomlabs-ai-headroom.md) | ⭐ 46.8k | Orchestration |
| 3 | [xberg-io/xberg](./mcp/xberg-io-xberg.md) | ⭐ 8.5k | Mcp |
| 4 | [xberg-io/kreuzberg](./mcp/xberg-io-kreuzberg.md) | ⭐ 8.5k | Mcp |
| 5 | [diegosouzapw/OmniRoute](./mcp/diegosouzapw-omniroute.md) | ⭐ 6.7k | Mcp |
| 6 | [langgenius/dify](./orchestration/langgenius-dify.md) | ⭐ 146.2k | Orchestration |
| 7 | [hey-api/hey-api](./payments/hey-api-hey-api.md) | ⭐ 5k | Payments |
| 8 | [OpenAPITools/openapi-generator](./backend/openapitools-openapi-generator.md) | ⭐ 26.2k | Backend |
| 9 | [cheshire-cat-ai/core](./mcp/cheshire-cat-ai-core.md) | ⭐ 3.1k | Mcp |
| 10 | [google-antigravity/antigravity-sdk-python](./mcp/google-antigravity-antigravity-sdk-python.md) | ⭐ 2k | Mcp |

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
2. **Score** — weighted: usefulness, quality, integration, production readiness, outlook, adoption
3. **Categorize** — rule-based tagging across product domains, integrations, MCP, RAG, automation and infrastructure
4. **Summarize** — concise RU/EN/ZH summaries via LLM with deterministic fallback
5. **Sync** — markdown committed here, metadata upserted to PostgreSQL

## 🛠️ Self-host

```bash
git clone https://github.com/kirbudilov01/reposearchengine
cp .env.example .env
# Set LLM_PROVIDER, CATALOG_REPO_PATH, DATABASE_URL, ...
npm install && npm start
```

Supports cloud LLM providers (OpenAI · Anthropic · OpenRouter · Gemini · Groq · Z.AI).

## 📦 Data format

- [`index.json`](./index.json) — full catalog sorted by score
- `<category>/README.md` — category index with ranked table
- `<category>/<owner>-<name>.md` — per-repo card with stats, topics, summary

## 📜 License

MIT (metadata). Each linked repository retains its own license.

---

<sub>🤖 Maintained automatically by RepoScout · Built with Claude Code</sub>
