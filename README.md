# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **2059** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 786 | [Browse →](./aiml/) |
| 📦 **Misc** | 350 | [Browse →](./misc/) |
| 🎨 **Frontend** | 209 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 197 | [Browse →](./orchestration/) |
| 🔧 **DevTools** | 105 | [Browse →](./devtools/) |
| ⚙️ **Backend** | 104 | [Browse →](./backend/) |
| ⛓️ **Crypto** | 88 | [Browse →](./crypto/) |
| 📊 **Data** | 58 | [Browse →](./data/) |
| 💳 **Payments** | 53 | [Browse →](./payments/) |
| 📈 **Trading** | 32 | [Browse →](./trading/) |
| 🚀 **DevOps & Infra** | 28 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 24 | [Browse →](./mobile/) |
| 🔐 **Security** | 13 | [Browse →](./security/) |
| 🎯 **Product** | 6 | [Browse →](./product/) |
| ✨ **Design** | 5 | [Browse →](./design/) |
| 🏷️ **Marketing** | 1 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [oraios/serena](./aiml/oraios-serena.md) | ⭐ 23.9k | AI/ML |
| 2 | [louislam/uptime-kuma](./frontend/louislam-uptime-kuma.md) | ⭐ 86.4k | Frontend |
| 3 | [skypilot-org/skypilot](./aiml/skypilot-org-skypilot.md) | ⭐ 9.9k | AI/ML |
| 4 | [pwndbg/pwndbg](./misc/pwndbg-pwndbg.md) | ⭐ 10.4k | Misc |
| 5 | [cvxpy/cvxpy](./misc/cvxpy-cvxpy.md) | ⭐ 6.2k | Misc |
| 6 | [invoke-ai/InvokeAI](./aiml/invoke-ai-invokeai.md) | ⭐ 27.1k | AI/ML |
| 7 | [astral-sh/ruff](./frontend/astral-sh-ruff.md) | ⭐ 47.4k | Frontend |
| 8 | [ArduPilot/ardupilot](./misc/ardupilot-ardupilot.md) | ⭐ 15k | Misc |
| 9 | [bpftrace/bpftrace](./misc/bpftrace-bpftrace.md) | ⭐ 10.1k | Misc |
| 10 | [giampaolo/psutil](./misc/giampaolo-psutil.md) | ⭐ 11.2k | Misc |

## 🚀 How it works

```mermaid
graph LR
  A[GitHub · HN · Reddit · PH] --> B[RepoScout]
  B --> C[Score · Dedupe · Categorize]
  C --> D[LLM Summarize]
  D --> E[PostgreSQL DB]
  D --> F[This Catalog]
```

1. **Discover** — 4 sources pulled in parallel
2. **Score** — weighted: stars, forks, recency, topics, source trust
3. **Categorize** — rule-based + LLM-assisted tagging
4. **Summarize** — concise bilingual (EN/RU) summaries via LLM
5. **Sync** — markdown committed here, metadata upserted to PostgreSQL

## 🛠️ Self-host

```bash
git clone https://github.com/kirbudilov01/reposearchengine
cp .env.example .env
# Set LLM_PROVIDER, CATALOG_REPO_PATH, DATABASE_URL, ...
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
