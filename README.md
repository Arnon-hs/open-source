# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **16024** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 5964 | [Browse →](./aiml/) |
| 📦 **Misc** | 3331 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1581 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1166 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 984 | [Browse →](./backend/) |
| 🔧 **DevTools** | 949 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 541 | [Browse →](./crypto/) |
| 📊 **Data** | 366 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 343 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 221 | [Browse →](./mobile/) |
| 💳 **Payments** | 166 | [Browse →](./payments/) |
| 📈 **Trading** | 164 | [Browse →](./trading/) |
| 🔐 **Security** | 130 | [Browse →](./security/) |
| ✨ **Design** | 54 | [Browse →](./design/) |
| 🎯 **Product** | 33 | [Browse →](./product/) |
| 🏷️ **Marketing** | 31 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [mattermost-community/focalboard](./misc/mattermost-community-focalboard.md) | ⭐ 26.1k | Misc |
| 2 | [microsoft/presidio](./aiml/microsoft-presidio.md) | ⭐ 7.9k | AI/ML |
| 3 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 4 | [zitadel/zitadel](./aiml/zitadel-zitadel.md) | ⭐ 13.7k | AI/ML |
| 5 | [K-Dense-AI/scientific-agent-skills](./orchestration/k-dense-ai-scientific-agent-skills.md) | ⭐ 20k | Orchestration |
| 6 | [mastra-ai/mastra](./aiml/mastra-ai-mastra.md) | ⭐ 23.5k | AI/ML |
| 7 | [knative/docs](./aiml/knative-docs.md) | ⭐ 5k | AI/ML |
| 8 | [apache/hudi](./data/apache-hudi.md) | ⭐ 6.2k | Data |
| 9 | [community-scripts/ProxmoxVE](./aiml/community-scripts-proxmoxve.md) | ⭐ 27.9k | AI/ML |
| 10 | [screenpipe/screenpipe](./aiml/screenpipe-screenpipe.md) | ⭐ 18.5k | AI/ML |

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
