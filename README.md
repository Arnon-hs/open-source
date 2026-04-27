# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **8447** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 3256 | [Browse →](./aiml/) |
| 📦 **Misc** | 1550 | [Browse →](./misc/) |
| 🎨 **Frontend** | 861 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 712 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 490 | [Browse →](./backend/) |
| 🔧 **DevTools** | 482 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 290 | [Browse →](./crypto/) |
| 📊 **Data** | 183 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 166 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 118 | [Browse →](./mobile/) |
| 💳 **Payments** | 111 | [Browse →](./payments/) |
| 📈 **Trading** | 86 | [Browse →](./trading/) |
| 🔐 **Security** | 77 | [Browse →](./security/) |
| ✨ **Design** | 28 | [Browse →](./design/) |
| 🎯 **Product** | 22 | [Browse →](./product/) |
| 🏷️ **Marketing** | 15 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [AdguardTeam/AdGuardHome](./frontend/adguardteam-adguardhome.md) | ⭐ 33.7k | Frontend |
| 2 | [shadcn-ui/ui](./aiml/shadcn-ui-ui.md) | ⭐ 113.1k | AI/ML |
| 3 | [OpenAPITools/openapi-generator](./backend/openapitools-openapi-generator.md) | ⭐ 26.2k | Backend |
| 4 | [vxcontrol/pentagi](./orchestration/vxcontrol-pentagi.md) | ⭐ 15.9k | Orchestration |
| 5 | [leon-ai/leon](./aiml/leon-ai-leon.md) | ⭐ 17.2k | AI/ML |
| 6 | [cri-o/cri-o](./aiml/cri-o-cri-o.md) | ⭐ 5.6k | AI/ML |
| 7 | [k2-fsa/sherpa-onnx](./backend/k2-fsa-sherpa-onnx.md) | ⭐ 11.9k | Backend |
| 8 | [gogs/gogs](./aiml/gogs-gogs.md) | ⭐ 47.5k | AI/ML |
| 9 | [microsoft/terminal](./misc/microsoft-terminal.md) | ⭐ 102.9k | Misc |
| 10 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |

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
