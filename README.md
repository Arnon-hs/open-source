# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **10202** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 3944 | [Browse →](./aiml/) |
| 📦 **Misc** | 1907 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1011 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 835 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 603 | [Browse →](./backend/) |
| 🔧 **DevTools** | 583 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 365 | [Browse →](./crypto/) |
| 📊 **Data** | 222 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 212 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 131 | [Browse →](./mobile/) |
| 💳 **Payments** | 120 | [Browse →](./payments/) |
| 📈 **Trading** | 100 | [Browse →](./trading/) |
| 🔐 **Security** | 92 | [Browse →](./security/) |
| ✨ **Design** | 35 | [Browse →](./design/) |
| 🎯 **Product** | 24 | [Browse →](./product/) |
| 🏷️ **Marketing** | 18 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [aimeos/aimeos-laravel](./aiml/aimeos-aimeos-laravel.md) | ⭐ 8.6k | AI/ML |
| 2 | [readest/readest](./aiml/readest-readest.md) | ⭐ 20k | AI/ML |
| 3 | [paperless-ngx/paperless-ngx](./misc/paperless-ngx-paperless-ngx.md) | ⭐ 40k | Misc |
| 4 | [fluent/fluent-bit](./data/fluent-fluent-bit.md) | ⭐ 7.8k | Data |
| 5 | [MonoGame/MonoGame](./misc/monogame-monogame.md) | ⭐ 13.8k | Misc |
| 6 | [DioxusLabs/dioxus](./aiml/dioxuslabs-dioxus.md) | ⭐ 35.9k | AI/ML |
| 7 | [openvinotoolkit/openvino](./aiml/openvinotoolkit-openvino.md) | ⭐ 10.1k | AI/ML |
| 8 | [containerd/containerd](./aiml/containerd-containerd.md) | ⭐ 20.6k | AI/ML |
| 9 | [nukeop/nuclear](./aiml/nukeop-nuclear.md) | ⭐ 17.4k | AI/ML |
| 10 | [spaceship-prompt/spaceship-prompt](./misc/spaceship-prompt-spaceship-prompt.md) | ⭐ 20.5k | Misc |

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
