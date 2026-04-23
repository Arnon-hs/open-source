# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **2230** |
| 📁 **Categories** | **15** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 832 | [Browse →](./aiml/) |
| 📦 **Misc** | 379 | [Browse →](./misc/) |
| 🎨 **Frontend** | 250 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 194 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 140 | [Browse →](./backend/) |
| 🔧 **DevTools** | 109 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 89 | [Browse →](./crypto/) |
| 📊 **Data** | 68 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 51 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 32 | [Browse →](./mobile/) |
| 💳 **Payments** | 25 | [Browse →](./payments/) |
| 📈 **Trading** | 24 | [Browse →](./trading/) |
| 🔐 **Security** | 23 | [Browse →](./security/) |
| 🎯 **Product** | 8 | [Browse →](./product/) |
| ✨ **Design** | 6 | [Browse →](./design/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [microsoft/vcpkg](./misc/microsoft-vcpkg.md) | ⭐ 26.9k | Misc |
| 2 | [js-org/js.org](./aiml/js-org-js.org.md) | ⭐ 5.7k | AI/ML |
| 3 | [google/syzkaller](./aiml/google-syzkaller.md) | ⭐ 6.1k | AI/ML |
| 4 | [playframework/playframework](./aiml/playframework-playframework.md) | ⭐ 12.6k | AI/ML |
| 5 | [bytecodealliance/wasmtime](./misc/bytecodealliance-wasmtime.md) | ⭐ 17.9k | Misc |
| 6 | [gofiber/fiber](./backend/gofiber-fiber.md) | ⭐ 39.6k | Backend |
| 7 | [quay/clair](./aiml/quay-clair.md) | ⭐ 11k | AI/ML |
| 8 | [safishamsi/graphify](./aiml/safishamsi-graphify.md) | ⭐ 33.7k | AI/ML |
| 9 | [spree/spree](./backend/spree-spree.md) | ⭐ 15.4k | Backend |
| 10 | [PrefectHQ/prefect](./orchestration/prefecthq-prefect.md) | ⭐ 22.2k | Orchestration |

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
