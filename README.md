# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **5618** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2239 | [Browse →](./aiml/) |
| 📦 **Misc** | 1022 | [Browse →](./misc/) |
| 🎨 **Frontend** | 559 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 515 | [Browse →](./orchestration/) |
| 🔧 **DevTools** | 298 | [Browse →](./devtools/) |
| ⚙️ **Backend** | 271 | [Browse →](./backend/) |
| ⛓️ **Crypto** | 203 | [Browse →](./crypto/) |
| 📊 **Data** | 132 | [Browse →](./data/) |
| 💳 **Payments** | 94 | [Browse →](./payments/) |
| 📈 **Trading** | 72 | [Browse →](./trading/) |
| 📱 **Mobile** | 68 | [Browse →](./mobile/) |
| 🚀 **DevOps & Infra** | 62 | [Browse →](./devopsinfra/) |
| 🔐 **Security** | 43 | [Browse →](./security/) |
| ✨ **Design** | 19 | [Browse →](./design/) |
| 🎯 **Product** | 13 | [Browse →](./product/) |
| 🏷️ **Marketing** | 8 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [ohmyzsh/ohmyzsh](./aiml/ohmyzsh-ohmyzsh.md) | ⭐ 186.9k | AI/ML |
| 2 | [streamlink/streamlink](./aiml/streamlink-streamlink.md) | ⭐ 11.5k | AI/ML |
| 3 | [hugohe3/ppt-master](./aiml/hugohe3-ppt-master.md) | ⭐ 14.1k | AI/ML |
| 4 | [JuliusBrussee/caveman](./aiml/juliusbrussee-caveman.md) | ⭐ 57.3k | AI/ML |
| 5 | [koodo-reader/koodo-reader](./aiml/koodo-reader-koodo-reader.md) | ⭐ 26.8k | AI/ML |
| 6 | [AI4Finance-Foundation/FinRobot](./aiml/ai4finance-foundation-finrobot.md) | ⭐ 6.9k | AI/ML |
| 7 | [joomla/joomla-cms](./aiml/joomla-joomla-cms.md) | ⭐ 5.1k | AI/ML |
| 8 | [evcc-io/evcc](./misc/evcc-io-evcc.md) | ⭐ 6.6k | Misc |
| 9 | [yairm210/Unciv](./aiml/yairm210-unciv.md) | ⭐ 10.3k | AI/ML |
| 10 | [hoochanlon/hamuleite](./misc/hoochanlon-hamuleite.md) | ⭐ 9.4k | Misc |

## 🚀 How it works

```mermaid
graph LR
  A[GitHub · HN · Reddit · PH] --> B[RepoScout]
  B --> C[Score · Dedupe · Categorize]
  C --> D[LLM Summarize]
  D --> E[PostgreSQL DB]
  D --> F[This Catalog]
```

1. **Discover** — 4 sources pulled in parallel
2. **Score** — weighted: stars, forks, recency, topics, source trust
3. **Categorize** — rule-based + LLM-assisted tagging
4. **Summarize** — concise bilingual (EN/RU) summaries via LLM
5. **Sync** — markdown committed here, metadata upserted to PostgreSQL

## 🛠️ Self-host

```bash
git clone https://github.com/kirbudilov01/reposearchengine
cp .env.example .env
# Set LLM_PROVIDER, CATALOG_REPO_PATH, DATABASE_URL, ...
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
