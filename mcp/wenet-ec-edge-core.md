# wenet-ec/edge-core

[![Stars](https://img.shields.io/github/stars/wenet-ec/edge-core?style=flat-square&color=yellow)](https://github.com/wenet-ec/edge-core/stargazers) [![Forks](https://img.shields.io/github/forks/wenet-ec/edge-core?style=flat-square&color=blue)](https://github.com/wenet-ec/edge-core/network) [![Language](https://img.shields.io/badge/lang-Elixir-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> Open-source distributed machine control plane — WireGuard mesh, SSH proxy, remote execution, Prometheus metrics, all over one REST API/MCP.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 21 |
| 🍴 **Forks** | 1 |
| 💻 **Language** | Elixir |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`automation` `command-line` `edge-ai` `edge-computing` `mcp-server` `mesh-networks` `prometheus-metrics` `proxy-server` `ssh-server` `vpn` `wireguard`

## 🎯 Categories

MCP · Automation · AI/ML · Backend · Observability

## 📝 Summary

### English

**Brief Summary**  
wenet‑ec/edge‑core is an open‑source distributed control plane that bundles a WireGuard mesh, SSH proxy, remote‑execution engine, and Prometheus metrics behind a single REST/MCP API. Written in Elixir, it lets developers expose a uniform “Model Context Protocol” for AI agents to invoke real‑world tools and data sources.

**Value**  
The project provides a turnkey way to bridge large‑language‑model assistants with concrete infrastructure: a secure mesh network, observable metrics, and a programmable execution layer are all reachable through a single, language‑agnostic API/SDK. This eliminates the need to stitch together separate VPN, SSH, and monitoring components, accelerating the creation of AI‑driven automation and tool‑integration services.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1. **Prototype** | Clone the repo, run the provided Docker compose or local Elixir mix setup, and call the REST API from a sandboxed AI agent. | Quick validation that the MCP endpoints work and that WireGuard/SSH tunnels can be provisioned on your test nodes. |
| 2. **Integrate** | Add the generated SDK (or use the CLI) to your existing service, configure the mesh topology and Prometheus scrape targets, and expose the needed tool endpoints via the remote‑execution interface. | Leverages the existing API contract and lets you reuse your language‑specific client libraries. |
| 3. **Secure & Harden** | Review the license, perform a security audit of the WireGuard keys handling and SSH proxy, and set up role‑based access control via the MCP auth layer. | Addresses the current “medium” production readiness rating and mitigates supply‑chain risk. |
| 4. **Observability & Scaling** | Deploy the service in a Kubernetes or Nomad cluster, enable Prometheus scraping, and configure alerts for mesh health and execution failures. | Provides the observability needed for production monitoring and capacity planning. |
| 5. **Production Roll‑out** | Gradually shift traffic from legacy tool‑integration pipelines to edge‑core, using canary releases and automated tests that verify AI‑agent calls succeed. | Ensures a smooth transition while confirming reliability under real load. |

**Production Readiness**  
- **Maturity**: Medium – the codebase is recent (last update 2026‑06‑23) and has modest community traction (21 stars, 1 fork). It is suitable for prototypes, internal tooling, or early‑stage services, but it still requires a thorough security review and possibly additional testing for high‑availability scenarios.  
- **Dependencies**: Built on Elixir/Erlang, which offers strong concurrency and fault tolerance, but teams unfamiliar with the BEAM ecosystem will need to allocate ramp‑up time.  
- **Maintainability**: Limited contributor base; you should plan for internal ownership (e.g., a dedicated maintainer) or contribute back fixes.  

Overall, edge‑core can accelerate AI‑agent integration projects when you need a unified, observable, and secure control plane, provided you allocate resources for security hardening and ongoing maintenance before treating it as a mission‑critical production component.

### Русский

**wenet-ec/edge‑core** — открытая распределённая система управления: WireGuard‑мэш, SSH‑прокси, удалённое исполнение и метрики Prometheus доступны через единый REST‑API/MCP. Проект позволяет быстро подключать AI‑ассистентов к реальным инструментам и данным, стандартизируя интеграцию и упрощая развертывание Model Context Protocol серверов. Готов к использованию в прототипах и внутренних workflow, но перед запуском в продакшн требуется проверка лицензии, безопасности и уровня поддержки.

### 中文

**项目简介**  
wenet-ec/edge‑core 是一套开源的分布式机器控制平面，提供基于 WireGuard 的网状网络、SSH 代理、远程执行、Prometheus 监控等功能，并统一暴露在单一的 REST API / MCP 接口上。

**价值**  
- 为 AI 助手提供统一、标准化的“工具与数据”接入层，使其能够安全、低延迟地调用真实的后端资源。  
- 将 Model Context Protocol（MCP）与基础设施（网络、SSH、监控）融合，简化 AI‑to‑Ops 场景的集成工作。  
- 通过 REST/MCP 一站式管理，降低多系统拼接的运维成本，提升可观测性与安全审计能力。

**典型接入方式**  
1. **API/SDK**：直接调用公开的 REST 端点或使用项目提供的 Elixir SDK，完成节点注册、WireGuard 隧道创建、SSH 代理转发等操作。  
2. **CLI**：通过项目自带的命令行工具执行远程命令、查询拓扑或导出 Prometheus 指标，适合脚本化集成。  
3. **语言元数据**：项目在 GitHub 上标记了多语言元信息，可在 CI/CD 流水线或微服务框架中快速生成对应的客户端代码。  

**生产可用性**  
- **成熟度**：目前处于 **Medium** 级别，已足以支撑原型、内部工具或低风险业务的部署。  
- **依赖与维护**：核心实现基于 Elixir，社区活跃度一般（≈21 Stars，1 Fork），需自行评估安全审计、许可证合规以及长期维护计划。  
- **上线建议**：在生产环境使用前，建议完成以下检查：  
  1. 对 WireGuard 配置和 SSH 代理进行安全加固。  
  2. 在独立的测试集群验证 API 稳定性与 Prometheus 指标的可靠性。  
  3. 设立监控和告警，确保节点失联或隧道异常时能够快速响应。  

总体而言，wenet-ec/edge-core 为 AI 与真实工具的桥接提供了统一且可观测的基础设施层，适合作为原型或内部平台的核心组件，经过适当的安全与运维审查后即可投入生产使用。

## 🧭 Practical evaluation

**Value:** wenet-ec/edge-core helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 21 GitHub stars
- 1 forks
- updated 2026-06-23
- primary language: Elixir
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 8/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 50/100 |
| recency | 40/100 |
| adoption | 23/100 |
| production | 54/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/wenet-ec/edge-core) · [← Back to Mcp](./README.md)</sub>
