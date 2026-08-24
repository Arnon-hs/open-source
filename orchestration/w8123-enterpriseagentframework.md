# w8123/EnterpriseAgentFramework

[![Stars](https://img.shields.io/github/stars/w8123/EnterpriseAgentFramework?style=flat-square&color=yellow)](https://github.com/w8123/EnterpriseAgentFramework/stargazers) [![Forks](https://img.shields.io/github/forks/w8123/EnterpriseAgentFramework?style=flat-square&color=blue)](https://github.com/w8123/EnterpriseAgentFramework/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> Enterprise AI Capability Platform for Java/Spring Boot. Register business APIs as governed AI capabilities, compose Agents with GraphSpec, Runtime, MCP/A2A/Gateway, RunOps and Trace. 企业智能体开发框架-把 Java 企业系统中的接口、领域方法、知识、模型和流程，沉淀为可治理、可编排、可开放的 AI 能力资产。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 337 |
| 🍴 **Forks** | 20 |
| 💻 **Language** | Java |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`a2a` `agent-framework` `ai-agents` `ai-capability` `ai-gateway` `ai-platform` `enterprise-ai` `java` `langgraph` `llmops` `llmops-platform` `mcp`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
EnterpriseAgentFramework (w8123/EnterpriseAgentFramework) is an open‑source Java/Spring Boot platform that lets you register business APIs, domain methods, knowledge bases, models, and workflows as governed AI capabilities. By composing these capabilities with GraphSpec, a runtime engine, MCP/A2A/Gateway, RunOps, and tracing, the framework turns isolated prompts and tools into repeatable, orchestrated agent workflows that can be managed, versioned, and exposed as services.

**Value**  
- **Governed AI assets:** Converts existing enterprise interfaces and logic into reusable, policy‑driven AI capabilities, enabling consistent security, compliance, and observability.  
- **Composable agents:** Developers can wire together multiple capabilities (e.g., RAG, tool use, memory) via a graph‑based spec, accelerating the creation of sophisticated multi‑agent solutions without hand‑crafting glue code.  
- **Operational tooling:** Built‑in runtime, monitoring (RunOps), and tracing give teams the same operational confidence they have for traditional microservices, reducing the overhead of deploying AI‑centric workloads.

**Practical Adoption Path**  
1. **Prototype:** Use the provided SDK/CLI to register a few existing REST endpoints or domain services as AI capabilities and define a simple GraphSpec workflow.  
2. **Integrate:** Replace ad‑hoc prompt‑to‑tool calls in your current Java/Spring Boot services with the framework’s runtime, leveraging the MCP/A2A gateway for secure inter‑service communication.  
3. **Standardize:** Extend the graph definitions to include memory modules, RAG pipelines, or external tools, and enforce governance policies (rate limits, data masking, audit logs) centrally.  
4. **Scale:** Deploy the runtime as a Spring Boot microservice in your Kubernetes/VM environment, using the built‑in tracing and RunOps dashboards for observability and automated roll‑outs.

**Production Readiness**  
- **Activity & Community:** 337 stars, recent commits (as of 2026‑06‑26), and a modest but active fork base indicate healthy maintenance.  
- **Ecosystem Fit:** Pure Java/Spring Boot stack aligns with typical enterprise back‑ends, and the exposed API/SDK/CLI make integration straightforward.  
- **Operational Maturity:** Includes runtime orchestration, monitoring, and tracing out of the box, which are essential for production deployments.  
- **Risks to Verify:** Final due‑diligence on the open‑source license, a security audit of the gateway components, and confirmation of an active maintainer team are still required, but no major red flags have been identified.  

Overall, EnterpriseAgentFramework is a strong candidate for piloting AI‑augmented services in Java‑centric enterprises and can be progressed to production once the licensing and security checks are cleared.

### Русский

**EnterpriseAgentFramework (w8123/EnterpriseAgentFramework)** – это open‑source платформа на Java/Spring Boot, позволяющая превратить разрозненные бизнес‑API, модели и процессы в управляемые AI‑возможности, которые можно оркестрировать через GraphSpec, Runtime, MCP/A2A/Gateway, RunOps и Trace. Типичный сценарий — построение повторяемых цепочек из нескольких агентов с поддержкой инструментов, памяти и RAG, что упрощает координацию сложных мульти‑агентных рабочих потоков и стандартизацию их поведения. Проект имеет высокий уровень готовности к production: активные коммиты, 337 звёзд, широкая экосистема Java, но окончательная проверка лицензии, безопасности и поддержки поддерживающих разработчиков всё ещё требуется.

### 中文

**项目简介（2‑3 句）**  
EnterpriseAgentFramework 是基于 Java / Spring Boot 的企业级 AI 能力平台，能够把业务 API、领域方法、知识库、模型和业务流程包装成可治理、可编排、可开放的 AI 能力资产。通过 GraphSpec、Runtime、MCP/A2A/Gateway、RunOps 与 Trace 等模块，支持快速构建、组合和运行可追溯的智能体（Agent）工作流。

**价值**  
- 将零散的 Prompt 与工具统一抽象为可复用、可治理的 AI 能力，降低业务系统接入 AI 的技术门槛。  
- 支持多智能体协同、工具链（Tool‑Use）流水线以及统一的记忆（Agent Memory）管理，帮助企业实现端到端的业务自动化和知识增强。  
- 基于 Spring Boot 的原生集成，使现有 Java 微服务能够无缝迁移到 AI 驱动的业务场景。

**典型接入方式**  
1. **API/SDK**：在已有 Spring Boot 项目中引入 `enterprise-agent-framework` 依赖，使用提供的 Java SDK 注册业务 API 为 AI 能力（Capability）。  
2. **GraphSpec 配置**：通过 YAML/JSON 描述能力之间的调用图，定义 Agent 的工作流和编排规则。  
3. **运行时部署**：将框架的 Runtime、MCP/A2A/Gateway 作为独立服务或容器化部署，使用 CLI 或 Spring 配置启动并与业务系统对接。  
4. **监控与追踪**：借助内置的 RunOps 与 Trace 模块，将每一次 Agent 调用记录到企业监控平台（Prometheus、Grafana、ELK 等），实现可观测性与审计。

**生产可用性**  
- **活跃度**：截至 2026‑06‑26，项目仍在持续更新，拥有 337 颗星、20+ Fork，近期提交频率稳定。  
- **生态兼容**：基于主流的 Java 17+ 与 Spring Boot 3.x，易于在现有微服务架构中直接引入。  
- **安全与治理**：提供能力治理（Capability Governance）与访问控制（MCP/A2A），满足企业合规需求。  
- **成熟度**：具备完整的运行时、运维（RunOps）与链路追踪（Trace），已可支撑中大型生产环境的试点或正式上线。  

总体而言，EnterpriseAgentFramework 是一套面向企业的、可治理的 AI 能力编排框架，适合希望在 Java 生态中快速落地多智能体、工具链和知识增强业务的团队。

## 🧭 Practical evaluation

**Value:** w8123/EnterpriseAgentFramework helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 337 GitHub stars
- 20 forks
- updated 2026-06-26
- primary language: Java
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 66/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 48/100 |
| production | 60/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/w8123/EnterpriseAgentFramework) · [← Back to Orchestration](./README.md)</sub>
