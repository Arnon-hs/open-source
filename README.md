# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **2580** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 958 | [Browse →](./aiml/) |
| 📦 **Misc** | 418 | [Browse →](./misc/) |
| 🎨 **Frontend** | 282 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 239 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 165 | [Browse →](./backend/) |
| 🔧 **DevTools** | 127 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 106 | [Browse →](./crypto/) |
| 📊 **Data** | 72 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 60 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 39 | [Browse →](./payments/) |
| 📱 **Mobile** | 35 | [Browse →](./mobile/) |
| 📈 **Trading** | 29 | [Browse →](./trading/) |
| 🔐 **Security** | 28 | [Browse →](./security/) |
| ✨ **Design** | 10 | [Browse →](./design/) |
| 🎯 **Product** | 10 | [Browse →](./product/) |
| 🏷️ **Marketing** | 2 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [firebase/firebase-js-sdk](./aiml/firebase-firebase-js-sdk.md) | ⭐ 5.1k | AI/ML |
| 2 | [frappe/frappe](./aiml/frappe-frappe.md) | ⭐ 10k | AI/ML |
| 3 | [Kilo-Org/kilocode](./aiml/kilo-org-kilocode.md) | ⭐ 18.5k | AI/ML |
| 4 | [azerothcore/azerothcore-wotlk](./backend/azerothcore-azerothcore-wotlk.md) | ⭐ 8.2k | Backend |
| 5 | [huggingface/datasets](./aiml/huggingface-datasets.md) | ⭐ 21.4k | AI/ML |
| 6 | [awesome-foss/awesome-sysadmin](./misc/awesome-foss-awesome-sysadmin.md) | ⭐ 33.7k | Misc |
| 7 | [cube-js/cube](./aiml/cube-js-cube.md) | ⭐ 19.8k | AI/ML |
| 8 | [flameshot-org/flameshot](./frontend/flameshot-org-flameshot.md) | ⭐ 29.8k | Frontend |
| 9 | [mickael-kerjean/filestash](./data/mickael-kerjean-filestash.md) | ⭐ 14.1k | Data |
| 10 | [juicedata/juicefs](./aiml/juicedata-juicefs.md) | ⭐ 13.5k | AI/ML |

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
