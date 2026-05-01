# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **13149** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 5001 | [Browse →](./aiml/) |
| 📦 **Misc** | 2587 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1281 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1006 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 801 | [Browse →](./backend/) |
| 🔧 **DevTools** | 780 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 472 | [Browse →](./crypto/) |
| 📊 **Data** | 298 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 282 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 161 | [Browse →](./mobile/) |
| 💳 **Payments** | 140 | [Browse →](./payments/) |
| 📈 **Trading** | 136 | [Browse →](./trading/) |
| 🔐 **Security** | 111 | [Browse →](./security/) |
| ✨ **Design** | 41 | [Browse →](./design/) |
| 🎯 **Product** | 27 | [Browse →](./product/) |
| 🏷️ **Marketing** | 25 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [dotnet/efcore](./data/dotnet-efcore.md) | ⭐ 14.6k | Data |
| 2 | [JuliusBrussee/caveman](./aiml/juliusbrussee-caveman.md) | ⭐ 51.5k | AI/ML |
| 3 | [TykTechnologies/tyk](./backend/tyktechnologies-tyk.md) | ⭐ 10.7k | Backend |
| 4 | [caddyserver/caddy](./backend/caddyserver-caddy.md) | ⭐ 72k | Backend |
| 5 | [birobirobiro/awesome-shadcn-ui](./frontend/birobirobiro-awesome-shadcn-ui.md) | ⭐ 19.4k | Frontend |
| 6 | [langchain-ai/langchain](./orchestration/langchain-ai-langchain.md) | ⭐ 135.5k | Orchestration |
| 7 | [janhq/jan](./aiml/janhq-jan.md) | ⭐ 42.3k | AI/ML |
| 8 | [CoplayDev/unity-mcp](./aiml/coplaydev-unity-mcp.md) | ⭐ 9.1k | AI/ML |
| 9 | [openshift/origin](./aiml/openshift-origin.md) | ⭐ 8.6k | AI/ML |
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
