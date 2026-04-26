# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **7521** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2887 | [Browse →](./aiml/) |
| 📦 **Misc** | 1390 | [Browse →](./misc/) |
| 🎨 **Frontend** | 754 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 651 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 428 | [Browse →](./backend/) |
| 🔧 **DevTools** | 421 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 256 | [Browse →](./crypto/) |
| 📊 **Data** | 169 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 143 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 112 | [Browse →](./mobile/) |
| 💳 **Payments** | 105 | [Browse →](./payments/) |
| 📈 **Trading** | 76 | [Browse →](./trading/) |
| 🔐 **Security** | 72 | [Browse →](./security/) |
| ✨ **Design** | 26 | [Browse →](./design/) |
| 🎯 **Product** | 20 | [Browse →](./product/) |
| 🏷️ **Marketing** | 11 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [openscad/openscad](./misc/openscad-openscad.md) | ⭐ 9.3k | Misc |
| 2 | [fatedier/frp](./backend/fatedier-frp.md) | ⭐ 106.1k | Backend |
| 3 | [avajs/ava](./devtools/avajs-ava.md) | ⭐ 20.8k | DevTools |
| 4 | [calcom/cal.diy](./aiml/calcom-cal.diy.md) | ⭐ 42.1k | AI/ML |
| 5 | [bluewave-labs/Checkmate](./frontend/bluewave-labs-checkmate.md) | ⭐ 9.7k | Frontend |
| 6 | [mbadolato/iTerm2-Color-Schemes](./misc/mbadolato-iterm2-color-schemes.md) | ⭐ 26.8k | Misc |
| 7 | [Kong/insomnia](./aiml/kong-insomnia.md) | ⭐ 38.4k | AI/ML |
| 8 | [saleor/saleor](./payments/saleor-saleor.md) | ⭐ 22.9k | Payments |
| 9 | [tikv/tikv](./data/tikv-tikv.md) | ⭐ 16.6k | Data |
| 10 | [rustfs/rustfs](./aiml/rustfs-rustfs.md) | ⭐ 26.5k | AI/ML |

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
