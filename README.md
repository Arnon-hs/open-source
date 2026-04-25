# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **6150** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2366 | [Browse →](./aiml/) |
| 📦 **Misc** | 1057 | [Browse →](./misc/) |
| 🎨 **Frontend** | 611 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 556 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 361 | [Browse →](./backend/) |
| 🔧 **DevTools** | 342 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 221 | [Browse →](./crypto/) |
| 📊 **Data** | 144 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 127 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 94 | [Browse →](./mobile/) |
| 💳 **Payments** | 90 | [Browse →](./payments/) |
| 🔐 **Security** | 66 | [Browse →](./security/) |
| 📈 **Trading** | 63 | [Browse →](./trading/) |
| ✨ **Design** | 24 | [Browse →](./design/) |
| 🎯 **Product** | 19 | [Browse →](./product/) |
| 🏷️ **Marketing** | 9 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [ngosang/trackerslist](./misc/ngosang-trackerslist.md) | ⭐ 53.6k | Misc |
| 2 | [projectdiscovery/nuclei](./aiml/projectdiscovery-nuclei.md) | ⭐ 28.1k | AI/ML |
| 3 | [casdoor/casdoor](./aiml/casdoor-casdoor.md) | ⭐ 13.5k | AI/ML |
| 4 | [astral-sh/ruff](./frontend/astral-sh-ruff.md) | ⭐ 47.2k | Frontend |
| 5 | [matplotlib/matplotlib](./data/matplotlib-matplotlib.md) | ⭐ 22.7k | Data |
| 6 | [alam00000/bentopdf](./devopsinfra/alam00000-bentopdf.md) | ⭐ 12.9k | DevOps & Infra |
| 7 | [alibaba/nacos](./aiml/alibaba-nacos.md) | ⭐ 32.9k | AI/ML |
| 8 | [flybywiresim/aircraft](./aiml/flybywiresim-aircraft.md) | ⭐ 5.4k | AI/ML |
| 9 | [labstack/echo](./backend/labstack-echo.md) | ⭐ 32.3k | Backend |
| 10 | [siteboon/claudecodeui](./aiml/siteboon-claudecodeui.md) | ⭐ 10.2k | AI/ML |

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
