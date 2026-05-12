# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **7431** |
| 📁 **Categories** | **22** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2686 | [Browse →](./aiml/) |
| 📦 **Misc** | 1354 | [Browse →](./misc/) |
| 🎨 **Frontend** | 726 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 634 | [Browse →](./orchestration/) |
| 🔧 **DevTools** | 394 | [Browse →](./devtools/) |
| ⚙️ **Backend** | 362 | [Browse →](./backend/) |
| ⛓️ **Crypto** | 260 | [Browse →](./crypto/) |
| 📊 **Data** | 174 | [Browse →](./data/) |
| 🏷️ **Mcp** | 140 | [Browse →](./mcp/) |
| 💳 **Payments** | 121 | [Browse →](./payments/) |
| 🏷️ **Automation** | 104 | [Browse →](./automation/) |
| 📱 **Mobile** | 86 | [Browse →](./mobile/) |
| 📈 **Trading** | 86 | [Browse →](./trading/) |
| 🏷️ **Knowledgerag** | 75 | [Browse →](./knowledgerag/) |
| 🚀 **DevOps & Infra** | 72 | [Browse →](./devopsinfra/) |
| 🔐 **Security** | 59 | [Browse →](./security/) |
| 🏷️ **Database** | 39 | [Browse →](./database/) |
| ✨ **Design** | 22 | [Browse →](./design/) |
| 🎯 **Product** | 15 | [Browse →](./product/) |
| 🏷️ **Observability** | 10 | [Browse →](./observability/) |
| 🏷️ **Marketing** | 9 | [Browse →](./marketing/) |
| 🏷️ **Education** | 3 | [Browse →](./education/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [ohmyzsh/ohmyzsh](./aiml/ohmyzsh-ohmyzsh.md) | ⭐ 186.9k | AI/ML |
| 2 | [google-gemini/gemini-cli](./aiml/google-gemini-gemini-cli.md) | ⭐ 103.3k | AI/ML |
| 3 | [n8n-io/n8n](./aiml/n8n-io-n8n.md) | ⭐ 186.9k | AI/ML |
| 4 | [PipedreamHQ/pipedream](./backend/pipedreamhq-pipedream.md) | ⭐ 11.3k | Backend |
| 5 | [teng-lin/notebooklm-py](./aiml/teng-lin-notebooklm-py.md) | ⭐ 12.9k | AI/ML |
| 6 | [rocketride-org/rocketride-server](./orchestration/rocketride-org-rocketride-server.md) | ⭐ 2.4k | Orchestration |
| 7 | [open-webui/open-webui](./aiml/open-webui-open-webui.md) | ⭐ 136.1k | AI/ML |
| 8 | [googleapis/mcp-toolbox](./aiml/googleapis-mcp-toolbox.md) | ⭐ 15k | AI/ML |
| 9 | [danny-avila/LibreChat](./orchestration/danny-avila-librechat.md) | ⭐ 36.7k | Orchestration |
| 10 | [BerriAI/litellm](./orchestration/berriai-litellm.md) | ⭐ 46k | Orchestration |

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
