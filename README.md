# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **6101** |
| 📁 **Categories** | **21** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2395 | [Browse →](./aiml/) |
| 📦 **Misc** | 1127 | [Browse →](./misc/) |
| 🎨 **Frontend** | 604 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 543 | [Browse →](./orchestration/) |
| 🔧 **DevTools** | 321 | [Browse →](./devtools/) |
| ⚙️ **Backend** | 302 | [Browse →](./backend/) |
| ⛓️ **Crypto** | 214 | [Browse →](./crypto/) |
| 📊 **Data** | 143 | [Browse →](./data/) |
| 💳 **Payments** | 98 | [Browse →](./payments/) |
| 📱 **Mobile** | 78 | [Browse →](./mobile/) |
| 📈 **Trading** | 78 | [Browse →](./trading/) |
| 🚀 **DevOps & Infra** | 65 | [Browse →](./devopsinfra/) |
| 🔐 **Security** | 45 | [Browse →](./security/) |
| ✨ **Design** | 20 | [Browse →](./design/) |
| 🏷️ **Automation** | 18 | [Browse →](./automation/) |
| 🎯 **Product** | 14 | [Browse →](./product/) |
| 🏷️ **Mcp** | 10 | [Browse →](./mcp/) |
| 🏷️ **Database** | 9 | [Browse →](./database/) |
| 🏷️ **Knowledgerag** | 8 | [Browse →](./knowledgerag/) |
| 🏷️ **Marketing** | 8 | [Browse →](./marketing/) |
| 🏷️ **Observability** | 1 | [Browse →](./observability/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [ohmyzsh/ohmyzsh](./aiml/ohmyzsh-ohmyzsh.md) | ⭐ 186.9k | AI/ML |
| 2 | [teng-lin/notebooklm-py](./aiml/teng-lin-notebooklm-py.md) | ⭐ 12.9k | AI/ML |
| 3 | [google-gemini/gemini-cli](./aiml/google-gemini-gemini-cli.md) | ⭐ 103.3k | AI/ML |
| 4 | [open-webui/open-webui](./aiml/open-webui-open-webui.md) | ⭐ 136.1k | AI/ML |
| 5 | [n8n-io/n8n](./aiml/n8n-io-n8n.md) | ⭐ 186.9k | AI/ML |
| 6 | [mcp-use/mcp-use](./aiml/mcp-use-mcp-use.md) | ⭐ 9.9k | AI/ML |
| 7 | [D4Vinci/Scrapling](./aiml/d4vinci-scrapling.md) | ⭐ 47.9k | AI/ML |
| 8 | [wshobson/agents](./orchestration/wshobson-agents.md) | ⭐ 35k | Orchestration |
| 9 | [sickn33/antigravity-awesome-skills](./orchestration/sickn33-antigravity-awesome-skills.md) | ⭐ 36.8k | Orchestration |
| 10 | [PipedreamHQ/pipedream](./backend/pipedreamhq-pipedream.md) | ⭐ 11.3k | Backend |

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

Supports local LLMs (Ollama) and cloud providers (OpenAI · Anthropic · OpenRouter).

## 📦 Data format

- [`index.json`](./index.json) — full catalog sorted by score
- `<category>/README.md` — category index with ranked table
- `<category>/<owner>-<name>.md` — per-repo card with stats, topics, summary

## 📜 License

MIT (metadata). Each linked repository retains its own license.

---

<sub>🤖 Maintained automatically by RepoScout · Built with Claude Code</sub>
