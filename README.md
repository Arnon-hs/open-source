# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **11096** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 4253 | [Browse →](./aiml/) |
| 📦 **Misc** | 2115 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1090 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 882 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 669 | [Browse →](./backend/) |
| 🔧 **DevTools** | 661 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 396 | [Browse →](./crypto/) |
| 📊 **Data** | 240 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 235 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 136 | [Browse →](./mobile/) |
| 💳 **Payments** | 125 | [Browse →](./payments/) |
| 📈 **Trading** | 113 | [Browse →](./trading/) |
| 🔐 **Security** | 99 | [Browse →](./security/) |
| ✨ **Design** | 36 | [Browse →](./design/) |
| 🎯 **Product** | 25 | [Browse →](./product/) |
| 🏷️ **Marketing** | 21 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [tiajinsha/JKVideo](./frontend/tiajinsha-jkvideo.md) | ⭐ 4.9k | Frontend |
| 2 | [clash-verge-rev/clash-verge-rev](./aiml/clash-verge-rev-clash-verge-rev.md) | ⭐ 114.5k | AI/ML |
| 3 | [ueberdosis/tiptap](./frontend/ueberdosis-tiptap.md) | ⭐ 36.5k | Frontend |
| 4 | [nilbuild/developer-roadmap](./crypto/nilbuild-developer-roadmap.md) | ⭐ 353.9k | Crypto |
| 5 | [vnotex/vnote](./aiml/vnotex-vnote.md) | ⭐ 12.8k | AI/ML |
| 6 | [zhkl0228/unidbg](./mobile/zhkl0228-unidbg.md) | ⭐ 4.9k | Mobile |
| 7 | [huggingface/transformers](./crypto/huggingface-transformers.md) | ⭐ 160.1k | Crypto |
| 8 | [gruntwork-io/terratest](./devtools/gruntwork-io-terratest.md) | ⭐ 7.9k | DevTools |
| 9 | [assistant-ui/assistant-ui](./aiml/assistant-ui-assistant-ui.md) | ⭐ 9.8k | AI/ML |
| 10 | [matplotlib/matplotlib](./data/matplotlib-matplotlib.md) | ⭐ 22.8k | Data |

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
