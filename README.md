# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **2906** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 1094 | [Browse →](./aiml/) |
| 📦 **Misc** | 464 | [Browse →](./misc/) |
| 🎨 **Frontend** | 316 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 266 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 182 | [Browse →](./backend/) |
| 🔧 **DevTools** | 150 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 115 | [Browse →](./crypto/) |
| 📊 **Data** | 80 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 68 | [Browse →](./devopsinfra/) |
| 💳 **Payments** | 42 | [Browse →](./payments/) |
| 📱 **Mobile** | 38 | [Browse →](./mobile/) |
| 📈 **Trading** | 33 | [Browse →](./trading/) |
| 🔐 **Security** | 33 | [Browse →](./security/) |
| 🎯 **Product** | 11 | [Browse →](./product/) |
| ✨ **Design** | 11 | [Browse →](./design/) |
| 🏷️ **Marketing** | 3 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [supabase/supabase](./aiml/supabase-supabase.md) | ⭐ 101.3k | AI/ML |
| 2 | [musescore/MuseScore](./aiml/musescore-musescore.md) | ⭐ 14.5k | AI/ML |
| 3 | [Kong/insomnia](./aiml/kong-insomnia.md) | ⭐ 38.3k | AI/ML |
| 4 | [future-architect/vuls](./aiml/future-architect-vuls.md) | ⭐ 12.1k | AI/ML |
| 5 | [fmtlib/fmt](./misc/fmtlib-fmt.md) | ⭐ 23.4k | Misc |
| 6 | [mrousavy/react-native-vision-camera](./aiml/mrousavy-react-native-vision-camera.md) | ⭐ 9.3k | AI/ML |
| 7 | [frappe/erpnext](./aiml/frappe-erpnext.md) | ⭐ 33.2k | AI/ML |
| 8 | [better-auth/better-auth](./payments/better-auth-better-auth.md) | ⭐ 28k | Payments |
| 9 | [kubernetes-sigs/external-dns](./backend/kubernetes-sigs-external-dns.md) | ⭐ 8.9k | Backend |
| 10 | [PaddlePaddle/Paddle](./aiml/paddlepaddle-paddle.md) | ⭐ 23.9k | AI/ML |

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
