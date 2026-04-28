# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **10635** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 4109 | [Browse →](./aiml/) |
| 📦 **Misc** | 2002 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1049 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 856 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 632 | [Browse →](./backend/) |
| 🔧 **DevTools** | 617 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 382 | [Browse →](./crypto/) |
| 📊 **Data** | 234 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 217 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 132 | [Browse →](./mobile/) |
| 💳 **Payments** | 123 | [Browse →](./payments/) |
| 📈 **Trading** | 106 | [Browse →](./trading/) |
| 🔐 **Security** | 95 | [Browse →](./security/) |
| ✨ **Design** | 36 | [Browse →](./design/) |
| 🎯 **Product** | 25 | [Browse →](./product/) |
| 🏷️ **Marketing** | 20 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [fatedier/frp](./backend/fatedier-frp.md) | ⭐ 106.1k | Backend |
| 2 | [coollabsio/coolify](./backend/coollabsio-coolify.md) | ⭐ 54.3k | Backend |
| 3 | [roboflow/supervision](./misc/roboflow-supervision.md) | ⭐ 38.2k | Misc |
| 4 | [CherryHQ/cherry-studio](./aiml/cherryhq-cherry-studio.md) | ⭐ 44.7k | AI/ML |
| 5 | [RIOT-OS/RIOT](./misc/riot-os-riot.md) | ⭐ 5.7k | Misc |
| 6 | [shadps4-emu/shadPS4](./frontend/shadps4-emu-shadps4.md) | ⭐ 30.9k | Frontend |
| 7 | [ollama/ollama](./aiml/ollama-ollama.md) | ⭐ 170.2k | AI/ML |
| 8 | [unslothai/unsloth](./aiml/unslothai-unsloth.md) | ⭐ 63.2k | AI/ML |
| 9 | [prometheus/alertmanager](./aiml/prometheus-alertmanager.md) | ⭐ 8.4k | AI/ML |
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
