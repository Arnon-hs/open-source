# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **3899** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1573 | [Browse →](./aiml/) |
| 📦 **Misc** | 616 | [Browse →](./misc/) |
| 🧩 **Orchestration** | 394 | [Browse →](./orchestration/) |
| 🎨 **Frontend** | 383 | [Browse →](./frontend/) |
| ⚙️ **Backend** | 202 | [Browse →](./backend/) |
| 🔧 **DevTools** | 202 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 156 | [Browse →](./crypto/) |
| 📊 **Data** | 86 | [Browse →](./data/) |
| 💳 **Payments** | 84 | [Browse →](./payments/) |
| 📈 **Trading** | 55 | [Browse →](./trading/) |
| 🚀 **DevOps & Infra** | 50 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 40 | [Browse →](./mobile/) |
| 🔐 **Security** | 33 | [Browse →](./security/) |
| ✨ **Design** | 11 | [Browse →](./design/) |
| 🎯 **Product** | 10 | [Browse →](./product/) |
| 🏷️ **Marketing** | 4 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [Narcooo/inkos](./aiml/narcooo-inkos.md) | ⭐ 5.9k | AI/ML |
| 2 | [yzhao062/pyod](./orchestration/yzhao062-pyod.md) | ⭐ 9.8k | Orchestration |
| 3 | [starship/starship](./misc/starship-starship.md) | ⭐ 57.3k | Misc |
| 4 | [hwdsl2/docker-ipsec-vpn-server](./backend/hwdsl2-docker-ipsec-vpn-server.md) | ⭐ 7.1k | Backend |
| 5 | [eosphoros-ai/DB-GPT](./aiml/eosphoros-ai-db-gpt.md) | ⭐ 18.7k | AI/ML |
| 6 | [StarRocks/starrocks](./devtools/starrocks-starrocks.md) | ⭐ 11.7k | DevTools |
| 7 | [stride3d/stride](./misc/stride3d-stride.md) | ⭐ 7.6k | Misc |
| 8 | [tikv/tikv](./data/tikv-tikv.md) | ⭐ 16.7k | Data |
| 9 | [mcp-use/mcp-use](./aiml/mcp-use-mcp-use.md) | ⭐ 9.9k | AI/ML |
| 10 | [arc53/DocsGPT](./aiml/arc53-docsgpt.md) | ⭐ 17.9k | AI/ML |

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
