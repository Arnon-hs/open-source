# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **1931** |
| 📁 **Categories** | **15** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 724 | [Browse →](./aiml/) |
| 📦 **Misc** | 324 | [Browse →](./misc/) |
| 🎨 **Frontend** | 216 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 174 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 115 | [Browse →](./backend/) |
| 🔧 **DevTools** | 95 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 78 | [Browse →](./crypto/) |
| 📊 **Data** | 58 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 45 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 29 | [Browse →](./mobile/) |
| 💳 **Payments** | 24 | [Browse →](./payments/) |
| 📈 **Trading** | 21 | [Browse →](./trading/) |
| 🔐 **Security** | 17 | [Browse →](./security/) |
| 🎯 **Product** | 8 | [Browse →](./product/) |
| ✨ **Design** | 3 | [Browse →](./design/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [Snailclimb/JavaGuide](./aiml/snailclimb-javaguide.md) | ⭐ 155.2k | AI/ML |
| 2 | [microsoft/agent-framework](./orchestration/microsoft-agent-framework.md) | ⭐ 9.7k | Orchestration |
| 3 | [huggingface/datasets](./aiml/huggingface-datasets.md) | ⭐ 21.4k | AI/ML |
| 4 | [oven-sh/bun](./frontend/oven-sh-bun.md) | ⭐ 89.3k | Frontend |
| 5 | [apache/superset](./frontend/apache-superset.md) | ⭐ 72.6k | Frontend |
| 6 | [saltstack/salt](./devopsinfra/saltstack-salt.md) | ⭐ 15.4k | DevOps & Infra |
| 7 | [seaweedfs/seaweedfs](./aiml/seaweedfs-seaweedfs.md) | ⭐ 31.7k | AI/ML |
| 8 | [awesome-foss/awesome-sysadmin](./misc/awesome-foss-awesome-sysadmin.md) | ⭐ 33.7k | Misc |
| 9 | [cube-js/cube](./aiml/cube-js-cube.md) | ⭐ 19.8k | AI/ML |
| 10 | [mickael-kerjean/filestash](./data/mickael-kerjean-filestash.md) | ⭐ 14.1k | Data |

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
