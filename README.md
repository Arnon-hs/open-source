# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **13783** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 5214 | [Browse →](./aiml/) |
| 📦 **Misc** | 2744 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1340 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1036 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 846 | [Browse →](./backend/) |
| 🔧 **DevTools** | 822 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 485 | [Browse →](./crypto/) |
| 📊 **Data** | 317 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 301 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 172 | [Browse →](./mobile/) |
| 💳 **Payments** | 150 | [Browse →](./payments/) |
| 📈 **Trading** | 141 | [Browse →](./trading/) |
| 🔐 **Security** | 116 | [Browse →](./security/) |
| ✨ **Design** | 44 | [Browse →](./design/) |
| 🎯 **Product** | 29 | [Browse →](./product/) |
| 🏷️ **Marketing** | 26 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [jestjs/jest](./aiml/jestjs-jest.md) | ⭐ 45.3k | AI/ML |
| 2 | [VoltAgent/awesome-design-md](./aiml/voltagent-awesome-design-md.md) | ⭐ 69.1k | AI/ML |
| 3 | [influxdata/influxdb](./frontend/influxdata-influxdb.md) | ⭐ 31.5k | Frontend |
| 4 | [Dokploy/dokploy](./frontend/dokploy-dokploy.md) | ⭐ 33.7k | Frontend |
| 5 | [CorentinTh/it-tools](./frontend/corentinth-it-tools.md) | ⭐ 38.3k | Frontend |
| 6 | [argoproj/argo-cd](./devopsinfra/argoproj-argo-cd.md) | ⭐ 22.8k | DevOps & Infra |
| 7 | [Stirling-Tools/Stirling-PDF](./devopsinfra/stirling-tools-stirling-pdf.md) | ⭐ 78.1k | DevOps & Infra |
| 8 | [xbmc/xbmc](./aiml/xbmc-xbmc.md) | ⭐ 20.7k | AI/ML |
| 9 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 10 | [iii-hq/iii](./aiml/iii-hq-iii.md) | ⭐ 15.5k | AI/ML |

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
