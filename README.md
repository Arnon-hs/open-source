# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **5765** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2297 | [Browse →](./aiml/) |
| 📦 **Misc** | 1054 | [Browse →](./misc/) |
| 🎨 **Frontend** | 574 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 525 | [Browse →](./orchestration/) |
| 🔧 **DevTools** | 306 | [Browse →](./devtools/) |
| ⚙️ **Backend** | 277 | [Browse →](./backend/) |
| ⛓️ **Crypto** | 206 | [Browse →](./crypto/) |
| 📊 **Data** | 137 | [Browse →](./data/) |
| 💳 **Payments** | 94 | [Browse →](./payments/) |
| 📈 **Trading** | 75 | [Browse →](./trading/) |
| 📱 **Mobile** | 71 | [Browse →](./mobile/) |
| 🚀 **DevOps & Infra** | 64 | [Browse →](./devopsinfra/) |
| 🔐 **Security** | 44 | [Browse →](./security/) |
| ✨ **Design** | 19 | [Browse →](./design/) |
| 🎯 **Product** | 14 | [Browse →](./product/) |
| 🏷️ **Marketing** | 8 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [moeru-ai/airi](./aiml/moeru-ai-airi.md) | ⭐ 39.1k | AI/ML |
| 2 | [VoltAgent/awesome-agent-skills](./orchestration/voltagent-awesome-agent-skills.md) | ⭐ 21.1k | Orchestration |
| 3 | [dockur/windows](./aiml/dockur-windows.md) | ⭐ 51.3k | AI/ML |
| 4 | [gofiber/fiber](./backend/gofiber-fiber.md) | ⭐ 39.7k | Backend |
| 5 | [quic-go/quic-go](./frontend/quic-go-quic-go.md) | ⭐ 11.6k | Frontend |
| 6 | [MudBlazor/MudBlazor](./frontend/mudblazor-mudblazor.md) | ⭐ 10.4k | Frontend |
| 7 | [x64dbg/x64dbg](./security/x64dbg-x64dbg.md) | ⭐ 48.3k | Security |
| 8 | [laurent22/joplin](./frontend/laurent22-joplin.md) | ⭐ 54.7k | Frontend |
| 9 | [ScrapeGraphAI/Scrapegraph-ai](./aiml/scrapegraphai-scrapegraph-ai.md) | ⭐ 24.9k | AI/ML |
| 10 | [ohmyzsh/ohmyzsh](./aiml/ohmyzsh-ohmyzsh.md) | ⭐ 186.9k | AI/ML |

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
