# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **5659** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2188 | [Browse →](./aiml/) |
| 📦 **Misc** | 932 | [Browse →](./misc/) |
| 🎨 **Frontend** | 559 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 526 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 337 | [Browse →](./backend/) |
| 🔧 **DevTools** | 319 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 203 | [Browse →](./crypto/) |
| 📊 **Data** | 136 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 126 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 83 | [Browse →](./mobile/) |
| 💳 **Payments** | 80 | [Browse →](./payments/) |
| 📈 **Trading** | 62 | [Browse →](./trading/) |
| 🔐 **Security** | 59 | [Browse →](./security/) |
| ✨ **Design** | 23 | [Browse →](./design/) |
| 🎯 **Product** | 18 | [Browse →](./product/) |
| 🏷️ **Marketing** | 8 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [FFmpeg/FFmpeg](./misc/ffmpeg-ffmpeg.md) | ⭐ 59.3k | Misc |
| 2 | [ZoneMinder/zoneminder](./frontend/zoneminder-zoneminder.md) | ⭐ 5.8k | Frontend |
| 3 | [siteboon/claudecodeui](./aiml/siteboon-claudecodeui.md) | ⭐ 10.2k | AI/ML |
| 4 | [huggingface/datasets](./aiml/huggingface-datasets.md) | ⭐ 21.5k | AI/ML |
| 5 | [firebase/firebase-ios-sdk](./aiml/firebase-firebase-ios-sdk.md) | ⭐ 6.6k | AI/ML |
| 6 | [HeyPuter/puter](./aiml/heyputer-puter.md) | ⭐ 40.7k | AI/ML |
| 7 | [dariubs/GoBooks](./product/dariubs-gobooks.md) | ⭐ 19.4k | Product |
| 8 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 9 | [curl/curl](./aiml/curl-curl.md) | ⭐ 41.4k | AI/ML |
| 10 | [onnx/onnx](./aiml/onnx-onnx.md) | ⭐ 20.7k | AI/ML |

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
