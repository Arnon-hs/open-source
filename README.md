# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **4179** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1697 | [Browse →](./aiml/) |
| 📦 **Misc** | 665 | [Browse →](./misc/) |
| 🧩 **Orchestration** | 420 | [Browse →](./orchestration/) |
| 🎨 **Frontend** | 410 | [Browse →](./frontend/) |
| 🔧 **DevTools** | 221 | [Browse →](./devtools/) |
| ⚙️ **Backend** | 215 | [Browse →](./backend/) |
| ⛓️ **Crypto** | 162 | [Browse →](./crypto/) |
| 📊 **Data** | 90 | [Browse →](./data/) |
| 💳 **Payments** | 86 | [Browse →](./payments/) |
| 📈 **Trading** | 56 | [Browse →](./trading/) |
| 🚀 **DevOps & Infra** | 51 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 45 | [Browse →](./mobile/) |
| 🔐 **Security** | 35 | [Browse →](./security/) |
| ✨ **Design** | 12 | [Browse →](./design/) |
| 🎯 **Product** | 10 | [Browse →](./product/) |
| 🏷️ **Marketing** | 4 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [jnMetaCode/agency-agents-zh](./crypto/jnmetacode-agency-agents-zh.md) | ⭐ 10.3k | Crypto |
| 2 | [fastlane/fastlane](./frontend/fastlane-fastlane.md) | ⭐ 41.5k | Frontend |
| 3 | [mrexodia/ida-pro-mcp](./aiml/mrexodia-ida-pro-mcp.md) | ⭐ 8.3k | AI/ML |
| 4 | [junit-team/junit-framework](./devtools/junit-team-junit-framework.md) | ⭐ 7k | DevTools |
| 5 | [rustdesk/rustdesk](./mobile/rustdesk-rustdesk.md) | ⭐ 113.8k | Mobile |
| 6 | [rohitg00/ai-engineering-from-scratch](./aiml/rohitg00-ai-engineering-from-scratch.md) | ⭐ 6.5k | AI/ML |
| 7 | [wailsapp/wails](./aiml/wailsapp-wails.md) | ⭐ 34k | AI/ML |
| 8 | [alibaba/nacos](./aiml/alibaba-nacos.md) | ⭐ 32.9k | AI/ML |
| 9 | [alibaba/arthas](./orchestration/alibaba-arthas.md) | ⭐ 37.3k | Orchestration |
| 10 | [open-multi-agent/open-multi-agent](./orchestration/open-multi-agent-open-multi-agent.md) | ⭐ 6.1k | Orchestration |

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
