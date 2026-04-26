# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **7256** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2789 | [Browse →](./aiml/) |
| 📦 **Misc** | 1313 | [Browse →](./misc/) |
| 🎨 **Frontend** | 725 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 639 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 415 | [Browse →](./backend/) |
| 🔧 **DevTools** | 411 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 250 | [Browse →](./crypto/) |
| 📊 **Data** | 162 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 142 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 107 | [Browse →](./mobile/) |
| 💳 **Payments** | 101 | [Browse →](./payments/) |
| 📈 **Trading** | 75 | [Browse →](./trading/) |
| 🔐 **Security** | 71 | [Browse →](./security/) |
| ✨ **Design** | 26 | [Browse →](./design/) |
| 🎯 **Product** | 20 | [Browse →](./product/) |
| 🏷️ **Marketing** | 10 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [code-yeongyu/oh-my-openagent](./orchestration/code-yeongyu-oh-my-openagent.md) | ⭐ 54.2k | Orchestration |
| 2 | [Tyrrrz/YoutubeDownloader](./marketing/tyrrrz-youtubedownloader.md) | ⭐ 14.8k | Marketing |
| 3 | [wailsapp/wails](./aiml/wailsapp-wails.md) | ⭐ 33.9k | AI/ML |
| 4 | [lionsoul2014/ip2region](./devtools/lionsoul2014-ip2region.md) | ⭐ 19k | DevTools |
| 5 | [jeessy2/ddns-go](./aiml/jeessy2-ddns-go.md) | ⭐ 16.7k | AI/ML |
| 6 | [lutzroeder/netron](./aiml/lutzroeder-netron.md) | ⭐ 32.8k | AI/ML |
| 7 | [netbox-community/netbox](./devopsinfra/netbox-community-netbox.md) | ⭐ 20.3k | DevOps & Infra |
| 8 | [wkentaro/labelme](./aiml/wkentaro-labelme.md) | ⭐ 15.8k | AI/ML |
| 9 | [zulip/zulip](./frontend/zulip-zulip.md) | ⭐ 25.1k | Frontend |
| 10 | [containerd/containerd](./aiml/containerd-containerd.md) | ⭐ 20.6k | AI/ML |

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
