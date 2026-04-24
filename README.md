# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **3787** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1451 | [Browse →](./aiml/) |
| 📦 **Misc** | 599 | [Browse →](./misc/) |
| 🎨 **Frontend** | 397 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 348 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 232 | [Browse →](./backend/) |
| 🔧 **DevTools** | 208 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 151 | [Browse →](./crypto/) |
| 📊 **Data** | 98 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 86 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 54 | [Browse →](./payments/) |
| 📱 **Mobile** | 53 | [Browse →](./mobile/) |
| 📈 **Trading** | 40 | [Browse →](./trading/) |
| 🔐 **Security** | 39 | [Browse →](./security/) |
| ✨ **Design** | 14 | [Browse →](./design/) |
| 🎯 **Product** | 12 | [Browse →](./product/) |
| 🏷️ **Marketing** | 5 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [shadps4-emu/shadPS4](./frontend/shadps4-emu-shadps4.md) | ⭐ 30.9k | Frontend |
| 2 | [GoogleChrome/lighthouse](./devtools/googlechrome-lighthouse.md) | ⭐ 30.1k | DevTools |
| 3 | [catboost/catboost](./aiml/catboost-catboost.md) | ⭐ 8.9k | AI/ML |
| 4 | [ansible/awx](./frontend/ansible-awx.md) | ⭐ 15.4k | Frontend |
| 5 | [tensorflow/tensorflow](./aiml/tensorflow-tensorflow.md) | ⭐ 194.9k | AI/ML |
| 6 | [stashapp/stash](./misc/stashapp-stash.md) | ⭐ 12.2k | Misc |
| 7 | [grafana/k6](./devtools/grafana-k6.md) | ⭐ 30.4k | DevTools |
| 8 | [RustPython/RustPython](./misc/rustpython-rustpython.md) | ⭐ 22k | Misc |
| 9 | [Canner/WrenAI](./aiml/canner-wrenai.md) | ⭐ 15k | AI/ML |
| 10 | [karatelabs/karate](./backend/karatelabs-karate.md) | ⭐ 8.8k | Backend |

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
