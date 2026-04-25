# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **4248** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1628 | [Browse →](./aiml/) |
| 📦 **Misc** | 668 | [Browse →](./misc/) |
| 🎨 **Frontend** | 438 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 400 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 257 | [Browse →](./backend/) |
| 🔧 **DevTools** | 235 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 166 | [Browse →](./crypto/) |
| 📊 **Data** | 112 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 98 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 60 | [Browse →](./payments/) |
| 📱 **Mobile** | 59 | [Browse →](./mobile/) |
| 📈 **Trading** | 46 | [Browse →](./trading/) |
| 🔐 **Security** | 45 | [Browse →](./security/) |
| ✨ **Design** | 17 | [Browse →](./design/) |
| 🎯 **Product** | 14 | [Browse →](./product/) |
| 🏷️ **Marketing** | 5 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [hoochanlon/hamuleite](./misc/hoochanlon-hamuleite.md) | ⭐ 9.4k | Misc |
| 2 | [harvard-edge/cs249r_book](./aiml/harvard-edge-cs249r-book.md) | ⭐ 23.8k | AI/ML |
| 3 | [godotengine/godot-docs](./misc/godotengine-godot-docs.md) | ⭐ 5.2k | Misc |
| 4 | [janhq/jan](./aiml/janhq-jan.md) | ⭐ 42.1k | AI/ML |
| 5 | [stride3d/stride](./misc/stride3d-stride.md) | ⭐ 7.6k | Misc |
| 6 | [web-platform-tests/wpt](./aiml/web-platform-tests-wpt.md) | ⭐ 5.9k | AI/ML |
| 7 | [gogs/gogs](./aiml/gogs-gogs.md) | ⭐ 47.5k | AI/ML |
| 8 | [Anionex/banana-slides](./aiml/anionex-banana-slides.md) | ⭐ 14.1k | AI/ML |
| 9 | [microsoft/playwright](./backend/microsoft-playwright.md) | ⭐ 87.2k | Backend |
| 10 | [YouMind-OpenLab/awesome-nano-banana-pro-prompts](./aiml/youmind-openlab-awesome-nano-banana-pro-prompts.md) | ⭐ 11.5k | AI/ML |

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
