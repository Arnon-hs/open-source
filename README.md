# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **5065** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2037 | [Browse →](./aiml/) |
| 📦 **Misc** | 885 | [Browse →](./misc/) |
| 🎨 **Frontend** | 508 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 475 | [Browse →](./orchestration/) |
| 🔧 **DevTools** | 269 | [Browse →](./devtools/) |
| ⚙️ **Backend** | 249 | [Browse →](./backend/) |
| ⛓️ **Crypto** | 185 | [Browse →](./crypto/) |
| 📊 **Data** | 116 | [Browse →](./data/) |
| 💳 **Payments** | 91 | [Browse →](./payments/) |
| 📈 **Trading** | 62 | [Browse →](./trading/) |
| 📱 **Mobile** | 59 | [Browse →](./mobile/) |
| 🚀 **DevOps & Infra** | 57 | [Browse →](./devopsinfra/) |
| 🔐 **Security** | 39 | [Browse →](./security/) |
| ✨ **Design** | 16 | [Browse →](./design/) |
| 🎯 **Product** | 11 | [Browse →](./product/) |
| 🏷️ **Marketing** | 6 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [PX4/PX4-Autopilot](./misc/px4-px4-autopilot.md) | ⭐ 11.7k | Misc |
| 2 | [clap-rs/clap](./misc/clap-rs-clap.md) | ⭐ 16.4k | Misc |
| 3 | [simple-icons/simple-icons](./design/simple-icons-simple-icons.md) | ⭐ 25.1k | Design |
| 4 | [mvanhorn/last30days-skill](./trading/mvanhorn-last30days-skill.md) | ⭐ 25.3k | Trading |
| 5 | [GyulyVGC/sniffnet](./frontend/gyulyvgc-sniffnet.md) | ⭐ 37.3k | Frontend |
| 6 | [jackocnr/intl-tel-input](./aiml/jackocnr-intl-tel-input.md) | ⭐ 8.2k | AI/ML |
| 7 | [santifer/career-ops](./aiml/santifer-career-ops.md) | ⭐ 43.8k | AI/ML |
| 8 | [exelban/stats](./misc/exelban-stats.md) | ⭐ 38.6k | Misc |
| 9 | [navidrome/navidrome](./aiml/navidrome-navidrome.md) | ⭐ 21k | AI/ML |
| 10 | [flybywiresim/aircraft](./aiml/flybywiresim-aircraft.md) | ⭐ 5.4k | AI/ML |

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
