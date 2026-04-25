# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **5562** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2158 | [Browse →](./aiml/) |
| 📦 **Misc** | 911 | [Browse →](./misc/) |
| 🎨 **Frontend** | 549 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 520 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 332 | [Browse →](./backend/) |
| 🔧 **DevTools** | 311 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 200 | [Browse →](./crypto/) |
| 📊 **Data** | 134 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 125 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 80 | [Browse →](./mobile/) |
| 💳 **Payments** | 79 | [Browse →](./payments/) |
| 📈 **Trading** | 61 | [Browse →](./trading/) |
| 🔐 **Security** | 55 | [Browse →](./security/) |
| ✨ **Design** | 23 | [Browse →](./design/) |
| 🎯 **Product** | 17 | [Browse →](./product/) |
| 🏷️ **Marketing** | 7 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [FFmpeg/FFmpeg](./misc/ffmpeg-ffmpeg.md) | ⭐ 59.3k | Misc |
| 2 | [ZoneMinder/zoneminder](./frontend/zoneminder-zoneminder.md) | ⭐ 5.8k | Frontend |
| 3 | [huggingface/datasets](./aiml/huggingface-datasets.md) | ⭐ 21.5k | AI/ML |
| 4 | [firebase/firebase-ios-sdk](./aiml/firebase-firebase-ios-sdk.md) | ⭐ 6.6k | AI/ML |
| 5 | [curl/curl](./aiml/curl-curl.md) | ⭐ 41.4k | AI/ML |
| 6 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 7 | [onnx/onnx](./aiml/onnx-onnx.md) | ⭐ 20.7k | AI/ML |
| 8 | [projectdiscovery/nuclei](./aiml/projectdiscovery-nuclei.md) | ⭐ 28.1k | AI/ML |
| 9 | [casdoor/casdoor](./aiml/casdoor-casdoor.md) | ⭐ 13.5k | AI/ML |
| 10 | [astral-sh/ruff](./frontend/astral-sh-ruff.md) | ⭐ 47.2k | Frontend |

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
