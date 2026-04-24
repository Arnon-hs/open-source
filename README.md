# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **4077** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1564 | [Browse →](./aiml/) |
| 📦 **Misc** | 643 | [Browse →](./misc/) |
| 🎨 **Frontend** | 419 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 382 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 246 | [Browse →](./backend/) |
| 🔧 **DevTools** | 229 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 161 | [Browse →](./crypto/) |
| 📊 **Data** | 105 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 94 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 57 | [Browse →](./payments/) |
| 📱 **Mobile** | 56 | [Browse →](./mobile/) |
| 📈 **Trading** | 45 | [Browse →](./trading/) |
| 🔐 **Security** | 43 | [Browse →](./security/) |
| ✨ **Design** | 15 | [Browse →](./design/) |
| 🎯 **Product** | 13 | [Browse →](./product/) |
| 🏷️ **Marketing** | 5 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [lutzroeder/netron](./aiml/lutzroeder-netron.md) | ⭐ 32.8k | AI/ML |
| 2 | [XIU2/TrackersListCollection](./aiml/xiu2-trackerslistcollection.md) | ⭐ 31.1k | AI/ML |
| 3 | [TanStack/query](./frontend/tanstack-query.md) | ⭐ 49.2k | Frontend |
| 4 | [ansible/awx](./frontend/ansible-awx.md) | ⭐ 15.4k | Frontend |
| 5 | [vxcontrol/pentagi](./orchestration/vxcontrol-pentagi.md) | ⭐ 15.6k | Orchestration |
| 6 | [quic-go/quic-go](./frontend/quic-go-quic-go.md) | ⭐ 11.6k | Frontend |
| 7 | [caddyserver/caddy](./backend/caddyserver-caddy.md) | ⭐ 71.8k | Backend |
| 8 | [expo/expo](./frontend/expo-expo.md) | ⭐ 49k | Frontend |
| 9 | [nestjs/nest](./frontend/nestjs-nest.md) | ⭐ 75.3k | Frontend |
| 10 | [Aider-AI/aider](./aiml/aider-ai-aider.md) | ⭐ 43.9k | AI/ML |

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
