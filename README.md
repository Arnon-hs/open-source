# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **32743** |
| 📁 **Categories** | **27** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · OpenAI · Anthropic · Gemini · Groq · Z.AI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 9249 | [Browse →](./aiml/) |
| 📦 **Misc** | 6710 | [Browse →](./misc/) |
| 🎨 **Frontend** | 2891 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 2317 | [Browse →](./orchestration/) |
| 🏷️ **Mcp** | 2073 | [Browse →](./mcp/) |
| 🔧 **DevTools** | 1540 | [Browse →](./devtools/) |
| 🏷️ **Automation** | 1402 | [Browse →](./automation/) |
| ⚙️ **Backend** | 1246 | [Browse →](./backend/) |
| ⛓️ **Crypto** | 1052 | [Browse →](./crypto/) |
| 🏷️ **Knowledgerag** | 779 | [Browse →](./knowledgerag/) |
| 🏷️ **Database** | 687 | [Browse →](./database/) |
| 📊 **Data** | 664 | [Browse →](./data/) |
| 📈 **Trading** | 369 | [Browse →](./trading/) |
| 📱 **Mobile** | 366 | [Browse →](./mobile/) |
| 💳 **Payments** | 365 | [Browse →](./payments/) |
| 🚀 **DevOps & Infra** | 227 | [Browse →](./devopsinfra/) |
| 🔐 **Security** | 206 | [Browse →](./security/) |
| 🏷️ **Education** | 145 | [Browse →](./education/) |
| 🏷️ **Observability** | 118 | [Browse →](./observability/) |
| ✨ **Design** | 115 | [Browse →](./design/) |
| 🎯 **Product** | 61 | [Browse →](./product/) |
| 🏷️ **Marketing** | 55 | [Browse →](./marketing/) |
| 🏷️ **Vertical-video** | 47 | [Browse →](./vertical-video/) |
| 🏷️ **Video-editing** | 34 | [Browse →](./video-editing/) |
| 🏷️ **Content-creation** | 20 | [Browse →](./content-creation/) |
| 🏷️ **Templates** | 4 | [Browse →](./templates/) |
| 🏷️ **Open-source** | 1 | [Browse →](./open-source/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [sickn33/agentic-awesome-skills](./orchestration/sickn33-agentic-awesome-skills.md) | ⭐ 42.6k | Orchestration |
| 2 | [Panniantong/Agent-Reach](./mcp/panniantong-agent-reach.md) | ⭐ 44.7k | Mcp |
| 3 | [headroomlabs-ai/headroom](./orchestration/headroomlabs-ai-headroom.md) | ⭐ 46.8k | Orchestration |
| 4 | [xberg-io/xberg](./mcp/xberg-io-xberg.md) | ⭐ 8.5k | Mcp |
| 5 | [xberg-io/kreuzberg](./mcp/xberg-io-kreuzberg.md) | ⭐ 8.5k | Mcp |
| 6 | [diegosouzapw/OmniRoute](./mcp/diegosouzapw-omniroute.md) | ⭐ 6.7k | Mcp |
| 7 | [langgenius/dify](./orchestration/langgenius-dify.md) | ⭐ 146.2k | Orchestration |
| 8 | [zeromicro/go-zero](./aiml/zeromicro-go-zero.md) | ⭐ 33.2k | AI/ML |
| 9 | [wasp-lang/open-saas](./payments/wasp-lang-open-saas.md) | ⭐ 14.9k | Payments |
| 10 | [firerpa/lamda](./mcp/firerpa-lamda.md) | ⭐ 7.9k | Mcp |

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

- [`index.json`](./index.json) — compact manifest for the sharded machine-readable catalog
- `data/repos-*.json` — catalog shards sorted by score (up to 1000 projects each)
- `<category>/README.md` — category index with ranked table
- `<category>/<owner>-<name>.md` — per-repo card with stats, topics, summary

## 📜 License

MIT (metadata). Each linked repository retains its own license.

---

<sub>🤖 Maintained automatically by RepoScout · Built with Claude Code</sub>
