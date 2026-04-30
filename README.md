# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **12363** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 4724 | [Browse →](./aiml/) |
| 📦 **Misc** | 2403 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1206 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 962 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 750 | [Browse →](./backend/) |
| 🔧 **DevTools** | 733 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 439 | [Browse →](./crypto/) |
| 📊 **Data** | 276 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 267 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 151 | [Browse →](./mobile/) |
| 💳 **Payments** | 130 | [Browse →](./payments/) |
| 📈 **Trading** | 129 | [Browse →](./trading/) |
| 🔐 **Security** | 109 | [Browse →](./security/) |
| ✨ **Design** | 37 | [Browse →](./design/) |
| 🎯 **Product** | 25 | [Browse →](./product/) |
| 🏷️ **Marketing** | 22 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [ophub/amlogic-s9xxx-armbian](./aiml/ophub-amlogic-s9xxx-armbian.md) | ⭐ 9.1k | AI/ML |
| 2 | [kubernetes/kube-state-metrics](./aiml/kubernetes-kube-state-metrics.md) | ⭐ 6.1k | AI/ML |
| 3 | [nocodb/nocodb](./aiml/nocodb-nocodb.md) | ⭐ 62.9k | AI/ML |
| 4 | [mastodon/mastodon](./devopsinfra/mastodon-mastodon.md) | ⭐ 49.9k | DevOps & Infra |
| 5 | [botpress/botpress](./orchestration/botpress-botpress.md) | ⭐ 14.7k | Orchestration |
| 6 | [microsoft/ai-agents-for-beginners](./orchestration/microsoft-ai-agents-for-beginners.md) | ⭐ 60.2k | Orchestration |
| 7 | [modelscope/ms-swift](./aiml/modelscope-ms-swift.md) | ⭐ 14k | AI/ML |
| 8 | [bitwarden/clients](./devtools/bitwarden-clients.md) | ⭐ 12.7k | DevTools |
| 9 | [vxcontrol/pentagi](./orchestration/vxcontrol-pentagi.md) | ⭐ 16.2k | Orchestration |
| 10 | [knative/serving](./aiml/knative-serving.md) | ⭐ 6k | AI/ML |

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
