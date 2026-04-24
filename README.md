# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **3249** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1236 | [Browse →](./aiml/) |
| 📦 **Misc** | 501 | [Browse →](./misc/) |
| 🎨 **Frontend** | 352 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 302 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 202 | [Browse →](./backend/) |
| 🔧 **DevTools** | 168 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 133 | [Browse →](./crypto/) |
| 📊 **Data** | 92 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 77 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 45 | [Browse →](./payments/) |
| 📱 **Mobile** | 44 | [Browse →](./mobile/) |
| 🔐 **Security** | 35 | [Browse →](./security/) |
| 📈 **Trading** | 34 | [Browse →](./trading/) |
| ✨ **Design** | 12 | [Browse →](./design/) |
| 🎯 **Product** | 11 | [Browse →](./product/) |
| 🏷️ **Marketing** | 5 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [duplicati/duplicati](./aiml/duplicati-duplicati.md) | ⭐ 14.5k | AI/ML |
| 2 | [rowboatlabs/rowboat](./orchestration/rowboatlabs-rowboat.md) | ⭐ 13.1k | Orchestration |
| 3 | [mdn/content](./aiml/mdn-content.md) | ⭐ 10.7k | AI/ML |
| 4 | [x64dbg/x64dbg](./security/x64dbg-x64dbg.md) | ⭐ 48.2k | Security |
| 5 | [Wei-Shaw/claude-relay-service](./aiml/wei-shaw-claude-relay-service.md) | ⭐ 11.3k | AI/ML |
| 6 | [apache/tvm](./misc/apache-tvm.md) | ⭐ 13.3k | Misc |
| 7 | [Anuken/Mindustry](./mobile/anuken-mindustry.md) | ⭐ 27.4k | Mobile |
| 8 | [hiyouga/LlamaFactory](./trading/hiyouga-llamafactory.md) | ⭐ 70.6k | Trading |
| 9 | [opf/openproject](./product/opf-openproject.md) | ⭐ 14.9k | Product |
| 10 | [bpftrace/bpftrace](./misc/bpftrace-bpftrace.md) | ⭐ 10.1k | Misc |

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
