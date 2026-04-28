# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **10442** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 4025 | [Browse →](./aiml/) |
| 📦 **Misc** | 1965 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1032 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 848 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 621 | [Browse →](./backend/) |
| 🔧 **DevTools** | 600 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 376 | [Browse →](./crypto/) |
| 📊 **Data** | 232 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 215 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 131 | [Browse →](./mobile/) |
| 💳 **Payments** | 121 | [Browse →](./payments/) |
| 📈 **Trading** | 103 | [Browse →](./trading/) |
| 🔐 **Security** | 94 | [Browse →](./security/) |
| ✨ **Design** | 36 | [Browse →](./design/) |
| 🎯 **Product** | 24 | [Browse →](./product/) |
| 🏷️ **Marketing** | 19 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [aws/aws-sam-cli](./frontend/aws-aws-sam-cli.md) | ⭐ 6.7k | Frontend |
| 2 | [aimeos/aimeos-laravel](./aiml/aimeos-aimeos-laravel.md) | ⭐ 8.6k | AI/ML |
| 3 | [MonoGame/MonoGame](./misc/monogame-monogame.md) | ⭐ 13.8k | Misc |
| 4 | [nukeop/nuclear](./aiml/nukeop-nuclear.md) | ⭐ 17.4k | AI/ML |
| 5 | [spaceship-prompt/spaceship-prompt](./misc/spaceship-prompt-spaceship-prompt.md) | ⭐ 20.5k | Misc |
| 6 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 7 | [photoprism/photoprism](./aiml/photoprism-photoprism.md) | ⭐ 39.6k | AI/ML |
| 8 | [triggerdotdev/trigger.dev](./orchestration/triggerdotdev-trigger.dev.md) | ⭐ 14.7k | Orchestration |
| 9 | [readest/readest](./aiml/readest-readest.md) | ⭐ 20k | AI/ML |
| 10 | [web-platform-tests/wpt](./aiml/web-platform-tests-wpt.md) | ⭐ 5.9k | AI/ML |

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
