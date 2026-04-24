# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **3153** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1190 | [Browse →](./aiml/) |
| 📦 **Misc** | 494 | [Browse →](./misc/) |
| 🎨 **Frontend** | 344 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 291 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 200 | [Browse →](./backend/) |
| 🔧 **DevTools** | 163 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 127 | [Browse →](./crypto/) |
| 📊 **Data** | 90 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 75 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 44 | [Browse →](./payments/) |
| 📱 **Mobile** | 41 | [Browse →](./mobile/) |
| 📈 **Trading** | 34 | [Browse →](./trading/) |
| 🔐 **Security** | 34 | [Browse →](./security/) |
| ✨ **Design** | 12 | [Browse →](./design/) |
| 🎯 **Product** | 11 | [Browse →](./product/) |
| 🏷️ **Marketing** | 3 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [k2-fsa/sherpa-onnx](./backend/k2-fsa-sherpa-onnx.md) | ⭐ 11.8k | Backend |
| 2 | [PaddlePaddle/PaddleOCR](./aiml/paddlepaddle-paddleocr.md) | ⭐ 76.4k | AI/ML |
| 3 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 4 | [comet-ml/opik](./orchestration/comet-ml-opik.md) | ⭐ 19k | Orchestration |
| 5 | [sktime/sktime](./aiml/sktime-sktime.md) | ⭐ 9.7k | AI/ML |
| 6 | [apache/seatunnel](./aiml/apache-seatunnel.md) | ⭐ 9.3k | AI/ML |
| 7 | [lobehub/lobehub](./orchestration/lobehub-lobehub.md) | ⭐ 75.6k | Orchestration |
| 8 | [goauthentik/authentik](./aiml/goauthentik-authentik.md) | ⭐ 21.1k | AI/ML |
| 9 | [unslothai/unsloth](./aiml/unslothai-unsloth.md) | ⭐ 62.8k | AI/ML |
| 10 | [dgtlmoon/changedetection.io](./backend/dgtlmoon-changedetection.io.md) | ⭐ 31.2k | Backend |

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
