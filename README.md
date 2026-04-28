# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **10018** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 3861 | [Browse →](./aiml/) |
| 📦 **Misc** | 1874 | [Browse →](./misc/) |
| 🎨 **Frontend** | 996 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 825 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 593 | [Browse →](./backend/) |
| 🔧 **DevTools** | 572 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 357 | [Browse →](./crypto/) |
| 📊 **Data** | 218 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 205 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 130 | [Browse →](./mobile/) |
| 💳 **Payments** | 119 | [Browse →](./payments/) |
| 📈 **Trading** | 99 | [Browse →](./trading/) |
| 🔐 **Security** | 93 | [Browse →](./security/) |
| ✨ **Design** | 34 | [Browse →](./design/) |
| 🎯 **Product** | 24 | [Browse →](./product/) |
| 🏷️ **Marketing** | 18 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [ramitsurana/awesome-kubernetes](./devopsinfra/ramitsurana-awesome-kubernetes.md) | ⭐ 15.9k | DevOps & Infra |
| 2 | [snowplow/snowplow](./data/snowplow-snowplow.md) | ⭐ 7k | Data |
| 3 | [lightningnetwork/lnd](./crypto/lightningnetwork-lnd.md) | ⭐ 8.1k | Crypto |
| 4 | [juicedata/juicefs](./aiml/juicedata-juicefs.md) | ⭐ 13.5k | AI/ML |
| 5 | [future-architect/vuls](./aiml/future-architect-vuls.md) | ⭐ 12.1k | AI/ML |
| 6 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 7 | [grafana/k6](./devtools/grafana-k6.md) | ⭐ 30.5k | DevTools |
| 8 | [Skyvern-AI/skyvern](./aiml/skyvern-ai-skyvern.md) | ⭐ 21.4k | AI/ML |
| 9 | [ossrs/srs](./backend/ossrs-srs.md) | ⭐ 28.8k | Backend |
| 10 | [flannel-io/flannel](./aiml/flannel-io-flannel.md) | ⭐ 9.4k | AI/ML |

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
