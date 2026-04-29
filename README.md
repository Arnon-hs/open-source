# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **10844** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 4181 | [Browse →](./aiml/) |
| 📦 **Misc** | 2051 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1066 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 870 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 650 | [Browse →](./backend/) |
| 🔧 **DevTools** | 633 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 390 | [Browse →](./crypto/) |
| 📊 **Data** | 236 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 224 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 134 | [Browse →](./mobile/) |
| 💳 **Payments** | 124 | [Browse →](./payments/) |
| 📈 **Trading** | 107 | [Browse →](./trading/) |
| 🔐 **Security** | 96 | [Browse →](./security/) |
| ✨ **Design** | 36 | [Browse →](./design/) |
| 🎯 **Product** | 25 | [Browse →](./product/) |
| 🏷️ **Marketing** | 21 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [github/awesome-copilot](./orchestration/github-awesome-copilot.md) | ⭐ 31.5k | Orchestration |
| 2 | [qax-os/excelize](./aiml/qax-os-excelize.md) | ⭐ 20.5k | AI/ML |
| 3 | [expo/expo](./frontend/expo-expo.md) | ⭐ 49.1k | Frontend |
| 4 | [envoyproxy/envoy](./misc/envoyproxy-envoy.md) | ⭐ 27.9k | Misc |
| 5 | [fatedier/frp](./backend/fatedier-frp.md) | ⭐ 106.1k | Backend |
| 6 | [coollabsio/coolify](./backend/coollabsio-coolify.md) | ⭐ 54.3k | Backend |
| 7 | [promptfoo/promptfoo](./aiml/promptfoo-promptfoo.md) | ⭐ 20.7k | AI/ML |
| 8 | [projectdiscovery/nuclei-templates](./security/projectdiscovery-nuclei-templates.md) | ⭐ 12.3k | Security |
| 9 | [playframework/playframework](./aiml/playframework-playframework.md) | ⭐ 12.6k | AI/ML |
| 10 | [roboflow/supervision](./misc/roboflow-supervision.md) | ⭐ 38.2k | Misc |

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
