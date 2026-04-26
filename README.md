# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **6302** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2417 | [Browse →](./aiml/) |
| 📦 **Misc** | 1097 | [Browse →](./misc/) |
| 🎨 **Frontend** | 627 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 568 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 370 | [Browse →](./backend/) |
| 🔧 **DevTools** | 349 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 224 | [Browse →](./crypto/) |
| 📊 **Data** | 150 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 130 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 97 | [Browse →](./mobile/) |
| 💳 **Payments** | 91 | [Browse →](./payments/) |
| 🔐 **Security** | 66 | [Browse →](./security/) |
| 📈 **Trading** | 63 | [Browse →](./trading/) |
| ✨ **Design** | 25 | [Browse →](./design/) |
| 🎯 **Product** | 19 | [Browse →](./product/) |
| 🏷️ **Marketing** | 9 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [simple-icons/simple-icons](./design/simple-icons-simple-icons.md) | ⭐ 25k | Design |
| 2 | [ngosang/trackerslist](./misc/ngosang-trackerslist.md) | ⭐ 53.6k | Misc |
| 3 | [duplicati/duplicati](./aiml/duplicati-duplicati.md) | ⭐ 14.5k | AI/ML |
| 4 | [WinMerge/winmerge](./misc/winmerge-winmerge.md) | ⭐ 8.7k | Misc |
| 5 | [ImageMagick/ImageMagick](./frontend/imagemagick-imagemagick.md) | ⭐ 16.3k | Frontend |
| 6 | [BlinkDL/RWKV-LM](./aiml/blinkdl-rwkv-lm.md) | ⭐ 14.5k | AI/ML |
| 7 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 8 | [spree/spree](./backend/spree-spree.md) | ⭐ 15.4k | Backend |
| 9 | [ultralytics/ultralytics](./devtools/ultralytics-ultralytics.md) | ⭐ 56.4k | DevTools |
| 10 | [seaweedfs/seaweedfs](./aiml/seaweedfs-seaweedfs.md) | ⭐ 31.7k | AI/ML |

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
