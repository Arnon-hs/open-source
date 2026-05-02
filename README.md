# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **14704** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 5508 | [Browse →](./aiml/) |
| 📦 **Misc** | 2991 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1434 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1093 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 903 | [Browse →](./backend/) |
| 🔧 **DevTools** | 882 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 513 | [Browse →](./crypto/) |
| 📊 **Data** | 335 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 319 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 195 | [Browse →](./mobile/) |
| 💳 **Payments** | 156 | [Browse →](./payments/) |
| 📈 **Trading** | 151 | [Browse →](./trading/) |
| 🔐 **Security** | 120 | [Browse →](./security/) |
| ✨ **Design** | 47 | [Browse →](./design/) |
| 🎯 **Product** | 29 | [Browse →](./product/) |
| 🏷️ **Marketing** | 28 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [datawhalechina/all-in-rag](./orchestration/datawhalechina-all-in-rag.md) | ⭐ 6.9k | Orchestration |
| 2 | [filamentphp/filament](./aiml/filamentphp-filament.md) | ⭐ 30.5k | AI/ML |
| 3 | [luanti-org/luanti](./devtools/luanti-org-luanti.md) | ⭐ 12.8k | DevTools |
| 4 | [hellodigua/ChatLab](./aiml/hellodigua-chatlab.md) | ⭐ 6.2k | AI/ML |
| 5 | [mlflow/mlflow](./orchestration/mlflow-mlflow.md) | ⭐ 25.7k | Orchestration |
| 6 | [immich-app/immich](./mobile/immich-app-immich.md) | ⭐ 99.5k | Mobile |
| 7 | [rapidsai/cudf](./aiml/rapidsai-cudf.md) | ⭐ 9.6k | AI/ML |
| 8 | [gpakosz/.tmux](./aiml/gpakosz-.tmux.md) | ⭐ 24.8k | AI/ML |
| 9 | [k2-fsa/sherpa-onnx](./backend/k2-fsa-sherpa-onnx.md) | ⭐ 12k | Backend |
| 10 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |

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
