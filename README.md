# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **16568** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 6158 | [Browse →](./aiml/) |
| 📦 **Misc** | 3474 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1633 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1197 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 1018 | [Browse →](./backend/) |
| 🔧 **DevTools** | 966 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 556 | [Browse →](./crypto/) |
| 📊 **Data** | 379 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 361 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 227 | [Browse →](./mobile/) |
| 📈 **Trading** | 170 | [Browse →](./trading/) |
| 💳 **Payments** | 169 | [Browse →](./payments/) |
| 🔐 **Security** | 139 | [Browse →](./security/) |
| ✨ **Design** | 57 | [Browse →](./design/) |
| 🎯 **Product** | 33 | [Browse →](./product/) |
| 🏷️ **Marketing** | 31 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [browserless/browserless](./devopsinfra/browserless-browserless.md) | ⭐ 13.1k | DevOps & Infra |
| 2 | [Wox-launcher/Wox](./misc/wox-launcher-wox.md) | ⭐ 26.8k | Misc |
| 3 | [Sjj1024/PakePlus](./aiml/sjj1024-pakeplus.md) | ⭐ 11.9k | AI/ML |
| 4 | [apache/casbin](./aiml/apache-casbin.md) | ⭐ 20.1k | AI/ML |
| 5 | [OthmanAdi/planning-with-files](./orchestration/othmanadi-planning-with-files.md) | ⭐ 20.4k | Orchestration |
| 6 | [cython/cython](./data/cython-cython.md) | ⭐ 10.7k | Data |
| 7 | [hoppscotch/hoppscotch](./frontend/hoppscotch-hoppscotch.md) | ⭐ 79.1k | Frontend |
| 8 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 9 | [sorin-ionescu/prezto](./devtools/sorin-ionescu-prezto.md) | ⭐ 14.5k | DevTools |
| 10 | [flame-engine/flame](./mobile/flame-engine-flame.md) | ⭐ 10.6k | Mobile |

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
