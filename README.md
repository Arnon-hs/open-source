# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **2799** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1054 | [Browse →](./aiml/) |
| 📦 **Misc** | 446 | [Browse →](./misc/) |
| 🎨 **Frontend** | 303 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 257 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 175 | [Browse →](./backend/) |
| 🔧 **DevTools** | 144 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 111 | [Browse →](./crypto/) |
| 📊 **Data** | 78 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 64 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 41 | [Browse →](./payments/) |
| 📱 **Mobile** | 38 | [Browse →](./mobile/) |
| 🔐 **Security** | 32 | [Browse →](./security/) |
| 📈 **Trading** | 31 | [Browse →](./trading/) |
| ✨ **Design** | 11 | [Browse →](./design/) |
| 🎯 **Product** | 11 | [Browse →](./product/) |
| 🏷️ **Marketing** | 3 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [rustdesk/rustdesk](./mobile/rustdesk-rustdesk.md) | ⭐ 112.8k | Mobile |
| 2 | [swc-project/swc](./misc/swc-project-swc.md) | ⭐ 33.4k | Misc |
| 3 | [pola-rs/polars](./data/pola-rs-polars.md) | ⭐ 38.3k | Data |
| 4 | [GopeedLab/gopeed](./frontend/gopeedlab-gopeed.md) | ⭐ 24.1k | Frontend |
| 5 | [kserve/kserve](./aiml/kserve-kserve.md) | ⭐ 5.4k | AI/ML |
| 6 | [home-assistant/core](./misc/home-assistant-core.md) | ⭐ 86.2k | Misc |
| 7 | [kestra-io/kestra](./orchestration/kestra-io-kestra.md) | ⭐ 26.8k | Orchestration |
| 8 | [daytonaio/daytona](./orchestration/daytonaio-daytona.md) | ⭐ 72.4k | Orchestration |
| 9 | [OpenHands/OpenHands](./aiml/openhands-openhands.md) | ⭐ 72k | AI/ML |
| 10 | [navidrome/navidrome](./aiml/navidrome-navidrome.md) | ⭐ 20.6k | AI/ML |

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
