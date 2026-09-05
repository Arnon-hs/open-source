# AtlasRepo Open Source Catalog

**Evidence-backed open-source search for coding agents.**

[Documentation](https://atlasrepo.com/docs) · [Hosted MCP](https://mcp.atlasrepo.com/mcp) · [npm](https://www.npmjs.com/package/atlasrepo-mcp) · [Skills](https://github.com/Arnon-hs/atlasrepo-skills)

> A living, auto-curated catalog of open-source projects, enriched with practical summaries, categories, quality signals and transparent scoring.

## Purpose

This repository turns a fast-moving open-source ecosystem into a browsable and machine-readable decision layer. Use it to discover candidates, compare practical fit and give coding agents grounded starting points before deeper technical, security and license review.

## At a glance

| | |
|---|---|
| **Projects** | **34554** |
| **Categories** | **28** |
| **Refresh** | Continuously maintained by AtlasRepo Scout |
| **Metadata** | Repository signals, multilingual summaries and practical evaluations |

## Browse the catalog

| Category | Projects | |
|---|---|---|
| 📦 **Misc** | 15872 | [Browse →](./misc/) |
| 🤖 **AI/ML** | 3321 | [Browse →](./aiml/) |
| 🏷️ **Mcp** | 2566 | [Browse →](./mcp/) |
| 🧩 **Orchestration** | 2205 | [Browse →](./orchestration/) |
| 🔧 **DevTools** | 1352 | [Browse →](./devtools/) |
| 🏷️ **Automation** | 1261 | [Browse →](./automation/) |
| 🎨 **Frontend** | 973 | [Browse →](./frontend/) |
| ⚙️ **Backend** | 902 | [Browse →](./backend/) |
| ⛓️ **Crypto** | 758 | [Browse →](./crypto/) |
| 📱 **Mobile** | 723 | [Browse →](./mobile/) |
| 🚀 **DevOps & Infra** | 616 | [Browse →](./devopsinfra/) |
| 🏷️ **Database** | 588 | [Browse →](./database/) |
| 🏷️ **Knowledgerag** | 564 | [Browse →](./knowledgerag/) |
| 🏷️ **Templates** | 421 | [Browse →](./templates/) |
| 🔐 **Security** | 396 | [Browse →](./security/) |
| 📊 **Data** | 393 | [Browse →](./data/) |
| 🏷️ **Observability** | 345 | [Browse →](./observability/) |
| 🏷️ **Video-editing** | 328 | [Browse →](./video-editing/) |
| 💳 **Payments** | 310 | [Browse →](./payments/) |
| 📈 **Trading** | 187 | [Browse →](./trading/) |
| ✨ **Design** | 170 | [Browse →](./design/) |
| 🏷️ **Content-creation** | 126 | [Browse →](./content-creation/) |
| 🏷️ **Vertical-video** | 77 | [Browse →](./vertical-video/) |
| 🏷️ **Education** | 45 | [Browse →](./education/) |
| 🏷️ **Marketing** | 44 | [Browse →](./marketing/) |
| 🎯 **Product** | 9 | [Browse →](./product/) |
| 🏷️ **Ai** | 1 | [Browse →](./ai/) |
| 🏷️ **Networking** | 1 | [Browse →](./networking/) |

## Top projects by score

| # | Project | Stars | Category |
|---|---|---|---|
| 1 | [jipraks/yt-short-clipper](./vertical-video/jipraks-yt-short-clipper.md) | ⭐ 964 | Vertical-video |
| 2 | [IgorShadurin/app.yumcut.com](./vertical-video/igorshadurin-app.yumcut.com.md) | ⭐ 855 | Vertical-video |
| 3 | [chengzuopeng/stock-sdk](./trading/chengzuopeng-stock-sdk.md) | ⭐ 1.9k | Trading |
| 4 | [wassim249/fastapi-langgraph-agent-production-ready-template](./templates/wassim249-fastapi-langgraph-agent-production-ready-template.md) | ⭐ 2.6k | Templates |
| 5 | [fastapi/full-stack-fastapi-template](./templates/fastapi-full-stack-fastapi-template.md) | ⭐ 44.7k | Templates |
| 6 | [sickn33/agentic-awesome-skills](./orchestration/sickn33-agentic-awesome-skills.md) | ⭐ 42.6k | Orchestration |
| 7 | [Panniantong/Agent-Reach](./mcp/panniantong-agent-reach.md) | ⭐ 44.7k | Mcp |
| 8 | [headroomlabs-ai/headroom](./orchestration/headroomlabs-ai-headroom.md) | ⭐ 46.8k | Orchestration |
| 9 | [hwchase17/langchain](./orchestration/hwchase17-langchain.md) | ⭐ 145k | Orchestration |
| 10 | [coze-dev/coze-studio](./knowledgerag/coze-dev-coze-studio.md) | ⭐ 21.3k | Knowledgerag |

## What each entry includes

| Signal | Why it matters |
|---|---|
| Repository activity | Stars, forks, language and last update provide a quick health snapshot |
| Practical summary | Concise English, Russian and Chinese context for faster evaluation |
| Fit and readiness | Use cases, integration notes, quality signals and production-readiness notes |
| Transparent score | A directional breakdown across usefulness, quality, integration, readiness, outlook and adoption |

## How it works

```mermaid
graph LR
  A[Approved discovery sources] --> B[AtlasRepo Scout]
  B --> C[Score · Dedupe · Categorize]
  C --> D[Summarize · Enrich]
  D --> E[AtlasRepo platform]
  D --> F[Open catalog]
```

1. **Discover** — collect candidates from approved public sources.
2. **Normalize** — deduplicate repositories and standardize metadata.
3. **Evaluate** — score practical value, quality, integration fit, readiness, outlook and adoption.
4. **Enrich** — add categories, summaries, use cases, quality signals and risk notes.
5. **Publish** — update the AtlasRepo platform and this open catalog.

## Install

### ChatGPT — hosted MCP plugin

1. Open **Settings → Security and login** and enable **Developer mode**.
2. Open [ChatGPT Plugins](https://chatgpt.com/#settings/Plugins), select **+**, and create a connection named `AtlasRepo`.
3. Set the MCP endpoint to `https://mcp.atlasrepo.com/mcp`, create the connection, and review the discovered read-only tools.

Developer mode availability depends on your account and workspace policy. See the [official OpenAI connection guide](https://developers.openai.com/plugins/deploy/connect-chatgpt).

### Claude Code

Plugin:

```text
/plugin marketplace add Arnon-hs/atlasrepo-skills
/plugin install atlasrepo@atlasrepo-skills
/reload-plugins
```

Hosted MCP only:

```bash
claude mcp add --transport http atlasrepo https://mcp.atlasrepo.com/mcp
```

Local npm MCP instead:

```bash
claude mcp add --transport stdio atlasrepo -- npx -y atlasrepo-mcp
```

Browse the [AtlasRepo Skills repository](https://github.com/Arnon-hs/atlasrepo-skills) or inspect the [`scout-rest-api` skill source](https://github.com/Arnon-hs/atlasrepo-skills/tree/main/plugins/atlasrepo/skills/scout-rest-api). Claude plugin commands follow the [official marketplace flow](https://code.claude.com/docs/en/discover-plugins); MCP-only commands follow the [official Claude MCP syntax](https://code.claude.com/docs/en/mcp).

## Data contract

- [`index.json`](./index.json) — machine-readable entry point, either a complete sorted index or a shard manifest for large snapshots.
- `data/repos-*.json` — machine-readable catalog shards when sharding is enabled.
- `<category>/README.md` — ranked category index.
- `<category>/<owner>-<name>.md` — human-readable project card with evidence and evaluation metadata.

## Trust boundary

Catalog records, scores, summaries and external installation commands are discovery aids, not endorsements or security guarantees. Verify repository ownership, current maintenance, dependencies, license compatibility and installation steps before adoption.

## License

MIT for this repository's catalog metadata. See [LICENSE](./LICENSE). Linked repositories remain governed by their respective licenses.
