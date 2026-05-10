# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **5658** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2251 | [Browse →](./aiml/) |
| 📦 **Misc** | 1030 | [Browse →](./misc/) |
| 🎨 **Frontend** | 568 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 516 | [Browse →](./orchestration/) |
| 🔧 **DevTools** | 299 | [Browse →](./devtools/) |
| ⚙️ **Backend** | 274 | [Browse →](./backend/) |
| ⛓️ **Crypto** | 205 | [Browse →](./crypto/) |
| 📊 **Data** | 132 | [Browse →](./data/) |
| 💳 **Payments** | 94 | [Browse →](./payments/) |
| 📈 **Trading** | 73 | [Browse →](./trading/) |
| 📱 **Mobile** | 68 | [Browse →](./mobile/) |
| 🚀 **DevOps & Infra** | 64 | [Browse →](./devopsinfra/) |
| 🔐 **Security** | 44 | [Browse →](./security/) |
| ✨ **Design** | 19 | [Browse →](./design/) |
| 🎯 **Product** | 13 | [Browse →](./product/) |
| 🏷️ **Marketing** | 8 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [gofiber/fiber](./backend/gofiber-fiber.md) | ⭐ 39.7k | Backend |
| 2 | [laurent22/joplin](./frontend/laurent22-joplin.md) | ⭐ 54.7k | Frontend |
| 3 | [quic-go/quic-go](./frontend/quic-go-quic-go.md) | ⭐ 11.6k | Frontend |
| 4 | [x64dbg/x64dbg](./security/x64dbg-x64dbg.md) | ⭐ 48.3k | Security |
| 5 | [MudBlazor/MudBlazor](./frontend/mudblazor-mudblazor.md) | ⭐ 10.4k | Frontend |
| 6 | [ScrapeGraphAI/Scrapegraph-ai](./aiml/scrapegraphai-scrapegraph-ai.md) | ⭐ 24.9k | AI/ML |
| 7 | [ohmyzsh/ohmyzsh](./aiml/ohmyzsh-ohmyzsh.md) | ⭐ 186.9k | AI/ML |
| 8 | [streamlink/streamlink](./aiml/streamlink-streamlink.md) | ⭐ 11.5k | AI/ML |
| 9 | [hugohe3/ppt-master](./aiml/hugohe3-ppt-master.md) | ⭐ 14.1k | AI/ML |
| 10 | [JuliusBrussee/caveman](./aiml/juliusbrussee-caveman.md) | ⭐ 57.3k | AI/ML |

## 🚀 How it works

```mermaid
graph LR
  A[GitHub · HN · Reddit · PH] --> B[RepoScout]
  B --> C[Score · Dedupe · Categorize]
  C --> D[LLM Summarize]
  D --> E[PostgreSQL DB]
  D --> F[This Catalog]
```

1. **Discover** — 4 sources pulled in parallel
2. **Score** — weighted: stars, forks, recency, topics, source trust
3. **Categorize** — rule-based + LLM-assisted tagging
4. **Summarize** — concise bilingual (EN/RU) summaries via LLM
5. **Sync** — markdown committed here, metadata upserted to PostgreSQL

## 🛠️ Self-host

```bash
git clone https://github.com/kirbudilov01/reposearchengine
cp .env.example .env
# Set LLM_PROVIDER, CATALOG_REPO_PATH, DATABASE_URL, ...
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
