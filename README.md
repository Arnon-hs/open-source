# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **7431** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2852 | [Browse →](./aiml/) |
| 📦 **Misc** | 1364 | [Browse →](./misc/) |
| 🎨 **Frontend** | 747 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 648 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 422 | [Browse →](./backend/) |
| 🔧 **DevTools** | 419 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 253 | [Browse →](./crypto/) |
| 📊 **Data** | 166 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 142 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 112 | [Browse →](./mobile/) |
| 💳 **Payments** | 103 | [Browse →](./payments/) |
| 📈 **Trading** | 75 | [Browse →](./trading/) |
| 🔐 **Security** | 72 | [Browse →](./security/) |
| ✨ **Design** | 26 | [Browse →](./design/) |
| 🎯 **Product** | 20 | [Browse →](./product/) |
| 🏷️ **Marketing** | 10 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [openscad/openscad](./misc/openscad-openscad.md) | ⭐ 9.3k | Misc |
| 2 | [fatedier/frp](./backend/fatedier-frp.md) | ⭐ 106.1k | Backend |
| 3 | [hibernate/hibernate-orm](./data/hibernate-hibernate-orm.md) | ⭐ 6.4k | Data |
| 4 | [jeessy2/ddns-go](./aiml/jeessy2-ddns-go.md) | ⭐ 16.7k | AI/ML |
| 5 | [iii-hq/iii](./aiml/iii-hq-iii.md) | ⭐ 15.3k | AI/ML |
| 6 | [containerd/containerd](./aiml/containerd-containerd.md) | ⭐ 20.6k | AI/ML |
| 7 | [PaddlePaddle/PaddleOCR](./aiml/paddlepaddle-paddleocr.md) | ⭐ 76.6k | AI/ML |
| 8 | [microsoft/agent-framework](./orchestration/microsoft-agent-framework.md) | ⭐ 9.8k | Orchestration |
| 9 | [huggingface/pytorch-image-models](./aiml/huggingface-pytorch-image-models.md) | ⭐ 36.7k | AI/ML |
| 10 | [gruntwork-io/terratest](./devtools/gruntwork-io-terratest.md) | ⭐ 7.9k | DevTools |

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
