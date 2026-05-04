# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **15747** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 5874 | [Browse →](./aiml/) |
| 📦 **Misc** | 3270 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1549 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1151 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 964 | [Browse →](./backend/) |
| 🔧 **DevTools** | 929 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 534 | [Browse →](./crypto/) |
| 📊 **Data** | 357 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 336 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 217 | [Browse →](./mobile/) |
| 💳 **Payments** | 164 | [Browse →](./payments/) |
| 📈 **Trading** | 161 | [Browse →](./trading/) |
| 🔐 **Security** | 128 | [Browse →](./security/) |
| ✨ **Design** | 52 | [Browse →](./design/) |
| 🏷️ **Marketing** | 31 | [Browse →](./marketing/) |
| 🎯 **Product** | 30 | [Browse →](./product/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [opendatalab/MinerU](./orchestration/opendatalab-mineru.md) | ⭐ 61.9k | Orchestration |
| 2 | [PatrickJS/awesome-angular](./aiml/patrickjs-awesome-angular.md) | ⭐ 10k | AI/ML |
| 3 | [JunkFood02/Seal](./mobile/junkfood02-seal.md) | ⭐ 26k | Mobile |
| 4 | [firecrawl/firecrawl](./aiml/firecrawl-firecrawl.md) | ⭐ 114.7k | AI/ML |
| 5 | [storybookjs/storybook](./aiml/storybookjs-storybook.md) | ⭐ 89.8k | AI/ML |
| 6 | [xtekky/gpt4free](./aiml/xtekky-gpt4free.md) | ⭐ 66.2k | AI/ML |
| 7 | [Leonxlnx/taste-skill](./aiml/leonxlnx-taste-skill.md) | ⭐ 14.9k | AI/ML |
| 8 | [zhkl0228/unidbg](./mobile/zhkl0228-unidbg.md) | ⭐ 4.9k | Mobile |
| 9 | [krzyzanowskim/CryptoSwift](./crypto/krzyzanowskim-cryptoswift.md) | ⭐ 10.5k | Crypto |
| 10 | [code-yeongyu/oh-my-openagent](./orchestration/code-yeongyu-oh-my-openagent.md) | ⭐ 55.6k | Orchestration |

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
