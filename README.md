# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **12735** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 4855 | [Browse →](./aiml/) |
| 📦 **Misc** | 2488 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1235 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 984 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 773 | [Browse →](./backend/) |
| 🔧 **DevTools** | 754 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 458 | [Browse →](./crypto/) |
| 📊 **Data** | 289 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 279 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 157 | [Browse →](./mobile/) |
| 💳 **Payments** | 134 | [Browse →](./payments/) |
| 📈 **Trading** | 132 | [Browse →](./trading/) |
| 🔐 **Security** | 110 | [Browse →](./security/) |
| ✨ **Design** | 37 | [Browse →](./design/) |
| 🎯 **Product** | 27 | [Browse →](./product/) |
| 🏷️ **Marketing** | 23 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [hasura/graphql-engine](./aiml/hasura-graphql-engine.md) | ⭐ 32k | AI/ML |
| 2 | [appium/appium](./frontend/appium-appium.md) | ⭐ 21.5k | Frontend |
| 3 | [openshift/origin](./aiml/openshift-origin.md) | ⭐ 8.6k | AI/ML |
| 4 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 5 | [bpftrace/bpftrace](./misc/bpftrace-bpftrace.md) | ⭐ 10.1k | Misc |
| 6 | [frappe/frappe](./aiml/frappe-frappe.md) | ⭐ 10k | AI/ML |
| 7 | [laramies/theHarvester](./aiml/laramies-theharvester.md) | ⭐ 16.1k | AI/ML |
| 8 | [mudler/LocalAI](./aiml/mudler-localai.md) | ⭐ 45.9k | AI/ML |
| 9 | [volcengine/OpenViking](./aiml/volcengine-openviking.md) | ⭐ 23.3k | AI/ML |
| 10 | [novuhq/novu](./aiml/novuhq-novu.md) | ⭐ 38.9k | AI/ML |

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
