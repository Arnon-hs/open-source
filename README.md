# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **7165** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2750 | [Browse →](./aiml/) |
| 📦 **Misc** | 1293 | [Browse →](./misc/) |
| 🎨 **Frontend** | 715 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 633 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 412 | [Browse →](./backend/) |
| 🔧 **DevTools** | 404 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 249 | [Browse →](./crypto/) |
| 📊 **Data** | 162 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 142 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 106 | [Browse →](./mobile/) |
| 💳 **Payments** | 99 | [Browse →](./payments/) |
| 📈 **Trading** | 74 | [Browse →](./trading/) |
| 🔐 **Security** | 70 | [Browse →](./security/) |
| ✨ **Design** | 26 | [Browse →](./design/) |
| 🎯 **Product** | 20 | [Browse →](./product/) |
| 🏷️ **Marketing** | 10 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [code-yeongyu/oh-my-openagent](./orchestration/code-yeongyu-oh-my-openagent.md) | ⭐ 54.2k | Orchestration |
| 2 | [Tyrrrz/YoutubeDownloader](./marketing/tyrrrz-youtubedownloader.md) | ⭐ 14.8k | Marketing |
| 3 | [wailsapp/wails](./aiml/wailsapp-wails.md) | ⭐ 33.9k | AI/ML |
| 4 | [Gallopsled/pwntools](./misc/gallopsled-pwntools.md) | ⭐ 13.4k | Misc |
| 5 | [netbox-community/netbox](./devopsinfra/netbox-community-netbox.md) | ⭐ 20.3k | DevOps & Infra |
| 6 | [wkentaro/labelme](./aiml/wkentaro-labelme.md) | ⭐ 15.8k | AI/ML |
| 7 | [containerd/containerd](./aiml/containerd-containerd.md) | ⭐ 20.6k | AI/ML |
| 8 | [dagster-io/dagster](./orchestration/dagster-io-dagster.md) | ⭐ 15.4k | Orchestration |
| 9 | [google/adk-python](./orchestration/google-adk-python.md) | ⭐ 19.3k | Orchestration |
| 10 | [invoiceninja/invoiceninja](./payments/invoiceninja-invoiceninja.md) | ⭐ 9.7k | Payments |

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
