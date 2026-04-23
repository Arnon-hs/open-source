# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **1984** |
| 📁 **Categories** | **15** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 747 | [Browse →](./aiml/) |
| 📦 **Misc** | 331 | [Browse →](./misc/) |
| 🎨 **Frontend** | 223 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 176 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 121 | [Browse →](./backend/) |
| 🔧 **DevTools** | 98 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 80 | [Browse →](./crypto/) |
| 📊 **Data** | 59 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 45 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 29 | [Browse →](./mobile/) |
| 💳 **Payments** | 24 | [Browse →](./payments/) |
| 📈 **Trading** | 22 | [Browse →](./trading/) |
| 🔐 **Security** | 18 | [Browse →](./security/) |
| 🎯 **Product** | 8 | [Browse →](./product/) |
| ✨ **Design** | 3 | [Browse →](./design/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [Snailclimb/JavaGuide](./aiml/snailclimb-javaguide.md) | ⭐ 155.2k | AI/ML |
| 2 | [microsoft/agent-framework](./orchestration/microsoft-agent-framework.md) | ⭐ 9.7k | Orchestration |
| 3 | [apache/superset](./frontend/apache-superset.md) | ⭐ 72.6k | Frontend |
| 4 | [payloadcms/payload](./frontend/payloadcms-payload.md) | ⭐ 42k | Frontend |
| 5 | [skypilot-org/skypilot](./aiml/skypilot-org-skypilot.md) | ⭐ 9.9k | AI/ML |
| 6 | [saltstack/salt](./devopsinfra/saltstack-salt.md) | ⭐ 15.4k | DevOps & Infra |
| 7 | [seaweedfs/seaweedfs](./aiml/seaweedfs-seaweedfs.md) | ⭐ 31.7k | AI/ML |
| 8 | [falconry/falcon](./backend/falconry-falcon.md) | ⭐ 9.8k | Backend |
| 9 | [Anionex/banana-slides](./aiml/anionex-banana-slides.md) | ⭐ 14.1k | AI/ML |
| 10 | [streamlink/streamlink](./aiml/streamlink-streamlink.md) | ⭐ 11.4k | AI/ML |

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
