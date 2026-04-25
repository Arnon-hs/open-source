# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **5467** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2133 | [Browse →](./aiml/) |
| 📦 **Misc** | 891 | [Browse →](./misc/) |
| 🎨 **Frontend** | 539 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 516 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 319 | [Browse →](./backend/) |
| 🔧 **DevTools** | 301 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 195 | [Browse →](./crypto/) |
| 📊 **Data** | 133 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 121 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 79 | [Browse →](./payments/) |
| 📱 **Mobile** | 79 | [Browse →](./mobile/) |
| 📈 **Trading** | 59 | [Browse →](./trading/) |
| 🔐 **Security** | 55 | [Browse →](./security/) |
| ✨ **Design** | 23 | [Browse →](./design/) |
| 🎯 **Product** | 17 | [Browse →](./product/) |
| 🏷️ **Marketing** | 7 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [bin456789/reinstall](./devtools/bin456789-reinstall.md) | ⭐ 11.6k | DevTools |
| 2 | [pear-devs/pear-desktop](./misc/pear-devs-pear-desktop.md) | ⭐ 31.4k | Misc |
| 3 | [XTLS/Xray-core](./misc/xtls-xray-core.md) | ⭐ 37.8k | Misc |
| 4 | [JunkFood02/Seal](./mobile/junkfood02-seal.md) | ⭐ 25.9k | Mobile |
| 5 | [invoke-ai/InvokeAI](./aiml/invoke-ai-invokeai.md) | ⭐ 27k | AI/ML |
| 6 | [googleapis/mcp-toolbox](./aiml/googleapis-mcp-toolbox.md) | ⭐ 14.8k | AI/ML |
| 7 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 8 | [arendst/Tasmota](./frontend/arendst-tasmota.md) | ⭐ 24.3k | Frontend |
| 9 | [JetBrains/kotlin](./aiml/jetbrains-kotlin.md) | ⭐ 52.6k | AI/ML |
| 10 | [docmost/docmost](./misc/docmost-docmost.md) | ⭐ 19.9k | Misc |

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
