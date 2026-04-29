# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **11608** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 4441 | [Browse →](./aiml/) |
| 📦 **Misc** | 2228 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1146 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 913 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 708 | [Browse →](./backend/) |
| 🔧 **DevTools** | 688 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 413 | [Browse →](./crypto/) |
| 📊 **Data** | 250 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 245 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 140 | [Browse →](./mobile/) |
| 💳 **Payments** | 127 | [Browse →](./payments/) |
| 📈 **Trading** | 117 | [Browse →](./trading/) |
| 🔐 **Security** | 105 | [Browse →](./security/) |
| ✨ **Design** | 39 | [Browse →](./design/) |
| 🎯 **Product** | 26 | [Browse →](./product/) |
| 🏷️ **Marketing** | 22 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [koreader/koreader](./mobile/koreader-koreader.md) | ⭐ 26.5k | Mobile |
| 2 | [samber/awesome-prometheus-alerts](./misc/samber-awesome-prometheus-alerts.md) | ⭐ 7.9k | Misc |
| 3 | [hwdsl2/docker-ipsec-vpn-server](./backend/hwdsl2-docker-ipsec-vpn-server.md) | ⭐ 7.1k | Backend |
| 4 | [elizaOS/eliza](./crypto/elizaos-eliza.md) | ⭐ 18.3k | Crypto |
| 5 | [logseq/logseq](./product/logseq-logseq.md) | ⭐ 42.5k | Product |
| 6 | [zhkl0228/unidbg](./mobile/zhkl0228-unidbg.md) | ⭐ 4.9k | Mobile |
| 7 | [huggingface/transformers](./crypto/huggingface-transformers.md) | ⭐ 160.1k | Crypto |
| 8 | [gruntwork-io/terratest](./devtools/gruntwork-io-terratest.md) | ⭐ 7.9k | DevTools |
| 9 | [MISP/MISP](./trading/misp-misp.md) | ⭐ 6.3k | Trading |
| 10 | [assistant-ui/assistant-ui](./aiml/assistant-ui-assistant-ui.md) | ⭐ 9.8k | AI/ML |

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
