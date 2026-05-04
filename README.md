# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **15896** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 5922 | [Browse →](./aiml/) |
| 📦 **Misc** | 3306 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1567 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1159 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 973 | [Browse →](./backend/) |
| 🔧 **DevTools** | 940 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 537 | [Browse →](./crypto/) |
| 📊 **Data** | 361 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 339 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 218 | [Browse →](./mobile/) |
| 💳 **Payments** | 165 | [Browse →](./payments/) |
| 📈 **Trading** | 163 | [Browse →](./trading/) |
| 🔐 **Security** | 130 | [Browse →](./security/) |
| ✨ **Design** | 53 | [Browse →](./design/) |
| 🎯 **Product** | 32 | [Browse →](./product/) |
| 🏷️ **Marketing** | 31 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [plankanban/planka](./frontend/plankanban-planka.md) | ⭐ 11.9k | Frontend |
| 2 | [HumanSignal/label-studio](./aiml/humansignal-label-studio.md) | ⭐ 27.2k | AI/ML |
| 3 | [alibaba/spring-cloud-alibaba](./frontend/alibaba-spring-cloud-alibaba.md) | ⭐ 29.1k | Frontend |
| 4 | [microsoft/presidio](./aiml/microsoft-presidio.md) | ⭐ 7.9k | AI/ML |
| 5 | [krzyzanowskim/CryptoSwift](./crypto/krzyzanowskim-cryptoswift.md) | ⭐ 10.5k | Crypto |
| 6 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 7 | [zitadel/zitadel](./aiml/zitadel-zitadel.md) | ⭐ 13.7k | AI/ML |
| 8 | [mvanhorn/last30days-skill](./trading/mvanhorn-last30days-skill.md) | ⭐ 24.7k | Trading |
| 9 | [goauthentik/authentik](./aiml/goauthentik-authentik.md) | ⭐ 21.3k | AI/ML |
| 10 | [PrefectHQ/prefect](./orchestration/prefecthq-prefect.md) | ⭐ 22.3k | Orchestration |

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
