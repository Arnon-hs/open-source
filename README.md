# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **17128** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 6363 | [Browse →](./aiml/) |
| 📦 **Misc** | 3596 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1692 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 1226 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 1055 | [Browse →](./backend/) |
| 🔧 **DevTools** | 1002 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 575 | [Browse →](./crypto/) |
| 📊 **Data** | 395 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 371 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 240 | [Browse →](./mobile/) |
| 💳 **Payments** | 172 | [Browse →](./payments/) |
| 📈 **Trading** | 171 | [Browse →](./trading/) |
| 🔐 **Security** | 145 | [Browse →](./security/) |
| ✨ **Design** | 57 | [Browse →](./design/) |
| 🎯 **Product** | 36 | [Browse →](./product/) |
| 🏷️ **Marketing** | 32 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [invertase/react-native-firebase](./aiml/invertase-react-native-firebase.md) | ⭐ 12.3k | AI/ML |
| 2 | [cython/cython](./data/cython-cython.md) | ⭐ 10.7k | Data |
| 3 | [awsdocs/aws-doc-sdk-examples](./aiml/awsdocs-aws-doc-sdk-examples.md) | ⭐ 10.4k | AI/ML |
| 4 | [WinMerge/winmerge](./misc/winmerge-winmerge.md) | ⭐ 8.8k | Misc |
| 5 | [HKUDS/nanobot](./aiml/hkuds-nanobot.md) | ⭐ 41.7k | AI/ML |
| 6 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 7 | [ludwig-ai/ludwig](./aiml/ludwig-ai-ludwig.md) | ⭐ 11.7k | AI/ML |
| 8 | [rclone/rclone](./aiml/rclone-rclone.md) | ⭐ 57k | AI/ML |
| 9 | [avajs/ava](./devtools/avajs-ava.md) | ⭐ 20.8k | DevTools |
| 10 | [Project-OSRM/osrm-backend](./backend/project-osrm-osrm-backend.md) | ⭐ 7.7k | Backend |

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
