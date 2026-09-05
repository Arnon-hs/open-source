# gensecaihq/Wazuh-Openclaw-Autopilot

[![Stars](https://img.shields.io/github/stars/gensecaihq/Wazuh-Openclaw-Autopilot?style=flat-square&color=yellow)](https://github.com/gensecaihq/Wazuh-Openclaw-Autopilot/stargazers) [![Forks](https://img.shields.io/github/forks/gensecaihq/Wazuh-Openclaw-Autopilot?style=flat-square&color=blue)](https://github.com/gensecaihq/Wazuh-Openclaw-Autopilot/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Autonomous SOC layer for Wazuh using OpenClaw agents with MCP . Auto-triage alerts, correlate incidents,           generate response plans with human-in-the-loop approval. Evidence packs, Prometheus metrics, Slack       integration.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 35 |
| 🍴 **Forks** | 13 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `agentic-ai` `agents` `autonomous` `autonomous-agents` `mcp` `openclaw` `security-automation` `siem` `soc` `threat-detection` `wazuh`

## 🎯 Categories

MCP · Automation · AI/ML · Communication · Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *Wazuh‑Openclaw‑Autopilot* project adds an autonomous SOC layer on top of Wazuh by leveraging OpenClaw agents and the Model‑Context‑Protocol (MCP). It automatically triages alerts, correlates incidents, and builds response playbooks that are presented for human‑in‑the‑loop approval, while also exporting evidence packs, Prometheus metrics, and Slack notifications.  

**Value**  
- **AI‑augmented security operations** – By connecting AI assistants to Wazuh through a standardized MCP interface, the platform can ingest raw alerts, run ML‑based triage, and suggest concrete remediation steps, dramatically cutting analyst fatigue and mean‑time‑to‑response.  
- **Standardised integration point** – MCP serves as a vendor‑agnostic contract, making it easy to swap or add new AI agents, tooling, or data sources without rewriting custom glue code.  
- **Observability & collaboration** – Built‑in Prometheus exporters and Slack hooks give teams real‑time visibility into automation health and enable rapid incident communication.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, spin up the provided Docker compose stack (Wazuh, OpenClaw, MCP server) and run the sample JavaScript agent to verify alert ingestion and auto‑triage on a test environment.  
2. **Integrate** – Replace the sample agent with your own AI model or LLM endpoint via the MCP SDK, map your organization’s alert taxonomy, and configure Slack/Prometheus endpoints.  
3. **Human‑in‑the‑loop rollout** – Enable the approval UI for response plans, pilot with a small SOC team, and iterate on correlation rules and evidence‑pack templates.  
4. **Scale** – Deploy the stack on Kubernetes, add HA for the MCP server, and externalise secrets (e.g., Vault) before moving to production.  

**Production Readiness**  
- **Maturity**: Medium. The codebase is recent (last update 2026‑06‑23) and functional for prototypes, but it still requires thorough dependency vetting, security review of the MCP server, and possibly adding persistence/backup for evidence packs.  
- **Signals**: 35 GitHub stars, 13 forks, primary language JavaScript, and clear API/CLI exposure indicate a usable foundation, though the community is small.  
- **Risks**: No critical metadata issues yet, but the license, long‑term maintainer commitment, and the security posture of the MCP server need final confirmation before a production deployment.  

Overall, *Wazuh‑Openclaw‑Autopilot* offers a compelling way to bring AI‑driven automation into a Wazuh‑based SOC, with a clear path from sandbox testing to production once the outstanding governance and hardening steps are addressed.

### Русский

**gensecaihq/Wazuh-Openclaw-Autopilot** – открытый проект, который добавляет автономный слой SOC к Wazuh, используя OpenClaw‑агентов и Model Context Protocol (MCP). Он автоматически триажирует тревоги, коррелирует инциденты и генерирует планы реагирования, требующие лишь одобрения человека; результаты упаковываются в «evidence packs», а метрики экспортируются в Prometheus и оповещения отправляются в Slack. Проект находится на среднем уровне готовности к продакшн: подходит для прототипов и внутренних процессов, но перед запуском в production требуется проверка зависимостей, лицензии и поддержка.

### 中文

**项目简介**  
gensecaihq/Wazuh-Openclaw-Autopilot 为 Wazuh 提供了一个基于 OpenClaw 代理的自主 SOC 层，利用 MCP（Model Context Protocol）实现自动化告警分流、事件关联和响应方案生成，并支持人工审批、证据包输出、Prometheus 监控以及 Slack 通知。

**价值**  
- **AI‑to‑Tool 桥梁**：通过标准化的 MCP 接口，将大模型或 AI 助手直接连接到真实的安全工具和监控数据，实现“AI 赋能的安全运营”。  
- **自动化与可视化**：自动 triage、关联分析和响应计划降低了响应时延；Prometheus 指标和 Slack 通知提供即时可观测性。  
- **可审计的人工介入**：在关键响应步骤加入 human‑in‑the‑loop 审批，兼顾效率与合规。

**典型接入方式**  
1. **部署 OpenClaw 代理**：在受监控主机上运行 OpenClaw 代理，使用提供的 API/SDK 与 Wazuh 交互。  
2. **启动 MCP Server**：在控制节点运行项目自带的 MCP 服务器（Node.js/JavaScript），该服务器负责转发 AI 请求、收集指标并调用 OpenClaw API。  
3. **集成外部系统**：通过配置文件或环境变量接入 Prometheus（抓取 `/metrics`）和 Slack（Webhook URL），即可获得监控和告警推送。  
4. **AI 助手对接**：在 AI 平台（如 ChatGPT、Claude）中使用 MCP 客户端库，发送 “生成响应计划” 等指令，系统返回结构化的响应方案供人工批准。

**生产可用性**  
- **成熟度**：目前评分 72/100，GitHub 35 星、13 Fork，代码最近一次更新于 2026‑06‑23，表明仍在活跃维护中。  
- **适用场景**：适合原型开发、内部 SOC 流程自动化或作为 AI‑Security 集成的参考实现。  
- **风险与准备**：依赖 Node.js 运行时和 OpenClaw 代理，需要对其安全补丁和许可证进行额外审查；在正式生产环境部署前建议进行依赖锁定、容器化封装以及灾备演练。  

总体而言，Wazuh-Openclaw-Autopilot 为希望在安全运营中引入 AI 自动化的团队提供了一个即插即用的解决方案，具备中等的生产可用性，只要完成常规的安全与运维审查即可投入使用。

## 🧭 Practical evaluation

**Value:** gensecaihq/Wazuh-Openclaw-Autopilot helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 35 GitHub stars
- 13 forks
- updated 2026-06-23
- primary language: JavaScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 32/100 |
| production | 66/100 |
| usefulness | 100/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/gensecaihq/Wazuh-Openclaw-Autopilot) · [← Back to Mcp](./README.md)</sub>
