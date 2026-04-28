# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **10751** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 4147 | [Browse →](./aiml/) |
| 📦 **Misc** | 2030 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1059 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 861 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 643 | [Browse →](./backend/) |
| 🔧 **DevTools** | 624 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 388 | [Browse →](./crypto/) |
| 📊 **Data** | 236 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 222 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 133 | [Browse →](./mobile/) |
| 💳 **Payments** | 123 | [Browse →](./payments/) |
| 📈 **Trading** | 107 | [Browse →](./trading/) |
| 🔐 **Security** | 96 | [Browse →](./security/) |
| ✨ **Design** | 36 | [Browse →](./design/) |
| 🎯 **Product** | 25 | [Browse →](./product/) |
| 🏷️ **Marketing** | 21 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [apache/hudi](./data/apache-hudi.md) | ⭐ 6.2k | Data |
| 2 | [go-acme/lego](./devtools/go-acme-lego.md) | ⭐ 9.5k | DevTools |
| 3 | [fatedier/frp](./backend/fatedier-frp.md) | ⭐ 106.1k | Backend |
| 4 | [coollabsio/coolify](./backend/coollabsio-coolify.md) | ⭐ 54.3k | Backend |
| 5 | [roboflow/supervision](./misc/roboflow-supervision.md) | ⭐ 38.2k | Misc |
| 6 | [CherryHQ/cherry-studio](./aiml/cherryhq-cherry-studio.md) | ⭐ 44.7k | AI/ML |
| 7 | [RIOT-OS/RIOT](./misc/riot-os-riot.md) | ⭐ 5.7k | Misc |
| 8 | [jhipster/generator-jhipster](./frontend/jhipster-generator-jhipster.md) | ⭐ 22.4k | Frontend |
| 9 | [apache/apisix](./aiml/apache-apisix.md) | ⭐ 16.5k | AI/ML |
| 10 | [apache/shardingsphere](./data/apache-shardingsphere.md) | ⭐ 20.7k | Data |

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
