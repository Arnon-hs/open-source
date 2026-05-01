# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **13873** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 5235 | [Browse →](./aiml/) |
| 📦 **Misc** | 2775 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1349 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1043 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 852 | [Browse →](./backend/) |
| 🔧 **DevTools** | 827 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 488 | [Browse →](./crypto/) |
| 📊 **Data** | 318 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 304 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 173 | [Browse →](./mobile/) |
| 💳 **Payments** | 151 | [Browse →](./payments/) |
| 📈 **Trading** | 142 | [Browse →](./trading/) |
| 🔐 **Security** | 117 | [Browse →](./security/) |
| ✨ **Design** | 44 | [Browse →](./design/) |
| 🎯 **Product** | 29 | [Browse →](./product/) |
| 🏷️ **Marketing** | 26 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [VoltAgent/awesome-design-md](./aiml/voltagent-awesome-design-md.md) | ⭐ 69.1k | AI/ML |
| 2 | [influxdata/influxdb](./frontend/influxdata-influxdb.md) | ⭐ 31.5k | Frontend |
| 3 | [argoproj/argo-cd](./devopsinfra/argoproj-argo-cd.md) | ⭐ 22.8k | DevOps & Infra |
| 4 | [zalando/postgres-operator](./data/zalando-postgres-operator.md) | ⭐ 5.1k | Data |
| 5 | [ruby/ruby](./misc/ruby-ruby.md) | ⭐ 23.6k | Misc |
| 6 | [LizardByte/Sunshine](./aiml/lizardbyte-sunshine.md) | ⭐ 36.6k | AI/ML |
| 7 | [future-architect/vuls](./aiml/future-architect-vuls.md) | ⭐ 12.1k | AI/ML |
| 8 | [shadps4-emu/shadPS4](./frontend/shadps4-emu-shadps4.md) | ⭐ 31k | Frontend |
| 9 | [pubkey/rxdb](./aiml/pubkey-rxdb.md) | ⭐ 23.2k | AI/ML |
| 10 | [Anil-matcha/Open-Generative-AI](./aiml/anil-matcha-open-generative-ai.md) | ⭐ 10.6k | AI/ML |

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
