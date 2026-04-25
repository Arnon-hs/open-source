# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **4411** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1702 | [Browse →](./aiml/) |
| 📦 **Misc** | 689 | [Browse →](./misc/) |
| 🎨 **Frontend** | 451 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 418 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 264 | [Browse →](./backend/) |
| 🔧 **DevTools** | 244 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 172 | [Browse →](./crypto/) |
| 📊 **Data** | 114 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 102 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 62 | [Browse →](./payments/) |
| 📱 **Mobile** | 61 | [Browse →](./mobile/) |
| 📈 **Trading** | 48 | [Browse →](./trading/) |
| 🔐 **Security** | 46 | [Browse →](./security/) |
| ✨ **Design** | 18 | [Browse →](./design/) |
| 🎯 **Product** | 14 | [Browse →](./product/) |
| 🏷️ **Marketing** | 6 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [awslabs/mcp](./backend/awslabs-mcp.md) | ⭐ 8.9k | Backend |
| 2 | [triggerdotdev/trigger.dev](./orchestration/triggerdotdev-trigger.dev.md) | ⭐ 14.7k | Orchestration |
| 3 | [hoochanlon/hamuleite](./misc/hoochanlon-hamuleite.md) | ⭐ 9.4k | Misc |
| 4 | [activepieces/activepieces](./aiml/activepieces-activepieces.md) | ⭐ 21.9k | AI/ML |
| 5 | [playframework/playframework](./aiml/playframework-playframework.md) | ⭐ 12.6k | AI/ML |
| 6 | [recharts/recharts](./crypto/recharts-recharts.md) | ⭐ 27k | Crypto |
| 7 | [huggingface/pytorch-image-models](./aiml/huggingface-pytorch-image-models.md) | ⭐ 36.7k | AI/ML |
| 8 | [bytecodealliance/wasmtime](./misc/bytecodealliance-wasmtime.md) | ⭐ 17.9k | Misc |
| 9 | [mcp-use/mcp-use](./aiml/mcp-use-mcp-use.md) | ⭐ 9.8k | AI/ML |
| 10 | [openvinotoolkit/openvino](./aiml/openvinotoolkit-openvino.md) | ⭐ 10.1k | AI/ML |

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
