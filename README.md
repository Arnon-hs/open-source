# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **8767** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 3386 | [Browse →](./aiml/) |
| 📦 **Misc** | 1611 | [Browse →](./misc/) |
| 🎨 **Frontend** | 886 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 738 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 509 | [Browse →](./backend/) |
| 🔧 **DevTools** | 501 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 310 | [Browse →](./crypto/) |
| 📊 **Data** | 187 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 175 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 118 | [Browse →](./mobile/) |
| 💳 **Payments** | 112 | [Browse →](./payments/) |
| 📈 **Trading** | 88 | [Browse →](./trading/) |
| 🔐 **Security** | 79 | [Browse →](./security/) |
| ✨ **Design** | 30 | [Browse →](./design/) |
| 🎯 **Product** | 22 | [Browse →](./product/) |
| 🏷️ **Marketing** | 15 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [Lissy93/dashy](./frontend/lissy93-dashy.md) | ⭐ 24.8k | Frontend |
| 2 | [ionic-team/capacitor](./aiml/ionic-team-capacitor.md) | ⭐ 15.5k | AI/ML |
| 3 | [formbricks/formbricks](./aiml/formbricks-formbricks.md) | ⭐ 12.1k | AI/ML |
| 4 | [marimo-team/marimo](./aiml/marimo-team-marimo.md) | ⭐ 20.7k | AI/ML |
| 5 | [wolfpld/tracy](./misc/wolfpld-tracy.md) | ⭐ 15.7k | Misc |
| 6 | [grafana/k6](./devtools/grafana-k6.md) | ⭐ 30.5k | DevTools |
| 7 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 8 | [MarlinFirmware/Marlin](./frontend/marlinfirmware-marlin.md) | ⭐ 17.4k | Frontend |
| 9 | [x-extends/vxe-table](./frontend/x-extends-vxe-table.md) | ⭐ 8.6k | Frontend |
| 10 | [elizaOS/eliza](./crypto/elizaos-eliza.md) | ⭐ 18.3k | Crypto |

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
