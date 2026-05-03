# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **15616** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 5825 | [Browse →](./aiml/) |
| 📦 **Misc** | 3230 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1527 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1147 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 956 | [Browse →](./backend/) |
| 🔧 **DevTools** | 930 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 529 | [Browse →](./crypto/) |
| 📊 **Data** | 354 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 336 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 213 | [Browse →](./mobile/) |
| 💳 **Payments** | 164 | [Browse →](./payments/) |
| 📈 **Trading** | 164 | [Browse →](./trading/) |
| 🔐 **Security** | 128 | [Browse →](./security/) |
| ✨ **Design** | 52 | [Browse →](./design/) |
| 🏷️ **Marketing** | 31 | [Browse →](./marketing/) |
| 🎯 **Product** | 30 | [Browse →](./product/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [Laravel-Lang/lang](./payments/laravel-lang-lang.md) | ⭐ 7.8k | Payments |
| 2 | [reactos/reactos](./frontend/reactos-reactos.md) | ⭐ 17.5k | Frontend |
| 3 | [ShareX/ShareX](./product/sharex-sharex.md) | ⭐ 37k | Product |
| 4 | [flameshot-org/flameshot](./frontend/flameshot-org-flameshot.md) | ⭐ 29.8k | Frontend |
| 5 | [Budibase/budibase](./orchestration/budibase-budibase.md) | ⭐ 27.9k | Orchestration |
| 6 | [oapi-codegen/oapi-codegen](./backend/oapi-codegen-oapi-codegen.md) | ⭐ 8.3k | Backend |
| 7 | [langchain-ai/open-swe](./orchestration/langchain-ai-open-swe.md) | ⭐ 9.7k | Orchestration |
| 8 | [openvinotoolkit/openvino](./aiml/openvinotoolkit-openvino.md) | ⭐ 10.2k | AI/ML |
| 9 | [krzyzanowskim/CryptoSwift](./crypto/krzyzanowskim-cryptoswift.md) | ⭐ 10.5k | Crypto |
| 10 | [rook/rook](./orchestration/rook-rook.md) | ⭐ 13.5k | Orchestration |

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
