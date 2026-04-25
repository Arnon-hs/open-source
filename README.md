# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **4782** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1856 | [Browse →](./aiml/) |
| 📦 **Misc** | 758 | [Browse →](./misc/) |
| 🎨 **Frontend** | 477 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 449 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 287 | [Browse →](./backend/) |
| 🔧 **DevTools** | 255 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 177 | [Browse →](./crypto/) |
| 📊 **Data** | 122 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 115 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 73 | [Browse →](./payments/) |
| 📱 **Mobile** | 66 | [Browse →](./mobile/) |
| 📈 **Trading** | 54 | [Browse →](./trading/) |
| 🔐 **Security** | 52 | [Browse →](./security/) |
| ✨ **Design** | 19 | [Browse →](./design/) |
| 🎯 **Product** | 16 | [Browse →](./product/) |
| 🏷️ **Marketing** | 6 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [YouMind-OpenLab/awesome-nano-banana-pro-prompts](./aiml/youmind-openlab-awesome-nano-banana-pro-prompts.md) | ⭐ 11.5k | AI/ML |
| 2 | [dyad-sh/dyad](./aiml/dyad-sh-dyad.md) | ⭐ 20.2k | AI/ML |
| 3 | [dgtlmoon/changedetection.io](./backend/dgtlmoon-changedetection.io.md) | ⭐ 31.2k | Backend |
| 4 | [volcano-sh/volcano](./aiml/volcano-sh-volcano.md) | ⭐ 5.5k | AI/ML |
| 5 | [raysan5/raylib](./mobile/raysan5-raylib.md) | ⭐ 32.5k | Mobile |
| 6 | [dubinc/dub](./aiml/dubinc-dub.md) | ⭐ 23.4k | AI/ML |
| 7 | [huggingface/chat-ui](./aiml/huggingface-chat-ui.md) | ⭐ 10.7k | AI/ML |
| 8 | [apache/superset](./frontend/apache-superset.md) | ⭐ 72.6k | Frontend |
| 9 | [wilsonfreitas/awesome-quant](./trading/wilsonfreitas-awesome-quant.md) | ⭐ 25.8k | Trading |
| 10 | [google/adk-python](./orchestration/google-adk-python.md) | ⭐ 19.3k | Orchestration |

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
