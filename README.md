# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **6444** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2472 | [Browse →](./aiml/) |
| 📦 **Misc** | 1123 | [Browse →](./misc/) |
| 🎨 **Frontend** | 637 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 583 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 374 | [Browse →](./backend/) |
| 🔧 **DevTools** | 361 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 227 | [Browse →](./crypto/) |
| 📊 **Data** | 152 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 136 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 99 | [Browse →](./mobile/) |
| 💳 **Payments** | 92 | [Browse →](./payments/) |
| 🔐 **Security** | 68 | [Browse →](./security/) |
| 📈 **Trading** | 67 | [Browse →](./trading/) |
| ✨ **Design** | 25 | [Browse →](./design/) |
| 🎯 **Product** | 19 | [Browse →](./product/) |
| 🏷️ **Marketing** | 9 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [stride3d/stride](./misc/stride3d-stride.md) | ⭐ 7.6k | Misc |
| 2 | [quay/clair](./aiml/quay-clair.md) | ⭐ 11k | AI/ML |
| 3 | [allinurl/goaccess](./frontend/allinurl-goaccess.md) | ⭐ 20.5k | Frontend |
| 4 | [biomejs/biome](./aiml/biomejs-biome.md) | ⭐ 24.5k | AI/ML |
| 5 | [FlowiseAI/Flowise](./orchestration/flowiseai-flowise.md) | ⭐ 52.3k | Orchestration |
| 6 | [OpenHands/OpenHands](./aiml/openhands-openhands.md) | ⭐ 72.1k | AI/ML |
| 7 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 8 | [apache/spark](./data/apache-spark.md) | ⭐ 43.2k | Data |
| 9 | [giampaolo/psutil](./misc/giampaolo-psutil.md) | ⭐ 11.2k | Misc |
| 10 | [appsmithorg/appsmith](./frontend/appsmithorg-appsmith.md) | ⭐ 39.7k | Frontend |

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
