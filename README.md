# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **6524** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2502 | [Browse →](./aiml/) |
| 📦 **Misc** | 1142 | [Browse →](./misc/) |
| 🎨 **Frontend** | 647 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 592 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 376 | [Browse →](./backend/) |
| 🔧 **DevTools** | 367 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 228 | [Browse →](./crypto/) |
| 📊 **Data** | 152 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 137 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 99 | [Browse →](./mobile/) |
| 💳 **Payments** | 92 | [Browse →](./payments/) |
| 🔐 **Security** | 69 | [Browse →](./security/) |
| 📈 **Trading** | 67 | [Browse →](./trading/) |
| ✨ **Design** | 25 | [Browse →](./design/) |
| 🎯 **Product** | 20 | [Browse →](./product/) |
| 🏷️ **Marketing** | 9 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [junegunn/fzf](./devtools/junegunn-fzf.md) | ⭐ 79.8k | DevTools |
| 2 | [kovidgoyal/kitty](./misc/kovidgoyal-kitty.md) | ⭐ 32.6k | Misc |
| 3 | [stride3d/stride](./misc/stride3d-stride.md) | ⭐ 7.6k | Misc |
| 4 | [ValueCell-ai/ClawX](./orchestration/valuecell-ai-clawx.md) | ⭐ 6.7k | Orchestration |
| 5 | [mlflow/mlflow](./orchestration/mlflow-mlflow.md) | ⭐ 25.6k | Orchestration |
| 6 | [ComposioHQ/composio](./aiml/composiohq-composio.md) | ⭐ 27.9k | AI/ML |
| 7 | [knative/serving](./aiml/knative-serving.md) | ⭐ 6k | AI/ML |
| 8 | [ToolJet/ToolJet](./aiml/tooljet-tooljet.md) | ⭐ 37.8k | AI/ML |
| 9 | [HKUDS/nanobot](./aiml/hkuds-nanobot.md) | ⭐ 40.9k | AI/ML |
| 10 | [cvat-ai/cvat](./aiml/cvat-ai-cvat.md) | ⭐ 15.7k | AI/ML |

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
