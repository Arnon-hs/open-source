# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **2134** |
| 📁 **Categories** | **15** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 796 | [Browse →](./aiml/) |
| 📦 **Misc** | 358 | [Browse →](./misc/) |
| 🎨 **Frontend** | 240 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 190 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 134 | [Browse →](./backend/) |
| 🔧 **DevTools** | 107 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 87 | [Browse →](./crypto/) |
| 📊 **Data** | 64 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 47 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 32 | [Browse →](./mobile/) |
| 💳 **Payments** | 24 | [Browse →](./payments/) |
| 📈 **Trading** | 23 | [Browse →](./trading/) |
| 🔐 **Security** | 20 | [Browse →](./security/) |
| 🎯 **Product** | 8 | [Browse →](./product/) |
| ✨ **Design** | 4 | [Browse →](./design/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [spree/spree](./backend/spree-spree.md) | ⭐ 15.4k | Backend |
| 2 | [PrefectHQ/prefect](./orchestration/prefecthq-prefect.md) | ⭐ 22.2k | Orchestration |
| 3 | [giampaolo/psutil](./misc/giampaolo-psutil.md) | ⭐ 11.1k | Misc |
| 4 | [Aider-AI/aider](./aiml/aider-ai-aider.md) | ⭐ 43.8k | AI/ML |
| 5 | [yeasy/docker_practice](./aiml/yeasy-docker-practice.md) | ⭐ 26k | AI/ML |
| 6 | [DNSCrypt/dnscrypt-proxy](./misc/dnscrypt-dnscrypt-proxy.md) | ⭐ 13.2k | Misc |
| 7 | [gofiber/fiber](./backend/gofiber-fiber.md) | ⭐ 39.6k | Backend |
| 8 | [envoyproxy/envoy](./misc/envoyproxy-envoy.md) | ⭐ 27.9k | Misc |
| 9 | [ipython/ipython](./aiml/ipython-ipython.md) | ⭐ 16.7k | AI/ML |
| 10 | [shanraisshan/claude-code-best-practice](./orchestration/shanraisshan-claude-code-best-practice.md) | ⭐ 47.6k | Orchestration |

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
