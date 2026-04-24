# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **3301** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1257 | [Browse →](./aiml/) |
| 📦 **Misc** | 512 | [Browse →](./misc/) |
| 🎨 **Frontend** | 357 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 306 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 205 | [Browse →](./backend/) |
| 🔧 **DevTools** | 172 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 135 | [Browse →](./crypto/) |
| 📊 **Data** | 92 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 77 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 45 | [Browse →](./mobile/) |
| 💳 **Payments** | 45 | [Browse →](./payments/) |
| 📈 **Trading** | 35 | [Browse →](./trading/) |
| 🔐 **Security** | 35 | [Browse →](./security/) |
| ✨ **Design** | 12 | [Browse →](./design/) |
| 🎯 **Product** | 11 | [Browse →](./product/) |
| 🏷️ **Marketing** | 5 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [duplicati/duplicati](./aiml/duplicati-duplicati.md) | ⭐ 14.5k | AI/ML |
| 2 | [ZhuLinsen/daily_stock_analysis](./trading/zhulinsen-daily-stock-analysis.md) | ⭐ 31.2k | Trading |
| 3 | [hellodigua/ChatLab](./aiml/hellodigua-chatlab.md) | ⭐ 6.1k | AI/ML |
| 4 | [nhivp/Awesome-Embedded](./aiml/nhivp-awesome-embedded.md) | ⭐ 8.5k | AI/ML |
| 5 | [ruby/ruby](./misc/ruby-ruby.md) | ⭐ 23.5k | Misc |
| 6 | [rowboatlabs/rowboat](./orchestration/rowboatlabs-rowboat.md) | ⭐ 13.1k | Orchestration |
| 7 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 8 | [opendataloader-project/opendataloader-pdf](./aiml/opendataloader-project-opendataloader-pdf.md) | ⭐ 19.2k | AI/ML |
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
