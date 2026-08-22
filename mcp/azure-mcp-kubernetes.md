# Azure/mcp-kubernetes

[![Stars](https://img.shields.io/github/stars/Azure/mcp-kubernetes?style=flat-square&color=yellow)](https://github.com/Azure/mcp-kubernetes/stargazers) [![Forks](https://img.shields.io/github/forks/Azure/mcp-kubernetes?style=flat-square&color=blue)](https://github.com/Azure/mcp-kubernetes/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> A Model Context Protocol (MCP) server that enables AI assistants to interact with Kubernetes clusters. It serves as a bridge between AI tools (like Claude, Cursor, and GitHub Copilot) and Kubernetes

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 60 |
| 🍴 **Forks** | 18 |
| 💻 **Language** | Go |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-07-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`kubernetes` `mcp-server` `model-context-protocol`

## 🎯 Categories

MCP · AI/ML · Backend · DevOps/Infra

## 📝 Summary

### English

Azure/mcp‑kubernetes is a Go‑based Model Context Protocol server that lets AI assistants such as Claude, Cursor, or GitHub Copilot query and act on Kubernetes clusters, providing a standardized bridge between AI tools and real‑world infrastructure. Adoption is straightforward: begin with a small proof‑of‑concept, review the README, and verify integration feasibility before scaling. While the project shows promise (60★, recent updates), it is currently medium‑readiness—suitable for prototypes or internal workflows, but requires dependency checks, security review, and maintainer assessment before moving to production.

### Русский

Azure/mcp‑kubernetes — это сервер Model Context Protocol, который выступает мостом между AI‑ассистентами (Claude, Cursor, GitHub Copilot) и кластерами Kubernetes, позволяя им выполнять запросы и управлять ресурсами через единый протокол. Типовой сценарий внедрения — подключение AI‑агента к внутреннему кластеру для автоматизации DevOps‑операций (например, развертывание, мониторинг или отладка) после небольшого proof‑of‑concept и проверки README. Проект имеет среднюю готовность к production: полезен для прототипов и внутренних workflows, но перед выходом в продакшн требуется оценка зависимостей, безопасности и активности мейнтейнеров.

### 中文

Azure/mcp‑kubernetes 是一个基于 Model Context Protocol（MCP）的 Kubernetes 服务器，能够让 Claude、Cursor、GitHub Copilot 等 AI 助手通过统一协议直接访问和操作 Kubernetes 集群，从而实现 AI 驱动的基础设施自动化。典型的接入方式是在集群中部署该 MCP 服务器，然后在 AI 工具侧配置对应的 MCP 客户端或插件，完成工具‑集群的桥接。虽然项目活跃（60 颗星、Go 语言、最近更新），但生产可用性目前处于中等水平，适用于原型或内部工作流，正式产品化前建议进行许可证、安全及维护者评估的小规模 PoC。

## 🧭 Practical evaluation

**Value:** Azure/mcp-kubernetes helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 60 GitHub stars
- 18 forks
- updated 2026-07-14
- primary language: Go
- 3 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 32/100 |
| stars | 38/100 |
| topics | 38/100 |
| outlook | 73/100 |
| quality | 62/100 |
| recency | 100/100 |
| adoption | 36/100 |
| production | 74/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-14 · [View on GitHub](https://github.com/Azure/mcp-kubernetes) · [← Back to Mcp](./README.md)</sub>
