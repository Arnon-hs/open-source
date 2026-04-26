# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **7793** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 3000 | [Browse →](./aiml/) |
| 📦 **Misc** | 1447 | [Browse →](./misc/) |
| 🎨 **Frontend** | 786 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 668 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 441 | [Browse →](./backend/) |
| 🔧 **DevTools** | 437 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 265 | [Browse →](./crypto/) |
| 📊 **Data** | 170 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 145 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 112 | [Browse →](./mobile/) |
| 💳 **Payments** | 108 | [Browse →](./payments/) |
| 📈 **Trading** | 79 | [Browse →](./trading/) |
| 🔐 **Security** | 74 | [Browse →](./security/) |
| ✨ **Design** | 27 | [Browse →](./design/) |
| 🎯 **Product** | 21 | [Browse →](./product/) |
| 🏷️ **Marketing** | 13 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [arendst/Tasmota](./frontend/arendst-tasmota.md) | ⭐ 24.3k | Frontend |
| 2 | [lichess-org/lila](./backend/lichess-org-lila.md) | ⭐ 18.1k | Backend |
| 3 | [rclone/rclone](./aiml/rclone-rclone.md) | ⭐ 56.9k | AI/ML |
| 4 | [secdev/scapy](./security/secdev-scapy.md) | ⭐ 12.2k | Security |
| 5 | [RT-Thread/rt-thread](./aiml/rt-thread-rt-thread.md) | ⭐ 11.9k | AI/ML |
| 6 | [tw93/Mole](./aiml/tw93-mole.md) | ⭐ 49.2k | AI/ML |
| 7 | [langchain-ai/langgraph](./orchestration/langchain-ai-langgraph.md) | ⭐ 30.5k | Orchestration |
| 8 | [ChatLab/ChatLab](./aiml/chatlab-chatlab.md) | ⭐ 6.1k | AI/ML |
| 9 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 10 | [zeroclaw-labs/zeroclaw](./aiml/zeroclaw-labs-zeroclaw.md) | ⭐ 30.7k | AI/ML |

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
