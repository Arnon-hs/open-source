# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **160** |
| 📁 **Categories** | **11** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 69 | [Browse →](./aiml/) |
| 📦 **Misc** | 31 | [Browse →](./misc/) |
| 🎨 **Frontend** | 17 | [Browse →](./frontend/) |
| ⚙️ **Backend** | 13 | [Browse →](./backend/) |
| 📊 **Data** | 11 | [Browse →](./data/) |
| 📱 **Mobile** | 10 | [Browse →](./mobile/) |
| 🚀 **DevOps & Infra** | 4 | [Browse →](./devopsinfra/) |
| 🔧 **DevTools** | 2 | [Browse →](./devtools/) |
| 🔐 **Security** | 1 | [Browse →](./security/) |
| ✨ **Design** | 1 | [Browse →](./design/) |
| 🎯 **Product** | 1 | [Browse →](./product/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [langfuse/langfuse](./aiml/langfuse-langfuse.md) | ⭐ 25.3k | AI/ML |
| 2 | [drawdb-io/drawdb](./aiml/drawdb-io-drawdb.md) | ⭐ 37.1k | AI/ML |
| 3 | [getsentry/sentry](./aiml/getsentry-sentry.md) | ⭐ 43.6k | AI/ML |
| 4 | [Fincept-Corporation/FinceptTerminal](./data/fincept-corporation-finceptterminal.md) | ⭐ 10.8k | Data |
| 5 | [chatwoot/chatwoot](./aiml/chatwoot-chatwoot.md) | ⭐ 28.7k | AI/ML |
| 6 | [usebruno/bruno](./backend/usebruno-bruno.md) | ⭐ 43.1k | Backend |
| 7 | [ente-io/ente](./mobile/ente-io-ente.md) | ⭐ 26.1k | Mobile |
| 8 | [nextcloud/server](./backend/nextcloud-server.md) | ⭐ 34.7k | Backend |
| 9 | [koala73/worldmonitor](./aiml/koala73-worldmonitor.md) | ⭐ 50.7k | AI/ML |
| 10 | [zaproxy/zaproxy](./security/zaproxy-zaproxy.md) | ⭐ 15k | Security |

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
