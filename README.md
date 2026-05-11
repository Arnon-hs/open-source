# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **6614** |
| 📁 **Categories** | **22** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2501 | [Browse →](./aiml/) |
| 📦 **Misc** | 1200 | [Browse →](./misc/) |
| 🎨 **Frontend** | 659 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 583 | [Browse →](./orchestration/) |
| 🔧 **DevTools** | 354 | [Browse →](./devtools/) |
| ⚙️ **Backend** | 331 | [Browse →](./backend/) |
| ⛓️ **Crypto** | 227 | [Browse →](./crypto/) |
| 📊 **Data** | 156 | [Browse →](./data/) |
| 💳 **Payments** | 101 | [Browse →](./payments/) |
| 📈 **Trading** | 82 | [Browse →](./trading/) |
| 📱 **Mobile** | 79 | [Browse →](./mobile/) |
| 🚀 **DevOps & Infra** | 69 | [Browse →](./devopsinfra/) |
| 🏷️ **Mcp** | 65 | [Browse →](./mcp/) |
| 🏷️ **Automation** | 51 | [Browse →](./automation/) |
| 🔐 **Security** | 46 | [Browse →](./security/) |
| 🏷️ **Knowledgerag** | 41 | [Browse →](./knowledgerag/) |
| ✨ **Design** | 21 | [Browse →](./design/) |
| 🏷️ **Database** | 18 | [Browse →](./database/) |
| 🎯 **Product** | 14 | [Browse →](./product/) |
| 🏷️ **Marketing** | 9 | [Browse →](./marketing/) |
| 🏷️ **Observability** | 4 | [Browse →](./observability/) |
| 🏷️ **Education** | 3 | [Browse →](./education/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [ohmyzsh/ohmyzsh](./aiml/ohmyzsh-ohmyzsh.md) | ⭐ 186.9k | AI/ML |
| 2 | [teng-lin/notebooklm-py](./aiml/teng-lin-notebooklm-py.md) | ⭐ 12.9k | AI/ML |
| 3 | [google-gemini/gemini-cli](./aiml/google-gemini-gemini-cli.md) | ⭐ 103.3k | AI/ML |
| 4 | [n8n-io/n8n](./aiml/n8n-io-n8n.md) | ⭐ 186.9k | AI/ML |
| 5 | [mcp-use/mcp-use](./aiml/mcp-use-mcp-use.md) | ⭐ 9.9k | AI/ML |
| 6 | [D4Vinci/Scrapling](./aiml/d4vinci-scrapling.md) | ⭐ 47.9k | AI/ML |
| 7 | [PipedreamHQ/pipedream](./backend/pipedreamhq-pipedream.md) | ⭐ 11.3k | Backend |
| 8 | [subzeroid/instagrapi](./backend/subzeroid-instagrapi.md) | ⭐ 6.2k | Backend |
| 9 | [xerrors/Yuxi](./orchestration/xerrors-yuxi.md) | ⭐ 5.1k | Orchestration |
| 10 | [Klavis-AI/klavis](./aiml/klavis-ai-klavis.md) | ⭐ 5.7k | AI/ML |

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
