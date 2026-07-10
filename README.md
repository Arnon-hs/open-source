# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **160** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · OpenAI · Anthropic · Gemini · Groq · Z.AI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 54 | [Browse →](./aiml/) |
| 📦 **Misc** | 23 | [Browse →](./misc/) |
| 🧩 **Orchestration** | 23 | [Browse →](./orchestration/) |
| 🎨 **Frontend** | 15 | [Browse →](./frontend/) |
| ⚙️ **Backend** | 10 | [Browse →](./backend/) |
| 📊 **Data** | 9 | [Browse →](./data/) |
| 🏷️ **Mcp** | 9 | [Browse →](./mcp/) |
| 📱 **Mobile** | 7 | [Browse →](./mobile/) |
| 🚀 **DevOps & Infra** | 2 | [Browse →](./devopsinfra/) |
| 🏷️ **Knowledgerag** | 2 | [Browse →](./knowledgerag/) |
| 🔐 **Security** | 1 | [Browse →](./security/) |
| 🔧 **DevTools** | 1 | [Browse →](./devtools/) |
| ✨ **Design** | 1 | [Browse →](./design/) |
| 🏷️ **Automation** | 1 | [Browse →](./automation/) |
| ⛓️ **Crypto** | 1 | [Browse →](./crypto/) |
| 💳 **Payments** | 1 | [Browse →](./payments/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [sickn33/agentic-awesome-skills](./orchestration/sickn33-agentic-awesome-skills.md) | ⭐ 42.7k | Orchestration |
| 2 | [headroomlabs-ai/headroom](./orchestration/headroomlabs-ai-headroom.md) | ⭐ 58.2k | Orchestration |
| 3 | [n8n-io/n8n](./mcp/n8n-io-n8n.md) | ⭐ 195.9k | Mcp |
| 4 | [BerriAI/litellm](./orchestration/berriai-litellm.md) | ⭐ 53.1k | Orchestration |
| 5 | [can1357/oh-my-pi](./mcp/can1357-oh-my-pi.md) | ⭐ 17.1k | Mcp |
| 6 | [strands-agents/harness-sdk](./orchestration/strands-agents-harness-sdk.md) | ⭐ 6.5k | Orchestration |
| 7 | [ThinkInAIXYZ/deepchat](./orchestration/thinkinaixyz-deepchat.md) | ⭐ 6.1k | Orchestration |
| 8 | [esengine/DeepSeek-Reasonix](./orchestration/esengine-deepseek-reasonix.md) | ⭐ 26.6k | Orchestration |
| 9 | [google/adk-python](./orchestration/google-adk-python.md) | ⭐ 20.5k | Orchestration |
| 10 | [nexu-io/open-design](./orchestration/nexu-io-open-design.md) | ⭐ 76.9k | Orchestration |

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
