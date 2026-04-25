# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **4491** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1734 | [Browse →](./aiml/) |
| 📦 **Misc** | 708 | [Browse →](./misc/) |
| 🎨 **Frontend** | 456 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 427 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 268 | [Browse →](./backend/) |
| 🔧 **DevTools** | 245 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 172 | [Browse →](./crypto/) |
| 📊 **Data** | 116 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 105 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 66 | [Browse →](./payments/) |
| 📱 **Mobile** | 62 | [Browse →](./mobile/) |
| 📈 **Trading** | 48 | [Browse →](./trading/) |
| 🔐 **Security** | 46 | [Browse →](./security/) |
| ✨ **Design** | 18 | [Browse →](./design/) |
| 🎯 **Product** | 14 | [Browse →](./product/) |
| 🏷️ **Marketing** | 6 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [linshenkx/prompt-optimizer](./aiml/linshenkx-prompt-optimizer.md) | ⭐ 26.8k | AI/ML |
| 2 | [nautechsystems/nautilus_trader](./crypto/nautechsystems-nautilus-trader.md) | ⭐ 22.3k | Crypto |
| 3 | [oppia/oppia](./misc/oppia-oppia.md) | ⭐ 6.7k | Misc |
| 4 | [langbot-app/LangBot](./aiml/langbot-app-langbot.md) | ⭐ 15.9k | AI/ML |
| 5 | [harvard-edge/cs249r_book](./aiml/harvard-edge-cs249r-book.md) | ⭐ 23.8k | AI/ML |
| 6 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 7 | [janhq/jan](./aiml/janhq-jan.md) | ⭐ 42.1k | AI/ML |
| 8 | [Skyvern-AI/skyvern](./aiml/skyvern-ai-skyvern.md) | ⭐ 21.4k | AI/ML |
| 9 | [VictoriaMetrics/VictoriaMetrics](./data/victoriametrics-victoriametrics.md) | ⭐ 16.9k | Data |
| 10 | [web-platform-tests/wpt](./aiml/web-platform-tests-wpt.md) | ⭐ 5.9k | AI/ML |

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
