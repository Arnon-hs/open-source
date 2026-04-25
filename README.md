# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **5935** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2274 | [Browse →](./aiml/) |
| 📦 **Misc** | 1008 | [Browse →](./misc/) |
| 🎨 **Frontend** | 588 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 543 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 350 | [Browse →](./backend/) |
| 🔧 **DevTools** | 333 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 219 | [Browse →](./crypto/) |
| 📊 **Data** | 142 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 127 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 89 | [Browse →](./mobile/) |
| 💳 **Payments** | 84 | [Browse →](./payments/) |
| 🔐 **Security** | 63 | [Browse →](./security/) |
| 📈 **Trading** | 63 | [Browse →](./trading/) |
| ✨ **Design** | 24 | [Browse →](./design/) |
| 🎯 **Product** | 19 | [Browse →](./product/) |
| 🏷️ **Marketing** | 9 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [azerothcore/azerothcore-wotlk](./backend/azerothcore-azerothcore-wotlk.md) | ⭐ 8.2k | Backend |
| 2 | [huggingface/datasets](./aiml/huggingface-datasets.md) | ⭐ 21.5k | AI/ML |
| 3 | [firebase/firebase-ios-sdk](./aiml/firebase-firebase-ios-sdk.md) | ⭐ 6.6k | AI/ML |
| 4 | [siteboon/claudecodeui](./aiml/siteboon-claudecodeui.md) | ⭐ 10.2k | AI/ML |
| 5 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 6 | [microsoft/Web-Dev-For-Beginners](./aiml/microsoft-web-dev-for-beginners.md) | ⭐ 95.7k | AI/ML |
| 7 | [qdrant/qdrant](./aiml/qdrant-qdrant.md) | ⭐ 30.7k | AI/ML |
| 8 | [microsoft/ai-agents-for-beginners](./orchestration/microsoft-ai-agents-for-beginners.md) | ⭐ 59.3k | Orchestration |
| 9 | [steven2358/awesome-generative-ai](./aiml/steven2358-awesome-generative-ai.md) | ⭐ 11.9k | AI/ML |
| 10 | [future-architect/vuls](./aiml/future-architect-vuls.md) | ⭐ 12.1k | AI/ML |

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
