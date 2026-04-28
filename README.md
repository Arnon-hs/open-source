# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **9379** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 3612 | [Browse →](./aiml/) |
| 📦 **Misc** | 1752 | [Browse →](./misc/) |
| 🎨 **Frontend** | 943 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 775 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 548 | [Browse →](./backend/) |
| 🔧 **DevTools** | 536 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 335 | [Browse →](./crypto/) |
| 📊 **Data** | 199 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 188 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 124 | [Browse →](./mobile/) |
| 💳 **Payments** | 115 | [Browse →](./payments/) |
| 📈 **Trading** | 95 | [Browse →](./trading/) |
| 🔐 **Security** | 85 | [Browse →](./security/) |
| ✨ **Design** | 32 | [Browse →](./design/) |
| 🎯 **Product** | 22 | [Browse →](./product/) |
| 🏷️ **Marketing** | 18 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [CorentinTh/it-tools](./frontend/corentinth-it-tools.md) | ⭐ 38.3k | Frontend |
| 2 | [wolfpld/tracy](./misc/wolfpld-tracy.md) | ⭐ 15.7k | Misc |
| 3 | [1Panel-dev/1Panel](./aiml/1panel-dev-1panel.md) | ⭐ 35.2k | AI/ML |
| 4 | [grafana/k6](./devtools/grafana-k6.md) | ⭐ 30.5k | DevTools |
| 5 | [openscad/openscad](./misc/openscad-openscad.md) | ⭐ 9.3k | Misc |
| 6 | [coollabsio/coolify](./backend/coollabsio-coolify.md) | ⭐ 54.3k | Backend |
| 7 | [roboflow/supervision](./misc/roboflow-supervision.md) | ⭐ 38.2k | Misc |
| 8 | [RIOT-OS/RIOT](./misc/riot-os-riot.md) | ⭐ 5.7k | Misc |
| 9 | [shadps4-emu/shadPS4](./frontend/shadps4-emu-shadps4.md) | ⭐ 30.9k | Frontend |
| 10 | [getsops/sops](./security/getsops-sops.md) | ⭐ 21.6k | Security |

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
