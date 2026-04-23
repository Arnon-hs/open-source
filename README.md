# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **1198** |
| 📁 **Categories** | **15** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 453 | [Browse →](./aiml/) |
| 📦 **Misc** | 213 | [Browse →](./misc/) |
| 🎨 **Frontend** | 128 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 103 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 69 | [Browse →](./backend/) |
| 🔧 **DevTools** | 47 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 46 | [Browse →](./crypto/) |
| 📊 **Data** | 35 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 30 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 26 | [Browse →](./mobile/) |
| 💳 **Payments** | 15 | [Browse →](./payments/) |
| 📈 **Trading** | 15 | [Browse →](./trading/) |
| 🔐 **Security** | 12 | [Browse →](./security/) |
| 🎯 **Product** | 5 | [Browse →](./product/) |
| ✨ **Design** | 1 | [Browse →](./design/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [HKUDS/nanobot](./aiml/hkuds-nanobot.md) | ⭐ 40.6k | AI/ML |
| 2 | [armbian/build](./aiml/armbian-build.md) | ⭐ 5.2k | AI/ML |
| 3 | [zhayujie/CowAgent](./orchestration/zhayujie-cowagent.md) | ⭐ 43.6k | Orchestration |
| 4 | [stashapp/stash](./misc/stashapp-stash.md) | ⭐ 12.2k | Misc |
| 5 | [openshift/origin](./aiml/openshift-origin.md) | ⭐ 8.6k | AI/ML |
| 6 | [getsops/sops](./security/getsops-sops.md) | ⭐ 21.6k | Security |
| 7 | [rtk-ai/rtk](./aiml/rtk-ai-rtk.md) | ⭐ 32.7k | AI/ML |
| 8 | [evcc-io/evcc](./misc/evcc-io-evcc.md) | ⭐ 6.5k | Misc |
| 9 | [expo/expo](./frontend/expo-expo.md) | ⭐ 48.9k | Frontend |
| 10 | [mem0ai/mem0](./orchestration/mem0ai-mem0.md) | ⭐ 53.9k | Orchestration |

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
