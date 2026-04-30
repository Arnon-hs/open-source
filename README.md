# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **12462** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 4756 | [Browse →](./aiml/) |
| 📦 **Misc** | 2425 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1214 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 966 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 758 | [Browse →](./backend/) |
| 🔧 **DevTools** | 741 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 446 | [Browse →](./crypto/) |
| 📊 **Data** | 280 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 272 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 151 | [Browse →](./mobile/) |
| 💳 **Payments** | 131 | [Browse →](./payments/) |
| 📈 **Trading** | 129 | [Browse →](./trading/) |
| 🔐 **Security** | 109 | [Browse →](./security/) |
| ✨ **Design** | 37 | [Browse →](./design/) |
| 🎯 **Product** | 25 | [Browse →](./product/) |
| 🏷️ **Marketing** | 22 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [bpftrace/bpftrace](./misc/bpftrace-bpftrace.md) | ⭐ 10.1k | Misc |
| 2 | [dragonflydb/dragonfly](./aiml/dragonflydb-dragonfly.md) | ⭐ 30.4k | AI/ML |
| 3 | [mastodon/mastodon](./devopsinfra/mastodon-mastodon.md) | ⭐ 49.9k | DevOps & Infra |
| 4 | [arc53/DocsGPT](./aiml/arc53-docsgpt.md) | ⭐ 17.9k | AI/ML |
| 5 | [Wei-Shaw/sub2api](./aiml/wei-shaw-sub2api.md) | ⭐ 16.9k | AI/ML |
| 6 | [lichess-org/lila](./backend/lichess-org-lila.md) | ⭐ 18.1k | Backend |
| 7 | [XIU2/TrackersListCollection](./aiml/xiu2-trackerslistcollection.md) | ⭐ 31.2k | AI/ML |
| 8 | [openshift/origin](./aiml/openshift-origin.md) | ⭐ 8.6k | AI/ML |
| 9 | [hiyouga/LlamaFactory](./trading/hiyouga-llamafactory.md) | ⭐ 70.8k | Trading |
| 10 | [aio-libs/aiohttp](./aiml/aio-libs-aiohttp.md) | ⭐ 16.4k | AI/ML |

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
