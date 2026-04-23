# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **2411** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 902 | [Browse →](./aiml/) |
| 📦 **Misc** | 398 | [Browse →](./misc/) |
| 🎨 **Frontend** | 259 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 213 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 158 | [Browse →](./backend/) |
| 🔧 **DevTools** | 121 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 99 | [Browse →](./crypto/) |
| 📊 **Data** | 70 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 57 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 34 | [Browse →](./mobile/) |
| 💳 **Payments** | 29 | [Browse →](./payments/) |
| 🔐 **Security** | 26 | [Browse →](./security/) |
| 📈 **Trading** | 25 | [Browse →](./trading/) |
| 🎯 **Product** | 10 | [Browse →](./product/) |
| ✨ **Design** | 9 | [Browse →](./design/) |
| 🏷️ **Marketing** | 1 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [mdn/content](./aiml/mdn-content.md) | ⭐ 10.7k | AI/ML |
| 2 | [x64dbg/x64dbg](./security/x64dbg-x64dbg.md) | ⭐ 48.2k | Security |
| 3 | [run-llama/llama_index](./orchestration/run-llama-llama-index.md) | ⭐ 48.9k | Orchestration |
| 4 | [Wei-Shaw/claude-relay-service](./aiml/wei-shaw-claude-relay-service.md) | ⭐ 11.3k | AI/ML |
| 5 | [zhayujie/CowAgent](./orchestration/zhayujie-cowagent.md) | ⭐ 43.7k | Orchestration |
| 6 | [stashapp/stash](./misc/stashapp-stash.md) | ⭐ 12.2k | Misc |
| 7 | [cython/cython](./data/cython-cython.md) | ⭐ 10.7k | Data |
| 8 | [JackChen-me/open-multi-agent](./orchestration/jackchen-me-open-multi-agent.md) | ⭐ 5.9k | Orchestration |
| 9 | [HKUDS/DeepTutor](./orchestration/hkuds-deeptutor.md) | ⭐ 21.2k | Orchestration |
| 10 | [hiyouga/LlamaFactory](./trading/hiyouga-llamafactory.md) | ⭐ 70.5k | Trading |

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
