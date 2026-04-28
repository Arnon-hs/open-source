# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **9514** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 3657 | [Browse →](./aiml/) |
| 📦 **Misc** | 1779 | [Browse →](./misc/) |
| 🎨 **Frontend** | 956 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 790 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 555 | [Browse →](./backend/) |
| 🔧 **DevTools** | 545 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 339 | [Browse →](./crypto/) |
| 📊 **Data** | 206 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 191 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 126 | [Browse →](./mobile/) |
| 💳 **Payments** | 115 | [Browse →](./payments/) |
| 📈 **Trading** | 96 | [Browse →](./trading/) |
| 🔐 **Security** | 87 | [Browse →](./security/) |
| ✨ **Design** | 32 | [Browse →](./design/) |
| 🎯 **Product** | 22 | [Browse →](./product/) |
| 🏷️ **Marketing** | 18 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [temporalio/temporal](./orchestration/temporalio-temporal.md) | ⭐ 19.9k | Orchestration |
| 2 | [grpc/grpc-go](./backend/grpc-grpc-go.md) | ⭐ 22.9k | Backend |
| 3 | [ImageMagick/ImageMagick](./frontend/imagemagick-imagemagick.md) | ⭐ 16.3k | Frontend |
| 4 | [sonic-pi-net/sonic-pi](./misc/sonic-pi-net-sonic-pi.md) | ⭐ 11.8k | Misc |
| 5 | [wkentaro/labelme](./aiml/wkentaro-labelme.md) | ⭐ 15.8k | AI/ML |
| 6 | [is-a-dev/register](./aiml/is-a-dev-register.md) | ⭐ 10.2k | AI/ML |
| 7 | [bytedance/UI-TARS-desktop](./aiml/bytedance-ui-tars-desktop.md) | ⭐ 29.5k | AI/ML |
| 8 | [istio/istio](./frontend/istio-istio.md) | ⭐ 38.1k | Frontend |
| 9 | [martin-ger/esp_wifi_repeater](./misc/martin-ger-esp-wifi-repeater.md) | ⭐ 5.2k | Misc |
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
