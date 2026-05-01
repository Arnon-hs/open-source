# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **13580** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 5147 | [Browse →](./aiml/) |
| 📦 **Misc** | 2693 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1319 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1029 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 834 | [Browse →](./backend/) |
| 🔧 **DevTools** | 809 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 482 | [Browse →](./crypto/) |
| 📊 **Data** | 309 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 296 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 166 | [Browse →](./mobile/) |
| 💳 **Payments** | 147 | [Browse →](./payments/) |
| 📈 **Trading** | 140 | [Browse →](./trading/) |
| 🔐 **Security** | 113 | [Browse →](./security/) |
| ✨ **Design** | 42 | [Browse →](./design/) |
| 🎯 **Product** | 28 | [Browse →](./product/) |
| 🏷️ **Marketing** | 26 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [CherryHQ/cherry-studio](./aiml/cherryhq-cherry-studio.md) | ⭐ 44.9k | AI/ML |
| 2 | [playcanvas/engine](./frontend/playcanvas-engine.md) | ⭐ 14.8k | Frontend |
| 3 | [RIOT-OS/RIOT](./misc/riot-os-riot.md) | ⭐ 5.7k | Misc |
| 4 | [dkhamsing/open-source-ios-apps](./frontend/dkhamsing-open-source-ios-apps.md) | ⭐ 50.1k | Frontend |
| 5 | [argoproj/argo-cd](./devopsinfra/argoproj-argo-cd.md) | ⭐ 22.8k | DevOps & Infra |
| 6 | [apache/tvm](./misc/apache-tvm.md) | ⭐ 13.3k | Misc |
| 7 | [thedotmack/claude-mem](./orchestration/thedotmack-claude-mem.md) | ⭐ 70.6k | Orchestration |
| 8 | [Stirling-Tools/Stirling-PDF](./devopsinfra/stirling-tools-stirling-pdf.md) | ⭐ 78k | DevOps & Infra |
| 9 | [gravitational/teleport](./backend/gravitational-teleport.md) | ⭐ 20.2k | Backend |
| 10 | [Yeachan-Heo/oh-my-claudecode](./orchestration/yeachan-heo-oh-my-claudecode.md) | ⭐ 32.1k | Orchestration |

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
