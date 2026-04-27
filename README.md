# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **7957** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 3060 | [Browse →](./aiml/) |
| 📦 **Misc** | 1480 | [Browse →](./misc/) |
| 🎨 **Frontend** | 803 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 677 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 460 | [Browse →](./backend/) |
| 🔧 **DevTools** | 444 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 274 | [Browse →](./crypto/) |
| 📊 **Data** | 171 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 150 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 112 | [Browse →](./mobile/) |
| 💳 **Payments** | 111 | [Browse →](./payments/) |
| 📈 **Trading** | 79 | [Browse →](./trading/) |
| 🔐 **Security** | 74 | [Browse →](./security/) |
| ✨ **Design** | 28 | [Browse →](./design/) |
| 🎯 **Product** | 21 | [Browse →](./product/) |
| 🏷️ **Marketing** | 13 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [meshtastic/firmware](./misc/meshtastic-firmware.md) | ⭐ 7.4k | Misc |
| 2 | [pubkey/rxdb](./aiml/pubkey-rxdb.md) | ⭐ 23.2k | AI/ML |
| 3 | [reflex-dev/reflex](./frontend/reflex-dev-reflex.md) | ⭐ 28.3k | Frontend |
| 4 | [volcengine/OpenViking](./aiml/volcengine-openviking.md) | ⭐ 23.1k | AI/ML |
| 5 | [ansible/awx](./frontend/ansible-awx.md) | ⭐ 15.4k | Frontend |
| 6 | [microsoft/RD-Agent](./aiml/microsoft-rd-agent.md) | ⭐ 12.7k | AI/ML |
| 7 | [TanStack/query](./frontend/tanstack-query.md) | ⭐ 49.2k | Frontend |
| 8 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 9 | [arendst/Tasmota](./frontend/arendst-tasmota.md) | ⭐ 24.3k | Frontend |
| 10 | [secdev/scapy](./security/secdev-scapy.md) | ⭐ 12.2k | Security |

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
