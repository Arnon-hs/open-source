# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **5752** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2216 | [Browse →](./aiml/) |
| 📦 **Misc** | 959 | [Browse →](./misc/) |
| 🎨 **Frontend** | 571 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 530 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 342 | [Browse →](./backend/) |
| 🔧 **DevTools** | 326 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 204 | [Browse →](./crypto/) |
| 📊 **Data** | 138 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 127 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 84 | [Browse →](./mobile/) |
| 💳 **Payments** | 82 | [Browse →](./payments/) |
| 🔐 **Security** | 62 | [Browse →](./security/) |
| 📈 **Trading** | 62 | [Browse →](./trading/) |
| ✨ **Design** | 23 | [Browse →](./design/) |
| 🎯 **Product** | 18 | [Browse →](./product/) |
| 🏷️ **Marketing** | 8 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [kavishdevar/librepods](./aiml/kavishdevar-librepods.md) | ⭐ 26.7k | AI/ML |
| 2 | [spantaleev/matrix-docker-ansible-deploy](./backend/spantaleev-matrix-docker-ansible-deploy.md) | ⭐ 6.3k | Backend |
| 3 | [hwdsl2/setup-ipsec-vpn](./backend/hwdsl2-setup-ipsec-vpn.md) | ⭐ 27.7k | Backend |
| 4 | [azerothcore/azerothcore-wotlk](./backend/azerothcore-azerothcore-wotlk.md) | ⭐ 8.2k | Backend |
| 5 | [huggingface/datasets](./aiml/huggingface-datasets.md) | ⭐ 21.5k | AI/ML |
| 6 | [firebase/firebase-ios-sdk](./aiml/firebase-firebase-ios-sdk.md) | ⭐ 6.6k | AI/ML |
| 7 | [siteboon/claudecodeui](./aiml/siteboon-claudecodeui.md) | ⭐ 10.2k | AI/ML |
| 8 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 9 | [navidrome/navidrome](./aiml/navidrome-navidrome.md) | ⭐ 20.7k | AI/ML |
| 10 | [microsoft/Web-Dev-For-Beginners](./aiml/microsoft-web-dev-for-beginners.md) | ⭐ 95.7k | AI/ML |

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
