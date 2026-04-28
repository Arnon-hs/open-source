# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **9429** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 3631 | [Browse →](./aiml/) |
| 📦 **Misc** | 1756 | [Browse →](./misc/) |
| 🎨 **Frontend** | 949 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 784 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 552 | [Browse →](./backend/) |
| 🔧 **DevTools** | 537 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 337 | [Browse →](./crypto/) |
| 📊 **Data** | 202 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 188 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 124 | [Browse →](./mobile/) |
| 💳 **Payments** | 115 | [Browse →](./payments/) |
| 📈 **Trading** | 95 | [Browse →](./trading/) |
| 🔐 **Security** | 87 | [Browse →](./security/) |
| ✨ **Design** | 32 | [Browse →](./design/) |
| 🎯 **Product** | 22 | [Browse →](./product/) |
| 🏷️ **Marketing** | 18 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [temporalio/temporal](./orchestration/temporalio-temporal.md) | ⭐ 19.9k | Orchestration |
| 2 | [grpc/grpc-go](./backend/grpc-grpc-go.md) | ⭐ 22.9k | Backend |
| 3 | [Stirling-Tools/Stirling-PDF](./devopsinfra/stirling-tools-stirling-pdf.md) | ⭐ 77.9k | DevOps & Infra |
| 4 | [sonic-pi-net/sonic-pi](./misc/sonic-pi-net-sonic-pi.md) | ⭐ 11.8k | Misc |
| 5 | [wkentaro/labelme](./aiml/wkentaro-labelme.md) | ⭐ 15.8k | AI/ML |
| 6 | [huggingface/peft](./aiml/huggingface-peft.md) | ⭐ 21k | AI/ML |
| 7 | [ipython/ipython](./aiml/ipython-ipython.md) | ⭐ 16.7k | AI/ML |
| 8 | [is-a-dev/register](./aiml/is-a-dev-register.md) | ⭐ 10.2k | AI/ML |
| 9 | [Donchitos/Claude-Code-Game-Studios](./aiml/donchitos-claude-code-game-studios.md) | ⭐ 16.4k | AI/ML |
| 10 | [TykTechnologies/tyk](./backend/tyktechnologies-tyk.md) | ⭐ 10.7k | Backend |

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
