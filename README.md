# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **7600** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2917 | [Browse →](./aiml/) |
| 📦 **Misc** | 1411 | [Browse →](./misc/) |
| 🎨 **Frontend** | 766 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 656 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 433 | [Browse →](./backend/) |
| 🔧 **DevTools** | 425 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 258 | [Browse →](./crypto/) |
| 📊 **Data** | 169 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 143 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 111 | [Browse →](./mobile/) |
| 💳 **Payments** | 105 | [Browse →](./payments/) |
| 📈 **Trading** | 76 | [Browse →](./trading/) |
| 🔐 **Security** | 72 | [Browse →](./security/) |
| ✨ **Design** | 26 | [Browse →](./design/) |
| 🎯 **Product** | 20 | [Browse →](./product/) |
| 🏷️ **Marketing** | 12 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [avajs/ava](./devtools/avajs-ava.md) | ⭐ 20.8k | DevTools |
| 2 | [TanStack/table](./frontend/tanstack-table.md) | ⭐ 27.9k | Frontend |
| 3 | [danny-avila/LibreChat](./orchestration/danny-avila-librechat.md) | ⭐ 36.1k | Orchestration |
| 4 | [n8n-io/n8n](./aiml/n8n-io-n8n.md) | ⭐ 185.7k | AI/ML |
| 5 | [calcom/cal.diy](./aiml/calcom-cal.diy.md) | ⭐ 42.1k | AI/ML |
| 6 | [sqlmapproject/sqlmap](./devtools/sqlmapproject-sqlmap.md) | ⭐ 37.1k | DevTools |
| 7 | [btcpayserver/btcpayserver](./crypto/btcpayserver-btcpayserver.md) | ⭐ 7.5k | Crypto |
| 8 | [BasedHardware/omi](./aiml/basedhardware-omi.md) | ⭐ 12.2k | AI/ML |
| 9 | [jeecgboot/JeecgBoot](./orchestration/jeecgboot-jeecgboot.md) | ⭐ 46k | Orchestration |
| 10 | [winsiderss/systeminformer](./security/winsiderss-systeminformer.md) | ⭐ 14.1k | Security |

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
