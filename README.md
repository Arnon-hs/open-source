# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **17005** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 6323 | [Browse →](./aiml/) |
| 📦 **Misc** | 3566 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1679 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1218 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 1045 | [Browse →](./backend/) |
| 🔧 **DevTools** | 994 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 570 | [Browse →](./crypto/) |
| 📊 **Data** | 392 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 370 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 237 | [Browse →](./mobile/) |
| 📈 **Trading** | 171 | [Browse →](./trading/) |
| 💳 **Payments** | 170 | [Browse →](./payments/) |
| 🔐 **Security** | 145 | [Browse →](./security/) |
| ✨ **Design** | 57 | [Browse →](./design/) |
| 🎯 **Product** | 36 | [Browse →](./product/) |
| 🏷️ **Marketing** | 32 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [cython/cython](./data/cython-cython.md) | ⭐ 10.7k | Data |
| 2 | [apache/beam](./data/apache-beam.md) | ⭐ 8.6k | Data |
| 3 | [zeek/zeek](./security/zeek-zeek.md) | ⭐ 7.6k | Security |
| 4 | [meshery/meshery](./frontend/meshery-meshery.md) | ⭐ 10.2k | Frontend |
| 5 | [WinMerge/winmerge](./misc/winmerge-winmerge.md) | ⭐ 8.8k | Misc |
| 6 | [HKUDS/nanobot](./aiml/hkuds-nanobot.md) | ⭐ 41.7k | AI/ML |
| 7 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 8 | [ludwig-ai/ludwig](./aiml/ludwig-ai-ludwig.md) | ⭐ 11.7k | AI/ML |
| 9 | [avajs/ava](./devtools/avajs-ava.md) | ⭐ 20.8k | DevTools |
| 10 | [grpc/grpc-go](./backend/grpc-grpc-go.md) | ⭐ 22.9k | Backend |

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
