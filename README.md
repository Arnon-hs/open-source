# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **5381** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2098 | [Browse →](./aiml/) |
| 📦 **Misc** | 874 | [Browse →](./misc/) |
| 🎨 **Frontend** | 530 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 509 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 314 | [Browse →](./backend/) |
| 🔧 **DevTools** | 298 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 193 | [Browse →](./crypto/) |
| 📊 **Data** | 130 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 121 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 79 | [Browse →](./payments/) |
| 📱 **Mobile** | 76 | [Browse →](./mobile/) |
| 📈 **Trading** | 59 | [Browse →](./trading/) |
| 🔐 **Security** | 54 | [Browse →](./security/) |
| ✨ **Design** | 23 | [Browse →](./design/) |
| 🎯 **Product** | 17 | [Browse →](./product/) |
| 🏷️ **Marketing** | 6 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [pear-devs/pear-desktop](./misc/pear-devs-pear-desktop.md) | ⭐ 31.4k | Misc |
| 2 | [XTLS/Xray-core](./misc/xtls-xray-core.md) | ⭐ 37.8k | Misc |
| 3 | [cvxpy/cvxpy](./misc/cvxpy-cvxpy.md) | ⭐ 6.2k | Misc |
| 4 | [arendst/Tasmota](./frontend/arendst-tasmota.md) | ⭐ 24.3k | Frontend |
| 5 | [ChromeDevTools/chrome-devtools-mcp](./aiml/chromedevtools-chrome-devtools-mcp.md) | ⭐ 37.2k | AI/ML |
| 6 | [docmost/docmost](./misc/docmost-docmost.md) | ⭐ 19.9k | Misc |
| 7 | [microsoft/terminal](./misc/microsoft-terminal.md) | ⭐ 102.9k | Misc |
| 8 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 9 | [gnuradio/gnuradio](./security/gnuradio-gnuradio.md) | ⭐ 6k | Security |
| 10 | [psf/black](./misc/psf-black.md) | ⭐ 41.5k | Misc |

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
