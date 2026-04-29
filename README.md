# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **11212** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 4296 | [Browse →](./aiml/) |
| 📦 **Misc** | 2144 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1100 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 888 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 677 | [Browse →](./backend/) |
| 🔧 **DevTools** | 670 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 399 | [Browse →](./crypto/) |
| 📊 **Data** | 241 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 238 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 136 | [Browse →](./mobile/) |
| 💳 **Payments** | 125 | [Browse →](./payments/) |
| 📈 **Trading** | 116 | [Browse →](./trading/) |
| 🔐 **Security** | 99 | [Browse →](./security/) |
| ✨ **Design** | 37 | [Browse →](./design/) |
| 🎯 **Product** | 25 | [Browse →](./product/) |
| 🏷️ **Marketing** | 21 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [tldraw/tldraw](./frontend/tldraw-tldraw.md) | ⭐ 46.7k | Frontend |
| 2 | [clash-verge-rev/clash-verge-rev](./aiml/clash-verge-rev-clash-verge-rev.md) | ⭐ 114.5k | AI/ML |
| 3 | [ueberdosis/tiptap](./frontend/ueberdosis-tiptap.md) | ⭐ 36.5k | Frontend |
| 4 | [nilbuild/developer-roadmap](./crypto/nilbuild-developer-roadmap.md) | ⭐ 353.9k | Crypto |
| 5 | [vnotex/vnote](./aiml/vnotex-vnote.md) | ⭐ 12.8k | AI/ML |
| 6 | [matplotlib/matplotlib](./data/matplotlib-matplotlib.md) | ⭐ 22.8k | Data |
| 7 | [sharkdp/fd](./devtools/sharkdp-fd.md) | ⭐ 42.7k | DevTools |
| 8 | [NousResearch/hermes-agent](./aiml/nousresearch-hermes-agent.md) | ⭐ 123.5k | AI/ML |
| 9 | [oapi-codegen/oapi-codegen](./backend/oapi-codegen-oapi-codegen.md) | ⭐ 8.3k | Backend |
| 10 | [micro-editor/micro](./frontend/micro-editor-micro.md) | ⭐ 28.5k | Frontend |

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
