# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **3597** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1372 | [Browse →](./aiml/) |
| 📦 **Misc** | 563 | [Browse →](./misc/) |
| 🎨 **Frontend** | 385 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 330 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 222 | [Browse →](./backend/) |
| 🔧 **DevTools** | 193 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 143 | [Browse →](./crypto/) |
| 📊 **Data** | 97 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 84 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 53 | [Browse →](./payments/) |
| 📱 **Mobile** | 49 | [Browse →](./mobile/) |
| 🔐 **Security** | 38 | [Browse →](./security/) |
| 📈 **Trading** | 38 | [Browse →](./trading/) |
| ✨ **Design** | 13 | [Browse →](./design/) |
| 🎯 **Product** | 12 | [Browse →](./product/) |
| 🏷️ **Marketing** | 5 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [gnuradio/gnuradio](./security/gnuradio-gnuradio.md) | ⭐ 6k | Security |
| 2 | [onnx/onnx](./aiml/onnx-onnx.md) | ⭐ 20.7k | AI/ML |
| 3 | [Dokploy/dokploy](./frontend/dokploy-dokploy.md) | ⭐ 33.4k | Frontend |
| 4 | [Raphire/Win11Debloat](./devtools/raphire-win11debloat.md) | ⭐ 45.3k | DevTools |
| 5 | [catboost/catboost](./aiml/catboost-catboost.md) | ⭐ 8.9k | AI/ML |
| 6 | [flameshot-org/flameshot](./frontend/flameshot-org-flameshot.md) | ⭐ 29.8k | Frontend |
| 7 | [juicedata/juicefs](./aiml/juicedata-juicefs.md) | ⭐ 13.5k | AI/ML |
| 8 | [charmbracelet/bubbletea](./frontend/charmbracelet-bubbletea.md) | ⭐ 41.8k | Frontend |
| 9 | [Graylog2/graylog2-server](./backend/graylog2-graylog2-server.md) | ⭐ 8k | Backend |
| 10 | [langbot-app/LangBot](./aiml/langbot-app-langbot.md) | ⭐ 15.9k | AI/ML |

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
