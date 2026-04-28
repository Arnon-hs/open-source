# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **9664** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 3721 | [Browse →](./aiml/) |
| 📦 **Misc** | 1805 | [Browse →](./misc/) |
| 🎨 **Frontend** | 966 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 799 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 571 | [Browse →](./backend/) |
| 🔧 **DevTools** | 555 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 344 | [Browse →](./crypto/) |
| 📊 **Data** | 208 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 192 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 127 | [Browse →](./mobile/) |
| 💳 **Payments** | 115 | [Browse →](./payments/) |
| 📈 **Trading** | 98 | [Browse →](./trading/) |
| 🔐 **Security** | 89 | [Browse →](./security/) |
| ✨ **Design** | 32 | [Browse →](./design/) |
| 🎯 **Product** | 24 | [Browse →](./product/) |
| 🏷️ **Marketing** | 18 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [temporalio/temporal](./orchestration/temporalio-temporal.md) | ⭐ 19.9k | Orchestration |
| 2 | [alibaba/MNN](./aiml/alibaba-mnn.md) | ⭐ 15k | AI/ML |
| 3 | [danny-avila/LibreChat](./orchestration/danny-avila-librechat.md) | ⭐ 36.2k | Orchestration |
| 4 | [hesreallyhim/awesome-claude-code](./orchestration/hesreallyhim-awesome-claude-code.md) | ⭐ 41.6k | Orchestration |
| 5 | [googleworkspace/cli](./orchestration/googleworkspace-cli.md) | ⭐ 25.5k | Orchestration |
| 6 | [labring/FastGPT](./orchestration/labring-fastgpt.md) | ⭐ 27.9k | Orchestration |
| 7 | [foundry-rs/foundry](./crypto/foundry-rs-foundry.md) | ⭐ 10.3k | Crypto |
| 8 | [JackChen-me/open-multi-agent](./orchestration/jackchen-me-open-multi-agent.md) | ⭐ 5.9k | Orchestration |
| 9 | [spree/spree](./backend/spree-spree.md) | ⭐ 15.4k | Backend |
| 10 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |

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
