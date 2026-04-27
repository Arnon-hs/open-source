# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **8127** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 3130 | [Browse →](./aiml/) |
| 📦 **Misc** | 1501 | [Browse →](./misc/) |
| 🎨 **Frontend** | 816 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 694 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 474 | [Browse →](./backend/) |
| 🔧 **DevTools** | 456 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 280 | [Browse →](./crypto/) |
| 📊 **Data** | 176 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 154 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 114 | [Browse →](./mobile/) |
| 💳 **Payments** | 111 | [Browse →](./payments/) |
| 📈 **Trading** | 84 | [Browse →](./trading/) |
| 🔐 **Security** | 75 | [Browse →](./security/) |
| ✨ **Design** | 28 | [Browse →](./design/) |
| 🎯 **Product** | 21 | [Browse →](./product/) |
| 🏷️ **Marketing** | 13 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [freqtrade/freqtrade](./crypto/freqtrade-freqtrade.md) | ⭐ 49.5k | Crypto |
| 2 | [apache/shardingsphere](./data/apache-shardingsphere.md) | ⭐ 20.7k | Data |
| 3 | [shadcn-ui/ui](./aiml/shadcn-ui-ui.md) | ⭐ 113.1k | AI/ML |
| 4 | [OpenAPITools/openapi-generator](./backend/openapitools-openapi-generator.md) | ⭐ 26.2k | Backend |
| 5 | [glpi-project/glpi](./data/glpi-project-glpi.md) | ⭐ 5.8k | Data |
| 6 | [dataease/dataease](./data/dataease-dataease.md) | ⭐ 23.8k | Data |
| 7 | [simple-icons/simple-icons](./design/simple-icons-simple-icons.md) | ⭐ 25k | Design |
| 8 | [authelia/authelia](./devopsinfra/authelia-authelia.md) | ⭐ 27.6k | DevOps & Infra |
| 9 | [yeasy/docker_practice](./aiml/yeasy-docker-practice.md) | ⭐ 26k | AI/ML |
| 10 | [meshtastic/firmware](./misc/meshtastic-firmware.md) | ⭐ 7.4k | Misc |

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
