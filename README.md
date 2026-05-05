# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **16676** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 6207 | [Browse →](./aiml/) |
| 📦 **Misc** | 3499 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1643 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1200 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 1022 | [Browse →](./backend/) |
| 🔧 **DevTools** | 973 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 560 | [Browse →](./crypto/) |
| 📊 **Data** | 381 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 363 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 227 | [Browse →](./mobile/) |
| 📈 **Trading** | 170 | [Browse →](./trading/) |
| 💳 **Payments** | 169 | [Browse →](./payments/) |
| 🔐 **Security** | 142 | [Browse →](./security/) |
| ✨ **Design** | 56 | [Browse →](./design/) |
| 🎯 **Product** | 33 | [Browse →](./product/) |
| 🏷️ **Marketing** | 31 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [shuaibiyy/awesome-tf](./aiml/shuaibiyy-awesome-tf.md) | ⭐ 6.4k | AI/ML |
| 2 | [cheeriojs/cheerio](./aiml/cheeriojs-cheerio.md) | ⭐ 30.3k | AI/ML |
| 3 | [prowler-cloud/prowler](./security/prowler-cloud-prowler.md) | ⭐ 13.7k | Security |
| 4 | [mochajs/mocha](./devtools/mochajs-mocha.md) | ⭐ 22.9k | DevTools |
| 5 | [swagger-api/swagger-ui](./aiml/swagger-api-swagger-ui.md) | ⭐ 28.8k | AI/ML |
| 6 | [FlowiseAI/Flowise](./orchestration/flowiseai-flowise.md) | ⭐ 52.5k | Orchestration |
| 7 | [AstrBotDevs/AstrBot](./aiml/astrbotdevs-astrbot.md) | ⭐ 31.3k | AI/ML |
| 8 | [jhy/jsoup](./aiml/jhy-jsoup.md) | ⭐ 11.4k | AI/ML |
| 9 | [Donchitos/Claude-Code-Game-Studios](./aiml/donchitos-claude-code-game-studios.md) | ⭐ 17.2k | AI/ML |
| 10 | [datahub-project/datahub](./aiml/datahub-project-datahub.md) | ⭐ 11.9k | AI/ML |

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
