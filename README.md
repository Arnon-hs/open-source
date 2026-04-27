# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **8047** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 3095 | [Browse →](./aiml/) |
| 📦 **Misc** | 1490 | [Browse →](./misc/) |
| 🎨 **Frontend** | 811 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 688 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 469 | [Browse →](./backend/) |
| 🔧 **DevTools** | 451 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 276 | [Browse →](./crypto/) |
| 📊 **Data** | 173 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 153 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 112 | [Browse →](./mobile/) |
| 💳 **Payments** | 111 | [Browse →](./payments/) |
| 📈 **Trading** | 81 | [Browse →](./trading/) |
| 🔐 **Security** | 75 | [Browse →](./security/) |
| ✨ **Design** | 28 | [Browse →](./design/) |
| 🎯 **Product** | 21 | [Browse →](./product/) |
| 🏷️ **Marketing** | 13 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [freqtrade/freqtrade](./crypto/freqtrade-freqtrade.md) | ⭐ 49.5k | Crypto |
| 2 | [apache/shardingsphere](./data/apache-shardingsphere.md) | ⭐ 20.7k | Data |
| 3 | [meshtastic/firmware](./misc/meshtastic-firmware.md) | ⭐ 7.4k | Misc |
| 4 | [avajs/ava](./devtools/avajs-ava.md) | ⭐ 20.8k | DevTools |
| 5 | [calcom/cal.diy](./aiml/calcom-cal.diy.md) | ⭐ 42.1k | AI/ML |
| 6 | [agentscope-ai/agentscope](./orchestration/agentscope-ai-agentscope.md) | ⭐ 24.4k | Orchestration |
| 7 | [microsoft/RD-Agent](./aiml/microsoft-rd-agent.md) | ⭐ 12.7k | AI/ML |
| 8 | [sharkdp/bat](./devtools/sharkdp-bat.md) | ⭐ 58.6k | DevTools |
| 9 | [danny-avila/LibreChat](./orchestration/danny-avila-librechat.md) | ⭐ 36.1k | Orchestration |
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
