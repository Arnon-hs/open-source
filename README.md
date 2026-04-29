# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **11804** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 4505 | [Browse →](./aiml/) |
| 📦 **Misc** | 2272 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1160 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 931 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 722 | [Browse →](./backend/) |
| 🔧 **DevTools** | 702 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 423 | [Browse →](./crypto/) |
| 📊 **Data** | 254 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 251 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 142 | [Browse →](./mobile/) |
| 💳 **Payments** | 128 | [Browse →](./payments/) |
| 📈 **Trading** | 121 | [Browse →](./trading/) |
| 🔐 **Security** | 106 | [Browse →](./security/) |
| ✨ **Design** | 39 | [Browse →](./design/) |
| 🎯 **Product** | 26 | [Browse →](./product/) |
| 🏷️ **Marketing** | 22 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [OthmanAdi/planning-with-files](./orchestration/othmanadi-planning-with-files.md) | ⭐ 19.9k | Orchestration |
| 2 | [Automattic/wp-calypso](./frontend/automattic-wp-calypso.md) | ⭐ 12.6k | Frontend |
| 3 | [huggingface/peft](./aiml/huggingface-peft.md) | ⭐ 21k | AI/ML |
| 4 | [ipython/ipython](./aiml/ipython-ipython.md) | ⭐ 16.7k | AI/ML |
| 5 | [TykTechnologies/tyk](./backend/tyktechnologies-tyk.md) | ⭐ 10.7k | Backend |
| 6 | [NativeScript/NativeScript](./frontend/nativescript-nativescript.md) | ⭐ 25.5k | Frontend |
| 7 | [caddyserver/caddy](./backend/caddyserver-caddy.md) | ⭐ 71.9k | Backend |
| 8 | [WeblateOrg/weblate](./misc/weblateorg-weblate.md) | ⭐ 5.8k | Misc |
| 9 | [argoproj/argo-cd](./devopsinfra/argoproj-argo-cd.md) | ⭐ 22.8k | DevOps & Infra |
| 10 | [saltstack/salt](./devopsinfra/saltstack-salt.md) | ⭐ 15.4k | DevOps & Infra |

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
