# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **9263** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 3569 | [Browse →](./aiml/) |
| 📦 **Misc** | 1722 | [Browse →](./misc/) |
| 🎨 **Frontend** | 928 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 767 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 541 | [Browse →](./backend/) |
| 🔧 **DevTools** | 530 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 332 | [Browse →](./crypto/) |
| 📊 **Data** | 197 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 188 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 124 | [Browse →](./mobile/) |
| 💳 **Payments** | 114 | [Browse →](./payments/) |
| 📈 **Trading** | 94 | [Browse →](./trading/) |
| 🔐 **Security** | 85 | [Browse →](./security/) |
| ✨ **Design** | 32 | [Browse →](./design/) |
| 🎯 **Product** | 22 | [Browse →](./product/) |
| 🏷️ **Marketing** | 18 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [ruvnet/ruflo](./orchestration/ruvnet-ruflo.md) | ⭐ 33.7k | Orchestration |
| 2 | [SigmaHQ/sigma](./aiml/sigmahq-sigma.md) | ⭐ 10.4k | AI/ML |
| 3 | [wolfpld/tracy](./misc/wolfpld-tracy.md) | ⭐ 15.7k | Misc |
| 4 | [grafana/k6](./devtools/grafana-k6.md) | ⭐ 30.5k | DevTools |
| 5 | [microsoft/promptflow](./aiml/microsoft-promptflow.md) | ⭐ 11.1k | AI/ML |
| 6 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 7 | [ngosang/trackerslist](./misc/ngosang-trackerslist.md) | ⭐ 53.7k | Misc |
| 8 | [SigNoz/signoz](./frontend/signoz-signoz.md) | ⭐ 26.7k | Frontend |
| 9 | [dagster-io/dagster](./orchestration/dagster-io-dagster.md) | ⭐ 15.4k | Orchestration |
| 10 | [dependabot/dependabot-core](./devopsinfra/dependabot-dependabot-core.md) | ⭐ 5.6k | DevOps & Infra |

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
