# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **8908** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 3425 | [Browse →](./aiml/) |
| 📦 **Misc** | 1653 | [Browse →](./misc/) |
| 🎨 **Frontend** | 896 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 745 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 515 | [Browse →](./backend/) |
| 🔧 **DevTools** | 512 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 319 | [Browse →](./crypto/) |
| 📊 **Data** | 192 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 177 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 120 | [Browse →](./mobile/) |
| 💳 **Payments** | 113 | [Browse →](./payments/) |
| 📈 **Trading** | 91 | [Browse →](./trading/) |
| 🔐 **Security** | 81 | [Browse →](./security/) |
| ✨ **Design** | 30 | [Browse →](./design/) |
| 🎯 **Product** | 22 | [Browse →](./product/) |
| 🏷️ **Marketing** | 17 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [webpack/webpack](./frontend/webpack-webpack.md) | ⭐ 65.8k | Frontend |
| 2 | [zeek/zeek](./security/zeek-zeek.md) | ⭐ 7.6k | Security |
| 3 | [PrivateBin/PrivateBin](./crypto/privatebin-privatebin.md) | ⭐ 8.2k | Crypto |
| 4 | [sunface/rust-course](./aiml/sunface-rust-course.md) | ⭐ 30.3k | AI/ML |
| 5 | [clap-rs/clap](./misc/clap-rs-clap.md) | ⭐ 16.3k | Misc |
| 6 | [Lissy93/dashy](./frontend/lissy93-dashy.md) | ⭐ 24.8k | Frontend |
| 7 | [marimo-team/marimo](./aiml/marimo-team-marimo.md) | ⭐ 20.7k | AI/ML |
| 8 | [dr5hn/countries-states-cities-database](./aiml/dr5hn-countries-states-cities-database.md) | ⭐ 9.5k | AI/ML |
| 9 | [xtermjs/xterm.js](./misc/xtermjs-xterm.js.md) | ⭐ 20.4k | Misc |
| 10 | [wolfpld/tracy](./misc/wolfpld-tracy.md) | ⭐ 15.7k | Misc |

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
