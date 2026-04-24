# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **3355** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1279 | [Browse →](./aiml/) |
| 📦 **Misc** | 525 | [Browse →](./misc/) |
| 🎨 **Frontend** | 361 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 306 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 209 | [Browse →](./backend/) |
| 🔧 **DevTools** | 177 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 136 | [Browse →](./crypto/) |
| 📊 **Data** | 92 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 78 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 47 | [Browse →](./payments/) |
| 📱 **Mobile** | 45 | [Browse →](./mobile/) |
| 📈 **Trading** | 36 | [Browse →](./trading/) |
| 🔐 **Security** | 35 | [Browse →](./security/) |
| ✨ **Design** | 13 | [Browse →](./design/) |
| 🎯 **Product** | 11 | [Browse →](./product/) |
| 🏷️ **Marketing** | 5 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [rclone/rclone](./aiml/rclone-rclone.md) | ⭐ 56.8k | AI/ML |
| 2 | [RT-Thread/rt-thread](./aiml/rt-thread-rt-thread.md) | ⭐ 11.9k | AI/ML |
| 3 | [pwndbg/pwndbg](./misc/pwndbg-pwndbg.md) | ⭐ 10.4k | Misc |
| 4 | [duplicati/duplicati](./aiml/duplicati-duplicati.md) | ⭐ 14.5k | AI/ML |
| 5 | [photoprism/photoprism](./aiml/photoprism-photoprism.md) | ⭐ 39.6k | AI/ML |
| 6 | [mbadolato/iTerm2-Color-Schemes](./misc/mbadolato-iterm2-color-schemes.md) | ⭐ 26.8k | Misc |
| 7 | [mlflow/mlflow](./orchestration/mlflow-mlflow.md) | ⭐ 25.5k | Orchestration |
| 8 | [modelscope/ms-swift](./aiml/modelscope-ms-swift.md) | ⭐ 13.9k | AI/ML |
| 9 | [redisson/redisson](./frontend/redisson-redisson.md) | ⭐ 24.3k | Frontend |
| 10 | [openemr/openemr](./misc/openemr-openemr.md) | ⭐ 5.1k | Misc |

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
