# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **975** |
| 📁 **Categories** | **15** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 356 | [Browse →](./aiml/) |
| 📦 **Misc** | 192 | [Browse →](./misc/) |
| 🎨 **Frontend** | 109 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 72 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 57 | [Browse →](./backend/) |
| 🔧 **DevTools** | 39 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 38 | [Browse →](./crypto/) |
| 📊 **Data** | 30 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 23 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 21 | [Browse →](./mobile/) |
| 📈 **Trading** | 13 | [Browse →](./trading/) |
| 💳 **Payments** | 11 | [Browse →](./payments/) |
| 🔐 **Security** | 8 | [Browse →](./security/) |
| 🎯 **Product** | 5 | [Browse →](./product/) |
| ✨ **Design** | 1 | [Browse →](./design/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [winsiderss/systeminformer](./security/winsiderss-systeminformer.md) | ⭐ 14k | Security |
| 2 | [comet-ml/opik](./orchestration/comet-ml-opik.md) | ⭐ 19k | Orchestration |
| 3 | [dgtlmoon/changedetection.io](./backend/dgtlmoon-changedetection.io.md) | ⭐ 31.2k | Backend |
| 4 | [community-scripts/ProxmoxVE](./aiml/community-scripts-proxmoxve.md) | ⭐ 27.7k | AI/ML |
| 5 | [electerm/electerm](./aiml/electerm-electerm.md) | ⭐ 14k | AI/ML |
| 6 | [kovidgoyal/kitty](./misc/kovidgoyal-kitty.md) | ⭐ 32.5k | Misc |
| 7 | [PowerShell/PowerShell](./misc/powershell-powershell.md) | ⭐ 52.6k | Misc |
| 8 | [caddyserver/caddy](./backend/caddyserver-caddy.md) | ⭐ 71.8k | Backend |
| 9 | [krzyzanowskim/CryptoSwift](./crypto/krzyzanowskim-cryptoswift.md) | ⭐ 10.5k | Crypto |
| 10 | [renovatebot/renovate](./devtools/renovatebot-renovate.md) | ⭐ 21.3k | DevTools |

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
