# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **11489** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 4402 | [Browse →](./aiml/) |
| 📦 **Misc** | 2200 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1131 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 907 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 699 | [Browse →](./backend/) |
| 🔧 **DevTools** | 683 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 409 | [Browse →](./crypto/) |
| 📊 **Data** | 247 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 243 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 139 | [Browse →](./mobile/) |
| 💳 **Payments** | 126 | [Browse →](./payments/) |
| 📈 **Trading** | 117 | [Browse →](./trading/) |
| 🔐 **Security** | 103 | [Browse →](./security/) |
| ✨ **Design** | 37 | [Browse →](./design/) |
| 🎯 **Product** | 25 | [Browse →](./product/) |
| 🏷️ **Marketing** | 21 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [samber/awesome-prometheus-alerts](./misc/samber-awesome-prometheus-alerts.md) | ⭐ 7.9k | Misc |
| 2 | [ceph/ceph](./crypto/ceph-ceph.md) | ⭐ 16.5k | Crypto |
| 3 | [hwdsl2/docker-ipsec-vpn-server](./backend/hwdsl2-docker-ipsec-vpn-server.md) | ⭐ 7.1k | Backend |
| 4 | [zitadel/zitadel](./aiml/zitadel-zitadel.md) | ⭐ 13.7k | AI/ML |
| 5 | [mudler/LocalAI](./aiml/mudler-localai.md) | ⭐ 45.9k | AI/ML |
| 6 | [jackocnr/intl-tel-input](./aiml/jackocnr-intl-tel-input.md) | ⭐ 8.2k | AI/ML |
| 7 | [activepieces/activepieces](./aiml/activepieces-activepieces.md) | ⭐ 22k | AI/ML |
| 8 | [emqx/emqx](./aiml/emqx-emqx.md) | ⭐ 16.2k | AI/ML |
| 9 | [keybase/client](./frontend/keybase-client.md) | ⭐ 9.2k | Frontend |
| 10 | [volcengine/OpenViking](./aiml/volcengine-openviking.md) | ⭐ 23.2k | AI/ML |

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
