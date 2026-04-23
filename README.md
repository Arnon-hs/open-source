# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **1278** |
| 📁 **Categories** | **15** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 493 | [Browse →](./aiml/) |
| 📦 **Misc** | 223 | [Browse →](./misc/) |
| 🎨 **Frontend** | 132 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 114 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 71 | [Browse →](./backend/) |
| 🔧 **DevTools** | 56 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 47 | [Browse →](./crypto/) |
| 📊 **Data** | 35 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 31 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 26 | [Browse →](./mobile/) |
| 💳 **Payments** | 16 | [Browse →](./payments/) |
| 📈 **Trading** | 16 | [Browse →](./trading/) |
| 🔐 **Security** | 12 | [Browse →](./security/) |
| 🎯 **Product** | 5 | [Browse →](./product/) |
| ✨ **Design** | 1 | [Browse →](./design/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [mermaid-js/mermaid](./aiml/mermaid-js-mermaid.md) | ⭐ 87.6k | AI/ML |
| 2 | [sickn33/antigravity-awesome-skills](./orchestration/sickn33-antigravity-awesome-skills.md) | ⭐ 34.7k | Orchestration |
| 3 | [sharkdp/fd](./devtools/sharkdp-fd.md) | ⭐ 42.7k | DevTools |
| 4 | [soxoj/maigret](./aiml/soxoj-maigret.md) | ⭐ 19.6k | AI/ML |
| 5 | [openshift/origin](./aiml/openshift-origin.md) | ⭐ 8.6k | AI/ML |
| 6 | [sherlock-project/sherlock](./aiml/sherlock-project-sherlock.md) | ⭐ 81.8k | AI/ML |
| 7 | [RustPython/RustPython](./misc/rustpython-rustpython.md) | ⭐ 22k | Misc |
| 8 | [authelia/authelia](./devopsinfra/authelia-authelia.md) | ⭐ 27.6k | DevOps & Infra |
| 9 | [nicolargo/glances](./backend/nicolargo-glances.md) | ⭐ 32.3k | Backend |
| 10 | [ValueCell-ai/ClawX](./orchestration/valuecell-ai-clawx.md) | ⭐ 6.7k | Orchestration |

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
