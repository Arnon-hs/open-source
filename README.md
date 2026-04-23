# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **1770** |
| 📁 **Categories** | **15** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 670 | [Browse →](./aiml/) |
| 📦 **Misc** | 293 | [Browse →](./misc/) |
| 🎨 **Frontend** | 192 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 160 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 103 | [Browse →](./backend/) |
| 🔧 **DevTools** | 88 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 76 | [Browse →](./crypto/) |
| 📊 **Data** | 50 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 43 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 27 | [Browse →](./mobile/) |
| 💳 **Payments** | 23 | [Browse →](./payments/) |
| 📈 **Trading** | 21 | [Browse →](./trading/) |
| 🔐 **Security** | 15 | [Browse →](./security/) |
| 🎯 **Product** | 6 | [Browse →](./product/) |
| ✨ **Design** | 3 | [Browse →](./design/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [vuetifyjs/vuetify](./frontend/vuetifyjs-vuetify.md) | ⭐ 41k | Frontend |
| 2 | [ansible/awx](./frontend/ansible-awx.md) | ⭐ 15.4k | Frontend |
| 3 | [quic-go/quic-go](./frontend/quic-go-quic-go.md) | ⭐ 11.5k | Frontend |
| 4 | [loopbackio/loopback-next](./frontend/loopbackio-loopback-next.md) | ⭐ 5.1k | Frontend |
| 5 | [botpress/botpress](./orchestration/botpress-botpress.md) | ⭐ 14.6k | Orchestration |
| 6 | [xtermjs/xterm.js](./misc/xtermjs-xterm.js.md) | ⭐ 20.4k | Misc |
| 7 | [elie222/inbox-zero](./aiml/elie222-inbox-zero.md) | ⭐ 10.5k | AI/ML |
| 8 | [outline/outline](./frontend/outline-outline.md) | ⭐ 38.2k | Frontend |
| 9 | [ccxt/ccxt](./crypto/ccxt-ccxt.md) | ⭐ 42k | Crypto |
| 10 | [woocommerce/woocommerce](./frontend/woocommerce-woocommerce.md) | ⭐ 10.3k | Frontend |

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
