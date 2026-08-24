# OpsinTech/opsintech-platform

[![Stars](https://img.shields.io/github/stars/OpsinTech/opsintech-platform?style=flat-square&color=yellow)](https://github.com/OpsinTech/opsintech-platform/stargazers) [![Forks](https://img.shields.io/github/forks/OpsinTech/opsintech-platform?style=flat-square&color=blue)](https://github.com/OpsinTech/opsintech-platform/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> OpsinTech Platform — An enterprise-grade AI agent platform built on LangGraph, featuring multi-tenant architecture, role-based access control, sandboxed tool execution, and an admin UI for managing models, MCP servers, skills, and tools. Designed for production deployment with Docker, PostgreSQL support, and comprehensive governance capabilities.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 89 |
| 🍴 **Forks** | 16 |
| 💻 **Language** | Python |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Orchestration · MCP · AI/ML · Database · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
OpsinTech Platform is an enterprise‑grade AI‑agent framework built on LangGraph that provides a multi‑tenant, role‑based architecture with sandboxed tool execution and a full‑featured admin UI for managing models, MCP servers, skills, and tools. Packaged for production with Docker, PostgreSQL support, and extensive governance features, it turns isolated prompts and utilities into repeatable, orchestrated agent workflows. With active maintenance, a growing user base, and strong ecosystem signals, it is ready for serious pilot deployments.

**Value**  
- **Workflow Standardisation** – Converts ad‑hoc prompts and tool calls into reusable, version‑controlled agent pipelines, reducing duplication and improving reliability.  
- **Governance & Security** – Role‑based access control, sandboxed execution, and audit‑ready administration let organisations enforce policies while still enabling rapid AI experimentation.  
- **Scalability** – Multi‑tenant design and MCP (Micro‑Control‑Plane) integration let multiple teams share the same infrastructure without interference, supporting large‑scale, production‑level deployments.

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – Clone the repo, spin up the Docker compose stack (API, PostgreSQL, admin UI) and run the provided example agents to validate basic functionality.  
2. **Integration Checklist** – Review the README for required environment variables, configure your own model endpoints and MCP servers, and replace the sample skills/tools with internal ones.  
3. **Security Review** – Perform a lightweight security audit of the Docker images and the sandboxing layer, and confirm the open‑source license aligns with corporate policy.  
4. **Pilot Deployment** – Deploy the platform in a staging Kubernetes namespace, connect it to production‑grade PostgreSQL, and onboard a single business unit to build a real‑world multi‑agent workflow.  
5. **Scale‑Out** – Enable multi‑tenant RBAC, add additional MCP nodes, and integrate with existing CI/CD pipelines for automated agent versioning and monitoring.

**Production Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑06‑27), 89 stars, 16 forks, and active issue handling indicate a healthy open‑source project.  
- **Infrastructure Maturity** – Docker‑first packaging, PostgreSQL persistence, and documented admin UI provide all the components needed for a production environment.  
- **Governance Features** – Built‑in RBAC, sandboxed tool execution, and audit logs address typical enterprise compliance requirements.  
- **Remaining Checks** – Final due‑diligence should verify the license compatibility, conduct a thorough security assessment of the sandbox, and confirm long‑term maintainer commitment, but overall the platform is sufficiently robust for a serious pilot and subsequent production rollout.

### Русский

OpsisnTech Platform — это готовая к продакшн open‑source платформа для создания и управления AI‑агентами, построенная на LangGraph и обеспечивающая многопользовательскую изоляцию, ролевой контроль доступа, безопасный запуск инструментов и удобный админ‑интерфейс для управления моделями, MCP‑серверами, навыками и инструментами. Она позволяет превратить разрозненные подсказки и утилиты в повторяемые, масштабируемые рабочие процессы — например, координацию нескольких агентов, построение конвейеров с использованием внешних инструментов и стандартизацию памяти агентов. Проект имеет высокий уровень готовности к продакшн: активные коммиты, Docker‑контейнеры, поддержка PostgreSQL, 89 звёзд на GitHub и недавнее обновление, что делает его надёжным кандидатом для пилотного внедрения после небольшого PoC и проверки README.

### 中文

**价值**  
OpsinTech Platform 将零散的 Prompt 与工具封装成可重复、可治理的智能体工作流，提供多租户、角色权限、工具沙箱等企业级特性，帮助企业快速搭建、管理和监控多代理协作、工具调用和记忆管理等 AI 应用，显著提升研发效率和运营安全。

**典型接入方式**  
1. **Docker 部署**：使用官方提供的 `docker-compose.yml` 一键启动平台、PostgreSQL 数据库和 MCP 服务器。  
2. **模型/技能注册**：通过内置的 Admin UI（或 REST API）添加自有大模型、LLM 接口、Skill（业务逻辑）和 Tool（外部系统）插件。  
3. **权限配置**：在 UI 中创建租户、角色并分配 RBAC 策略，确保不同团队只能访问各自的模型和工具。  
4. **工作流编排**：使用 LangGraph DSL 或 Python SDK 编写多代理工作流，将工具调用、记忆存储等步骤串联起来，提交到平台即能运行。  

**生产可用性**  
- **成熟度**：近期仍在活跃维护（2026‑06‑27），拥有 89 ★、16 Fork，社区活跃度良好。  
- **部署友好**：完整的 Docker 镜像、PostgreSQL 持久化、可配置的环境变量，适合在 Kubernetes 或传统 VM 上直接上线。  
- **治理能力**：多租户、基于角色的访问控制、工具沙箱执行、审计日志和模型/Skill 版本管理，满足企业合规与安全要求。  
- **风险**：需进一步确认许可证兼容性、代码安全审计以及维护者响应时效后方可正式投入关键业务。  

总体而言，OpsinTech/opsintech-platform 已具备高可用的生产级特性，适合作为企业内部 AI Agent 编排的核心平台，先在小范围 PoC 验证后即可逐步推广至全局使用。

## 🧭 Practical evaluation

**Value:** OpsinTech/opsintech-platform helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 89 GitHub stars
- 16 forks
- updated 2026-06-27
- primary language: Python

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 42/100 |
| topics | 0/100 |
| outlook | 52/100 |
| quality | 42/100 |
| recency | 40/100 |
| adoption | 39/100 |
| production | 55/100 |
| usefulness | 90/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/OpsinTech/opsintech-platform) · [← Back to Orchestration](./README.md)</sub>
