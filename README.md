# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **7676** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2954 | [Browse →](./aiml/) |
| 📦 **Misc** | 1427 | [Browse →](./misc/) |
| 🎨 **Frontend** | 772 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 660 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 436 | [Browse →](./backend/) |
| 🔧 **DevTools** | 429 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 259 | [Browse →](./crypto/) |
| 📊 **Data** | 168 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 144 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 112 | [Browse →](./mobile/) |
| 💳 **Payments** | 106 | [Browse →](./payments/) |
| 📈 **Trading** | 79 | [Browse →](./trading/) |
| 🔐 **Security** | 72 | [Browse →](./security/) |
| ✨ **Design** | 26 | [Browse →](./design/) |
| 🎯 **Product** | 20 | [Browse →](./product/) |
| 🏷️ **Marketing** | 12 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [yusufkaraaslan/Skill_Seekers](./aiml/yusufkaraaslan-skill-seekers.md) | ⭐ 13.1k | AI/ML |
| 2 | [wshobson/agents](./orchestration/wshobson-agents.md) | ⭐ 34.4k | Orchestration |
| 3 | [sharkdp/fd](./devtools/sharkdp-fd.md) | ⭐ 42.7k | DevTools |
| 4 | [NousResearch/hermes-agent](./aiml/nousresearch-hermes-agent.md) | ⭐ 118.2k | AI/ML |
| 5 | [micro-editor/micro](./frontend/micro-editor-micro.md) | ⭐ 28.5k | Frontend |
| 6 | [iced-rs/iced](./orchestration/iced-rs-iced.md) | ⭐ 30.3k | Orchestration |
| 7 | [zeromicro/go-zero](./aiml/zeromicro-go-zero.md) | ⭐ 33k | AI/ML |
| 8 | [rapidsai/cudf](./aiml/rapidsai-cudf.md) | ⭐ 9.6k | AI/ML |
| 9 | [datahub-project/datahub](./aiml/datahub-project-datahub.md) | ⭐ 11.8k | AI/ML |
| 10 | [Yeachan-Heo/oh-my-claudecode](./orchestration/yeachan-heo-oh-my-claudecode.md) | ⭐ 31.4k | Orchestration |

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
