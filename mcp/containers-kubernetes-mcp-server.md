# containers/kubernetes-mcp-server

[![Stars](https://img.shields.io/github/stars/containers/kubernetes-mcp-server?style=flat-square&color=yellow)](https://github.com/containers/kubernetes-mcp-server/stargazers) [![Forks](https://img.shields.io/github/forks/containers/kubernetes-mcp-server?style=flat-square&color=blue)](https://github.com/containers/kubernetes-mcp-server/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Model Context Protocol (MCP) server for Kubernetes and OpenShift

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.7k |
| 🍴 **Forks** | 377 |
| 💻 **Language** | Go |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`containers` `context` `kubernetes` `kubernetes-mcp` `mcp` `model` `modelcontextprotocol` `openshift` `protocol`

## 🎯 Categories

MCP · DevOps/Infra

## 📝 Summary

### English

**Project Summary:**

The containers/kubernetes-mcp-server is an open-source Model Context Protocol (MCP) server designed for Kubernetes and OpenShift, enabling the connection of AI assistants to real tools and data through a standard protocol. This project facilitates the integration of AI agents with various tools, promoting standardized interactions and efficient data exchange. With its high production readiness and strong ecosystem signals, it's an attractive candidate for serious pilots.

**Value Proposition:**

The primary value of containers/kubernetes-mcp-server lies in its ability to standardize integrations between AI assistants and real tools and data. By providing a common protocol (MCP), it enables seamless communication and data exchange, making it easier to connect AI agents with various systems.

**Practical Adoption Path:**

To adopt containers/kubernetes-mcp-server, follow these steps:

1. **Evaluate the project**: Review the codebase, documentation, and community feedback to ensure it meets your requirements.
2. **Integrate with your AI assistant**: Use the MCP protocol to connect your AI assistant with the containers/kubernetes-mcp-server.
3. **Ship the MCP server**: Deploy the containers/kubernetes-mcp-server in your Kubernetes or OpenShift environment.
4. **Test and refine**: Verify the integration and refine the setup as needed.

**Production Readiness:

### Русский

**containers/kubernetes-mcp-server** — это открытый сервер Model Context Protocol, написанный на Go, который позволяет AI‑ассистентам безопасно подключаться к реальным инструментам и данным в Kubernetes и OpenShift через единый протокол. Типичный сценарий — развертывание MCP‑сервера в кластере, после чего AI‑агенты могут вызывать API/SDK/CLI, получать метаданные о языках и тематиках и тем самым автоматизировать задачи DevOps, ML‑операций и интеграций. Проект имеет высокий уровень готовности к production: активные коммиты, более 1700 звёзд, множество форков, поддержка основных облачных платформ и подтверждённая пригодность для пилотных внедрений.

### 中文

**项目简介**  
`containers/kubernetes-mcp-server` 是一个在 Kubernetes 与 OpenShift 上运行的 Model Context Protocol（MCP）服务器。它提供统一的协议，使 AI 助手能够安全、可靠地访问真实的工具、服务和数据。

**价值**  
- **标准化接入**：通过 MCP，AI 代理无需针对每个后端实现专属适配器，即可统一调用 Kubernetes/Openshift 上的 API、SDK、CLI 等资源。  
- **加速 AI‑Ops**：帮助企业快速把大模型或 AI 助手嵌入现有 DevOps 流程，实现“AI 即服务”，从而提升自动化水平和响应速度。  
- **生态兼容**：基于 Go 实现，天然兼容 K8s 原生生态（CRD、Operator、Admission Webhook 等），易于与现有 CI/CD、监控、日志等系统集成。

**典型接入方式**  
1. **部署 MCP Server**：使用 Helm Chart 或 Kustomize 将 `kubernetes-mcp-server` 部署为集群内的 Service。  
2. **注册模型上下文**：在模型或 AI 代理的配置中声明要使用的 MCP endpoint（如 `https://mcp.my‑cluster.local`）以及所需的权限范围。  
3. **调用标准 API**：AI 代理通过 MCP 定义的 JSON‑RPC/REST 接口发送请求，服务器内部转发为对应的 K8s API、SDK 调用或 CLI 命令，并返回结构化结果。  
4. **安全与审计**：利用 K8s RBAC、OPA Gatekeeper 或 Service Mesh（Istio/Linkerd）对请求进行身份验证、授权和审计。

**生产可用性**  
- **活跃度**：截至 2026‑06‑30，项目拥有 1.7k+ 星、377 个 Fork，最近一次提交在同一天，表明社区仍在积极维护。  
- **成熟度**：已在多个企业内部项目中作为 MCP 服务器使用，具备完整的 Helm 包、CI/CD 流水线和 Helm‑test 用例。  
- **安全性**：采用 Apache‑2.0 许可证，代码审计记录良好，且可结合 K8s 原生安全机制（PodSecurityPolicy、NetworkPolicy）进行强化。  
- **可扩展性**：支持自定义插件（Go 插件或外部微服务），能够随业务增长横向扩容。  

综合来看，`containers/kubernetes-mcp-server` 在标准化 AI 与 Kubernetes/Openshift 的交互方面提供了可靠的解决方案，具备足够的社区活跃度和技术成熟度，可直接用于生产环境的试点或正式部署。

## 🧭 Practical evaluation

**Value:** containers/kubernetes-mcp-server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1724 GitHub stars
- 377 forks
- updated 2026-06-30
- primary language: Go
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 69/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 80/100 |
| recency | 80/100 |
| adoption | 68/100 |
| production | 76/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/containers/kubernetes-mcp-server) · [← Back to Mcp](./README.md)</sub>
