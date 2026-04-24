# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **3691** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1411 | [Browse →](./aiml/) |
| 📦 **Misc** | 581 | [Browse →](./misc/) |
| 🎨 **Frontend** | 390 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 337 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 229 | [Browse →](./backend/) |
| 🔧 **DevTools** | 202 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 148 | [Browse →](./crypto/) |
| 📊 **Data** | 97 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 85 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 54 | [Browse →](./payments/) |
| 📱 **Mobile** | 50 | [Browse →](./mobile/) |
| 📈 **Trading** | 39 | [Browse →](./trading/) |
| 🔐 **Security** | 38 | [Browse →](./security/) |
| ✨ **Design** | 13 | [Browse →](./design/) |
| 🎯 **Product** | 12 | [Browse →](./product/) |
| 🏷️ **Marketing** | 5 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [assistant-ui/assistant-ui](./aiml/assistant-ui-assistant-ui.md) | ⭐ 9.7k | AI/ML |
| 2 | [semaphoreui/semaphore](./aiml/semaphoreui-semaphore.md) | ⭐ 13.5k | AI/ML |
| 3 | [D4Vinci/Scrapling](./aiml/d4vinci-scrapling.md) | ⭐ 38.6k | AI/ML |
| 4 | [catboost/catboost](./aiml/catboost-catboost.md) | ⭐ 8.9k | AI/ML |
| 5 | [ansible/awx](./frontend/ansible-awx.md) | ⭐ 15.4k | Frontend |
| 6 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 7 | [RocketChat/Rocket.Chat](./misc/rocketchat-rocket.chat.md) | ⭐ 45.2k | Misc |
| 8 | [lionsoul2014/ip2region](./devtools/lionsoul2014-ip2region.md) | ⭐ 19k | DevTools |
| 9 | [secdev/scapy](./security/secdev-scapy.md) | ⭐ 12.2k | Security |
| 10 | [casdoor/casdoor](./aiml/casdoor-casdoor.md) | ⭐ 13.5k | AI/ML |

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
