# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **4871** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1895 | [Browse →](./aiml/) |
| 📦 **Misc** | 766 | [Browse →](./misc/) |
| 🎨 **Frontend** | 485 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 463 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 292 | [Browse →](./backend/) |
| 🔧 **DevTools** | 263 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 179 | [Browse →](./crypto/) |
| 📊 **Data** | 123 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 115 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 74 | [Browse →](./payments/) |
| 📱 **Mobile** | 68 | [Browse →](./mobile/) |
| 📈 **Trading** | 54 | [Browse →](./trading/) |
| 🔐 **Security** | 52 | [Browse →](./security/) |
| ✨ **Design** | 20 | [Browse →](./design/) |
| 🎯 **Product** | 16 | [Browse →](./product/) |
| 🏷️ **Marketing** | 6 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [jeecgboot/JeecgBoot](./orchestration/jeecgboot-jeecgboot.md) | ⭐ 46k | Orchestration |
| 2 | [weaviate/weaviate](./aiml/weaviate-weaviate.md) | ⭐ 16.1k | AI/ML |
| 3 | [Automattic/wp-calypso](./frontend/automattic-wp-calypso.md) | ⭐ 12.6k | Frontend |
| 4 | [SimplifyJobs/New-Grad-Positions](./trading/simplifyjobs-new-grad-positions.md) | ⭐ 16.8k | Trading |
| 5 | [sonic-pi-net/sonic-pi](./misc/sonic-pi-net-sonic-pi.md) | ⭐ 11.8k | Misc |
| 6 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 7 | [elizaOS/eliza](./crypto/elizaos-eliza.md) | ⭐ 18.2k | Crypto |
| 8 | [deepset-ai/haystack](./orchestration/deepset-ai-haystack.md) | ⭐ 25k | Orchestration |
| 9 | [farion1231/cc-switch](./aiml/farion1231-cc-switch.md) | ⭐ 51k | AI/ML |
| 10 | [microsoft/playwright](./backend/microsoft-playwright.md) | ⭐ 87.3k | Backend |

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
