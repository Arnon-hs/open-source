# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **5148** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2001 | [Browse →](./aiml/) |
| 📦 **Misc** | 823 | [Browse →](./misc/) |
| 🎨 **Frontend** | 508 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 494 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 303 | [Browse →](./backend/) |
| 🔧 **DevTools** | 285 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 183 | [Browse →](./crypto/) |
| 📊 **Data** | 128 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 117 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 78 | [Browse →](./payments/) |
| 📱 **Mobile** | 73 | [Browse →](./mobile/) |
| 📈 **Trading** | 57 | [Browse →](./trading/) |
| 🔐 **Security** | 53 | [Browse →](./security/) |
| ✨ **Design** | 22 | [Browse →](./design/) |
| 🎯 **Product** | 17 | [Browse →](./product/) |
| 🏷️ **Marketing** | 6 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [ansible/awx](./frontend/ansible-awx.md) | ⭐ 15.4k | Frontend |
| 2 | [google/langextract](./aiml/google-langextract.md) | ⭐ 35.8k | AI/ML |
| 3 | [graphhopper/graphhopper](./backend/graphhopper-graphhopper.md) | ⭐ 6.4k | Backend |
| 4 | [mumble-voip/mumble](./backend/mumble-voip-mumble.md) | ⭐ 8k | Backend |
| 5 | [apache/casbin](./aiml/apache-casbin.md) | ⭐ 20k | AI/ML |
| 6 | [VoltAgent/awesome-agent-skills](./orchestration/voltagent-awesome-agent-skills.md) | ⭐ 18.7k | Orchestration |
| 7 | [caddyserver/caddy](./backend/caddyserver-caddy.md) | ⭐ 71.8k | Backend |
| 8 | [facebook/react-native](./frontend/facebook-react-native.md) | ⭐ 125.7k | Frontend |
| 9 | [karatelabs/karate](./backend/karatelabs-karate.md) | ⭐ 8.8k | Backend |
| 10 | [expo/expo](./frontend/expo-expo.md) | ⭐ 49k | Frontend |

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
