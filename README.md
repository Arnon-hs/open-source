# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **7033** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 2691 | [Browse →](./aiml/) |
| 📦 **Misc** | 1274 | [Browse →](./misc/) |
| 🎨 **Frontend** | 699 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 618 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 404 | [Browse →](./backend/) |
| 🔧 **DevTools** | 399 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 244 | [Browse →](./crypto/) |
| 📊 **Data** | 161 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 141 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 106 | [Browse →](./mobile/) |
| 💳 **Payments** | 98 | [Browse →](./payments/) |
| 📈 **Trading** | 73 | [Browse →](./trading/) |
| 🔐 **Security** | 70 | [Browse →](./security/) |
| ✨ **Design** | 26 | [Browse →](./design/) |
| 🎯 **Product** | 20 | [Browse →](./product/) |
| 🏷️ **Marketing** | 9 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [Gallopsled/pwntools](./misc/gallopsled-pwntools.md) | ⭐ 13.4k | Misc |
| 2 | [containerd/containerd](./aiml/containerd-containerd.md) | ⭐ 20.6k | AI/ML |
| 3 | [invoiceninja/invoiceninja](./payments/invoiceninja-invoiceninja.md) | ⭐ 9.7k | Payments |
| 4 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 5 | [azerothcore/azerothcore-wotlk](./backend/azerothcore-azerothcore-wotlk.md) | ⭐ 8.2k | Backend |
| 6 | [XTLS/Xray-core](./misc/xtls-xray-core.md) | ⭐ 37.9k | Misc |
| 7 | [google/syzkaller](./aiml/google-syzkaller.md) | ⭐ 6.1k | AI/ML |
| 8 | [ipython/ipython](./aiml/ipython-ipython.md) | ⭐ 16.7k | AI/ML |
| 9 | [ory/kratos](./aiml/ory-kratos.md) | ⭐ 13.6k | AI/ML |
| 10 | [BerriAI/litellm](./orchestration/berriai-litellm.md) | ⭐ 44.7k | Orchestration |

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
