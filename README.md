# 🌟 Open Scout Catalog

> Auto-curated catalog of promising open-source projects.
> Scouted from GitHub · HackerNews · Reddit · ProductHunt. Updated every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

---

## 📊 At a glance

| | |
|---|---|
| 🗂️ **Total projects** | **12572** |
| 📁 **Categories** | **16** |
| 🔄 **Auto-sync** | every 30 min via GitHub Actions |
| 🧠 **Summaries** | LLM-generated (OpenRouter · Ollama · Claude · OpenAI) |

## 🗂️ Categories

| Category | Projects | |
|---|---|---|
| 🤖 **AI/ML** | 4800 | [Browse →](./aiml/) |
| 📦 **Misc** | 2447 | [Browse →](./misc/) |
| 🎨 **Frontend** | 1224 | [Browse →](./frontend/) |
| 🧩 **Orchestration** | 971 | [Browse →](./orchestration/) |
| ⚙️ **Backend** | 765 | [Browse →](./backend/) |
| 🔧 **DevTools** | 746 | [Browse →](./devtools/) |
| ⛓️ **Crypto** | 451 | [Browse →](./crypto/) |
| 📊 **Data** | 282 | [Browse →](./data/) |
| 🚀 **DevOps & Infra** | 276 | [Browse →](./devopsinfra/) |
| 📱 **Mobile** | 155 | [Browse →](./mobile/) |
| 💳 **Payments** | 133 | [Browse →](./payments/) |
| 📈 **Trading** | 129 | [Browse →](./trading/) |
| 🔐 **Security** | 109 | [Browse →](./security/) |
| ✨ **Design** | 37 | [Browse →](./design/) |
| 🎯 **Product** | 25 | [Browse →](./product/) |
| 🏷️ **Marketing** | 22 | [Browse →](./marketing/) |

## 🔥 Top 10 by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [dotansimha/graphql-code-generator](./payments/dotansimha-graphql-code-generator.md) | ⭐ 11.2k | Payments |
| 2 | [project-chip/connectedhomeip](./frontend/project-chip-connectedhomeip.md) | ⭐ 8.7k | Frontend |
| 3 | [serverless/serverless](./aiml/serverless-serverless.md) | ⭐ 46.9k | AI/ML |
| 4 | [appium/appium](./frontend/appium-appium.md) | ⭐ 21.5k | Frontend |
| 5 | [jnMetaCode/agency-agents-zh](./crypto/jnmetacode-agency-agents-zh.md) | ⭐ 9.2k | Crypto |
| 6 | [openshift/origin](./aiml/openshift-origin.md) | ⭐ 8.6k | AI/ML |
| 7 | [yeasy/docker_practice](./aiml/yeasy-docker-practice.md) | ⭐ 26k | AI/ML |
| 8 | [Gallopsled/pwntools](./misc/gallopsled-pwntools.md) | ⭐ 13.4k | Misc |
| 9 | [firecracker-microvm/firecracker](./payments/firecracker-microvm-firecracker.md) | ⭐ 33.9k | Payments |
| 10 | [frappe/frappe](./aiml/frappe-frappe.md) | ⭐ 10k | AI/ML |

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
