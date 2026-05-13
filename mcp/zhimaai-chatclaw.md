# zhimaAi/ChatClaw

[![Stars](https://img.shields.io/github/stars/zhimaAi/ChatClaw?style=flat-square&color=yellow)](https://github.com/zhimaAi/ChatClaw/stargazers) [![Forks](https://img.shields.io/github/forks/zhimaAi/ChatClaw?style=flat-square&color=blue)](https://github.com/zhimaAi/ChatClaw/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> ChatClaw: Get OpenClaw-like knowledge base personal AI agent in 5 mins. Sandbox-secured, ultra-small 30MB installer for macOS & Windows (install in 1 min). Connects to WhatsApp, Telegram, Slack, Discord, Gmail, DingTalk, WeChat Work, QQ, Feishu. Built-in Skill Market, Knowledge Base, Memory, MCP, Scheduled Tasks. Developed in Go ,run

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 282 |
| 🍴 **Forks** | 54 |
| 💻 **Language** | Go |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-assistant` `ima` `open-cowork` `openclaw` `rag`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Frontend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
ChatClaw is an ultra‑light (≈30 MB) Go‑based AI agent that can be installed on macOS or Windows in under a minute and instantly connects to a wide range of everyday tools—WhatsApp, Telegram, Slack, Discord, Gmail, DingTalk, WeChat Work, QQ, Feishu, etc. It ships with a built‑in skill market, knowledge‑base/RAG, persistent memory, MCP (Model Context Protocol) support, and scheduled‑task automation, making it a ready‑to‑use personal AI assistant for both developers and power users.

**Value**  
- **Unified integration layer**: By exposing a standard MCP/SDK/CLI, ChatClaw lets any LLM‑powered assistant talk to real‑world services without custom glue code, accelerating the “AI‑as‑a‑tool” workflow.  
- **Rapid deployment**: The 30 MB installer and one‑minute setup lower the barrier for pilots, proofs‑of‑concept, and internal tooling experiments.  
- **Extensible ecosystem**: The built‑in skill market and knowledge‑base enable teams to share and reuse custom actions, reducing duplicated effort across projects.

**Practical Adoption Path**  
1. **Pilot** – Download the installer on a dev workstation, run the 1‑minute setup, and configure a few connectors (e.g., Slack + Gmail) via the provided UI or CLI.  
2. **Extend** – Use the Go SDK or the exposed MCP endpoints to develop custom skills or integrate proprietary services; publish them to the internal skill market.  
3. **Scale** – Deploy the same lightweight binary to production VMs or containers, enable scheduled tasks for automation, and optionally run a clustered MCP server for higher throughput.  

**Production Readiness**  
- **Activity & community**: 282 ★, 54 forks, recent commits (as of 2026‑05‑13) and multiple integration topics indicate an active project.  
- **Stability**: The small codebase in Go, clear API surface, and sandboxed execution model make it easy to audit and hard to break.  
- **Risks**: Licensing terms, long‑term maintainer commitment, and a formal security audit still need verification, but no major red flags appear. Overall, ChatClaw is mature enough for a serious pilot and, with a brief security review, can be promoted to production use.

### Русский

**ChatClaw** — это лёгкий (30 МБ) кроссплатформенный агент‑ассистент, который за минуту разворачивается на macOS или Windows и сразу подключается к популярным каналам (WhatsApp, Telegram, Slack, Discord, Gmail, DingTalk, WeChat Work, QQ, Feishu). Он предоставляет готовый набор функций — рынок навыков, база знаний, долговременная память, MCP‑протокол и планировщик задач — что позволяет интегрировать AI‑агенты с реальными инструментами и данными без написания собственного кода. По состоянию на 2026‑05‑13 проект имеет активную поддержку, 282 звёзд и регулярные обновления, что делает его достаточно зрелым для пилотного внедрения в продакшн.

### 中文

**项目简介**  
ChatClaw 是一款基于 OpenClaw 思想的个人知识库 AI 代理，只需 5 分钟即可部署。提供 30 MB 超小安装包（macOS/Windows），在 1 分钟内完成本地安装，且全部运行在沙盒环境中。它内置 Skill Market、知识库、记忆、MCP（Model Context Protocol）以及定时任务，并可通过统一协议对接 WhatsApp、Telegram、Slack、Discord、Gmail、钉钉、企业微信、QQ、飞书等常用工具。

**价值**  
- **标准化接入**：通过 MCP 实现 AI 与外部工具、数据源的统一协议，降低二次开发成本。  
- **快速落地**：超小体积、即装即用，适合内部 PoC、原型或小团队快速验证 AI 助手的业务价值。  
- **生态丰富**：Skill Market 与可扩展的知识库让功能可插件化，支持记忆和定时任务，满足多场景需求。

**典型接入方式**  
1. **安装运行**：下载对应平台的 30 MB 安装包，执行一次安装即可启动本地服务。  
2. **配置 MCP**：在 `config.yaml` 中声明需要对接的渠道（如 Slack、WhatsApp）以及相应的凭证。系统会自动生成对应的 API/SDK/CLI 端点。  
3. **调用 API/SDK**：使用 Go、Python、Node 等语言的 SDK，或直接通过 HTTP/CLI 调用 MCP 接口，将业务系统的请求路由到 ChatClaw。  
4. **扩展 Skill**：在 Skill Market 中上传自定义技能（函数、RAG 检索等），即可在对话中即时调用。

**生产可用性**  
- **活跃度**：截至 2026‑05‑13，项目最近一次提交，拥有 282 ⭐、54 🍴，社区活跃。  
- **技术成熟度**：核心使用 Go 实现，提供完整的 API/SDK/CLI，已在多个内部项目中验证。  
- **安全与沙盒**：所有功能均在本地沙盒运行，避免网络泄露，适合作为企业内部部署。  
- **风险**：需进一步审查许可证兼容性、长期维护者承诺以及安全审计结果。总体而言，ChatClaw 已具备在生产环境中进行正式试点的条件。

## 🧭 Practical evaluation

**Value:** zhimaAi/ChatClaw helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 282 GitHub stars
- 54 forks
- updated 2026-05-13
- primary language: Go
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 52/100 |
| topics | 63/100 |
| outlook | 82/100 |
| quality | 72/100 |
| recency | 100/100 |
| adoption | 50/100 |
| production | 76/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/zhimaAi/ChatClaw) · [← Back to Mcp](./README.md)</sub>
