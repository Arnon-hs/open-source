# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **11380** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 4356 | [Browse →](./aiml/) |
| 📦 **Misc** | 2181 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1121 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 900 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 689 | [Browse →](./backend/) |
| 🔧 **DevTools** | 677 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 405 | [Browse →](./crypto/) |
| 📊 **Data** | 246 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 241 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 137 | [Browse →](./mobile/) |
| 💳 **Payments** | 125 | [Browse →](./payments/) |
| 📈 **Trading** | 117 | [Browse →](./trading/) |
| 🔐 **Security** | 102 | [Browse →](./security/) |
| ✨ **Design** | 37 | [Browse →](./design/) |
| 🎯 **Product** | 25 | [Browse →](./product/) |
| 🏷️ **Marketing** | 21 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [vnotex/vnote](./aiml/vnotex-vnote.md) | ⭐ 12.8k | AI/ML |
| 2 | [Wei-Shaw/sub2api](./aiml/wei-shaw-sub2api.md) | ⭐ 16.6k | AI/ML |
| 3 | [lichess-org/lila](./backend/lichess-org-lila.md) | ⭐ 18.1k | Backend |
| 4 | [opendataloader-project/opendataloader-pdf](./aiml/opendataloader-project-opendataloader-pdf.md) | ⭐ 19.7k | AI/ML |
| 5 | [LizardByte/Sunshine](./aiml/lizardbyte-sunshine.md) | ⭐ 36.5k | AI/ML |
| 6 | [evcc-io/evcc](./misc/evcc-io-evcc.md) | ⭐ 6.5k | Misc |
| 7 | [unslothai/unsloth](./aiml/unslothai-unsloth.md) | ⭐ 63.2k | AI/ML |
| 8 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 9 | [oven-sh/bun](./frontend/oven-sh-bun.md) | ⭐ 89.4k | Frontend |
| 10 | [hiyouga/LlamaFactory](./trading/hiyouga-llamafactory.md) | ⭐ 70.8k | Trading |

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
