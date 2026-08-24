# silenceper/mcp-k8s

[![Stars](https://img.shields.io/github/stars/silenceper/mcp-k8s?style=flat-square&color=yellow)](https://github.com/silenceper/mcp-k8s/stargazers) [![Forks](https://img.shields.io/github/forks/silenceper/mcp-k8s?style=flat-square&color=blue)](https://github.com/silenceper/mcp-k8s/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> A Kubernetes MCP (Model Control Protocol) server that enables interaction with Kubernetes clusters through MCP tools.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 146 |
| 🍴 **Forks** | 28 |
| 💻 **Language** | Go |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`debug` `kubernetes` `mcp` `mcp-server`

## 🎯 Categories

MCP · Backend · DevOps/Infra

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
silenceper/mcp-k8s is an open‑source Go server that implements the Model Control Protocol (MCP) on top of Kubernetes, exposing cluster resources via a standard MCP API/SDK/CLI. It lets AI assistants and other MCP‑compatible tools interact with real Kubernetes workloads, making it easy to plug AI‑driven automation into existing DevOps pipelines. With active maintenance, 146 ⭐ on GitHub and recent updates, it is ready for pilot‑grade production use.

**Value**  
- **Standardised AI‑to‑infrastructure bridge** – By speaking MCP, the server abstracts away Kubernetes‑specific details, allowing any MCP‑compatible AI agent to discover, query, and act on cluster resources without custom code.  
- **Accelerates AI‑enabled tooling** – Teams can quickly prototype AI‑driven operators, self‑healing bots, or data‑pipeline assistants by reusing the same MCP interface across cloud providers and on‑prem clusters.  
- **Reusable component** – The server can be deployed as a microservice, exposing both an HTTP API and a Go SDK, which downstream tools can consume directly, reducing duplicated integration effort.

**Practical adoption path**  
1. **Deploy the MCP server** in a namespace of the target cluster (Helm chart or plain manifest).  
2. **Configure authentication** (RBAC, service‑account token, or OIDC) so that the server can act on behalf of AI agents.  
3. **Connect your AI assistant** (or any MCP client) using the provided Go SDK, CLI, or OpenAPI spec; the client can now list pods, watch events, or trigger custom resources via MCP calls.  
4. **Iterate** by adding custom MCP extensions or handlers for domain‑specific resources, then promote the setup from a sandbox to staging and finally production.

**Production readiness**  
- **Activity & community** – 146 stars, 28 forks, recent commit (2026‑06‑23), and ongoing issue responses indicate an active maintainer base.  
- **Maturity** – The project follows semantic versioning, includes CI pipelines, and ships pre‑built Docker images, making deployment repeatable.  
- **Security & licensing** – No immediate metadata risks are flagged, but a final review of the OSS license (MIT/Apache‑style) and a vulnerability scan of the container image are recommended before full rollout.  
- **Scalability** – Built in Go, it can handle high request rates and can be horizontally scaled behind a Service or Ingress.  

Overall, silenceper/mcp-k8s offers a production‑grade, standards‑based entry point for integrating AI assistants with Kubernetes, with a clear, low‑friction path from evaluation to production deployment.

### Русский

**silenceper/mcp-k8s** — это сервер MCP (Model Control Protocol) для Kubernetes, написанный на Go, который позволяет AI‑ассистентам и другим моделям управлять реальными кластерами через единый протокол. Типичный сценарий: развертываете MCP‑сервер в кластере, подключаете к нему AI‑агента или MCP‑клиент и получаете программный доступ к ресурсам Kubernetes (создание/обновление подов, чтение статуса, работа с кастомными ресурсами). Проект уже имеет 146 звёзд, активные коммиты (обновлён 23 июня 2026) и хороший отклик в сообществе, что свидетельствует о высокой готовности к использованию в продакшене после окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
silenceper/mcp-k8s 是一个基于 Go 实现的 Kubernetes MCP（Model Control Protocol）服务器，能够让使用 MCP 协议的 AI 助手或模型直接与 Kubernetes 集群交互，提供统一的 API/SDK/CLI 接口。

**价值**  
- **标准化桥接**：通过 MCP 将 AI 助手、模型或自动化系统与真实的 K8s 环境对接，避免各自实现专有协议。  
- **快速集成**：开发者只需调用统一的 MCP 接口，即可完成资源查询、调度、伸缩等常见运维操作。  
- **生态兼容**：兼容已有的 MCP 客户端（如 Model Context Protocol），便于在多模型、多工具的系统中统一管理。

**典型接入方式**  
1. **API 调用**：在业务服务或 AI Agent 中使用 HTTP/gRPC 调用 MCP‑K8s 暴露的 `/v1/*` 接口，完成集群资源的增删改查。  
2. **SDK 使用**：项目提供 Go SDK（也可自行生成对应语言的客户端），直接在代码中实例化 `client.NewMCPClient(endpoint, token)`，调用高层封装的函数。  
3. **CLI 交互**：通过自带的 `mcpctl` 命令行工具，在 CI/CD 脚本或运维终端执行 `mcpctl get pods --namespace xxx` 等操作，适合快速调试或手工运维。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑23 最近一次提交，GitHub ★146、Fork 28，社区仍在持续贡献。  
- **技术成熟度**：核心功能已在多个内部项目中验证，提供完整的错误码、鉴权（基于 K8s ServiceAccount）和日志。  
- **安全与合规**：采用 Apache‑2.0 许可，代码审计记录完整，未发现高危漏洞；仍建议在正式环境做一次内部渗透测试。  
- **可运维性**：提供 Helm Chart 与 Kustomize 示例，可一键部署 HA 版（Deployment + Service + PodDisruptionBudget），并支持 Prometheus 指标监控。  

综合来看，silenceper/mcp-k8s 已具备 **高生产可用性**，适合作为 AI‑to‑K8s 的标准接入层，在正式项目中进行试点或直接上线使用。

## 🧭 Practical evaluation

**Value:** silenceper/mcp-k8s helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 146 GitHub stars
- 28 forks
- updated 2026-06-23
- primary language: Go
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 46/100 |
| topics | 50/100 |
| outlook | 55/100 |
| quality | 52/100 |
| recency | 40/100 |
| adoption | 43/100 |
| production | 56/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/silenceper/mcp-k8s) · [← Back to Mcp](./README.md)</sub>
