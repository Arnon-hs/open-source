# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **6681** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2563 | [Browse →](./aiml/) |
| 📦 **Misc** | 1183 | [Browse →](./misc/) |
| 🎨 **Frontend** | 660 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 596 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 383 | [Browse →](./backend/) |
| 🔧 **DevTools** | 380 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 233 | [Browse →](./crypto/) |
| 📊 **Data** | 155 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 138 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 102 | [Browse →](./mobile/) |
| 💳 **Payments** | 94 | [Browse →](./payments/) |
| 📈 **Trading** | 70 | [Browse →](./trading/) |
| 🔐 **Security** | 69 | [Browse →](./security/) |
| ✨ **Design** | 26 | [Browse →](./design/) |
| 🎯 **Product** | 20 | [Browse →](./product/) |
| 🏷️ **Marketing** | 9 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [vbenjs/vue-vben-admin](./aiml/vbenjs-vue-vben-admin.md) | ⭐ 32.2k | AI/ML |
| 2 | [zhkl0228/unidbg](./mobile/zhkl0228-unidbg.md) | ⭐ 4.9k | Mobile |
| 3 | [esphome/esphome](./aiml/esphome-esphome.md) | ⭐ 11k | AI/ML |
| 4 | [ether/etherpad](./misc/ether-etherpad.md) | ⭐ 18.3k | Misc |
| 5 | [AccumulateMore/CV](./aiml/accumulatemore-cv.md) | ⭐ 20.3k | AI/ML |
| 6 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 7 | [logseq/logseq](./product/logseq-logseq.md) | ⭐ 42.4k | Product |
| 8 | [endless-sky/endless-sky](./trading/endless-sky-endless-sky.md) | ⭐ 7.3k | Trading |
| 9 | [icsharpcode/ILSpy](./data/icsharpcode-ilspy.md) | ⭐ 25k | Data |
| 10 | [ohmyzsh/ohmyzsh](./aiml/ohmyzsh-ohmyzsh.md) | ⭐ 186.5k | AI/ML |

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
