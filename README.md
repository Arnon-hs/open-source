# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **8687** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 3352 | [Browse →](./aiml/) |
| 📦 **Misc** | 1599 | [Browse →](./misc/) |
| 🎨 **Frontend** | 877 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 729 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 504 | [Browse →](./backend/) |
| 🔧 **DevTools** | 500 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 305 | [Browse →](./crypto/) |
| 📊 **Data** | 184 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 174 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 118 | [Browse →](./mobile/) |
| 💳 **Payments** | 113 | [Browse →](./payments/) |
| 📈 **Trading** | 88 | [Browse →](./trading/) |
| 🔐 **Security** | 78 | [Browse →](./security/) |
| ✨ **Design** | 29 | [Browse →](./design/) |
| 🎯 **Product** | 22 | [Browse →](./product/) |
| 🏷️ **Marketing** | 15 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [swagger-api/swagger-core](./backend/swagger-api-swagger-core.md) | ⭐ 7.5k | Backend |
| 2 | [projectdiscovery/httpx](./devtools/projectdiscovery-httpx.md) | ⭐ 9.9k | DevTools |
| 3 | [moby/buildkit](./orchestration/moby-buildkit.md) | ⭐ 9.9k | Orchestration |
| 4 | [tw93/Pake](./misc/tw93-pake.md) | ⭐ 48.2k | Misc |
| 5 | [webstudio-is/webstudio](./frontend/webstudio-is-webstudio.md) | ⭐ 8.5k | Frontend |
| 6 | [ceph/ceph](./crypto/ceph-ceph.md) | ⭐ 16.5k | Crypto |
| 7 | [zitadel/zitadel](./aiml/zitadel-zitadel.md) | ⭐ 13.6k | AI/ML |
| 8 | [ruby/ruby](./misc/ruby-ruby.md) | ⭐ 23.5k | Misc |
| 9 | [ionic-team/capacitor](./aiml/ionic-team-capacitor.md) | ⭐ 15.5k | AI/ML |
| 10 | [formbricks/formbricks](./aiml/formbricks-formbricks.md) | ⭐ 12.1k | AI/ML |

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
