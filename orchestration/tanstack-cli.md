# TanStack/cli

[![Stars](https://img.shields.io/github/stars/TanStack/cli?style=flat-square&color=yellow)](https://github.com/TanStack/cli/stargazers) [![Forks](https://img.shields.io/github/forks/TanStack/cli?style=flat-square&color=blue)](https://github.com/TanStack/cli/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> The official TanStack CLI - Project Scaffolding, MCP Server, Agent Skills Installation, etc

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.3k |
| 🍴 **Forks** | 172 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Orchestration · MCP

## 📝 Summary

### English

**Summary**  
TanStack CLI is the official command‑line tool for the TanStack ecosystem, offering project scaffolding, an MCP server, and easy installation of agent‑skill packages. It enables developers to turn isolated prompts and utilities into repeatable, multi‑agent workflows, standardizing memory handling and tool‑use pipelines. With over 1,200 stars, active maintenance, and recent TypeScript updates, it is ready for serious pilot projects.

**Value**  
The CLI abstracts the boilerplate of building and orchestrating AI agents, letting teams focus on domain logic rather than wiring prompts, tools, and state management. By providing a unified scaffolding experience and a built‑in MCP server, it accelerates the creation of robust, multi‑agent pipelines that can be versioned, shared, and reproduced across environments.

**Practical Adoption Path**  
1. **Proof of Concept** – Clone the repo, run the built‑in scaffolding command, and follow the README to spin up a minimal MCP server and a sample agent skill.  
2. **Integration** – Replace the sample skill with your own prompt/tool wrappers, configure memory persistence, and test the workflow locally.  
3. **Pilot** – Deploy the MCP server to a staging environment, connect it to existing services (e.g., databases, APIs), and monitor logs and performance.  
4. **Scale** – Use the CLI’s project templates to generate additional agents, standardize configuration via the provided `.tanstackrc`, and incorporate CI/CD pipelines for automated releases.

**Production Readiness**  
The project shows high production readiness: recent commits (as of 2026‑05‑11), active issue handling, a sizable community (1.2 k stars, 172 forks), and a TypeScript codebase that aligns well with modern backend stacks. While the license and security posture still need a final audit, the overall health signals—steady maintenance, clear documentation, and growing adoption—make TanStack CLI a solid candidate for a production‑grade pilot.

### Русский

**TanStack/cli** – официальная CLI‑утилита TanStack, позволяющая превратить разрозненные подсказки и инструменты в повторяемые рабочие процессы агентов: от scaffold‑инга проектов и запуска MCP‑сервера до установки навыков и построения конвейеров с использованием инструментов. Типичный сценарий внедрения — небольшое proof‑of‑concept, в котором через CLI создаётся шаблон проекта, подключается набор агентных навыков и настраивается оркестрация многопользовательских (multi‑agent) задач; после проверки README и базовых тестов можно масштабировать решение в продакшн. Проект имеет высокий уровень готовности: активные коммиты (обновление 2026‑05‑11), 1251 звёзд, 172 форка, широкая поддержка TypeScript и положительные сигналы экосистемы, что делает его надёжным кандидатом для серьёзного пилотного внедрения.

### 中文

**项目简介（2‑3 句）**  
TanStack/cli 是 TanStack 官方推出的全栈 CLI 工具，提供项目脚手架、MCP（Multi‑Component Platform）服务器、Agent Skills 安装等功能。它能够把零散的 Prompt 与工具包装成可重复、可组合的智能体工作流，帮助开发者快速搭建多代理协同系统。

**价值**  
- **工作流标准化**：将孤立的 Prompt 与工具统一抽象为「Skill」，形成可复用的流水线，降低重复实现成本。  
- **多代理编排**：内置 MCP Server，支持多智能体之间的消息路由、状态共享和记忆持久化，适用于复杂的业务流程。  
- **开发者友好**：基于 TypeScript 的 CLI 与插件机制，让项目初始化、依赖管理、Skill 发布都可以一键完成，提升开发效率。

**典型接入方式**  
1. **小范围 PoC**：先在本地使用 `npx @tanstack/cli init` 创建一个示例项目，阅读 README 中的快速上手章节。  
2. **集成到现有系统**：在已有的 Node/TS 后端项目中添加 `@tanstack/cli` 依赖，使用 `tanstack mcp start` 启动 MCP Server；通过 REST/gRPC 与业务服务对接。  
3. **Skill 开发与注册**：在项目根目录下 `tanstack skill create <name>` 生成 Skill 模板，编写业务逻辑后 `tanstack skill publish` 将其注册到 MCP，其他智能体即可调用。  
4. **CI/CD 自动化**：将 CLI 命令写入构建脚本，实现代码提交即自动生成/更新工作流，保持环境一致性。

**生产可用性**  
- **活跃度**：截至 2026‑05‑11，项目最近一次提交，拥有 1251 星、172 Fork，社区活跃。  
- **技术成熟度**：使用 TypeScript 开发，提供完整类型定义，易于在企业代码库中集成。  
- **安全与合规**：暂无重大元数据风险，仍需对许可证（MIT）和依赖安全审计进行最终确认。  
- **推荐策略**：可以直接作为 OSS 候选进入生产环境，先在非关键业务做小规模试点（如内部工具或实验性服务），验证与现有监控、日志体系的兼容性后再全面推广。  

总体而言，TanStack/cli 已具备高可用的技术底座与社区支持，适合作为多智能体编排与工具化 Prompt 的核心平台进行生产部署。

## 🧭 Practical evaluation

**Value:** TanStack/cli helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1251 GitHub stars
- 172 forks
- updated 2026-05-11
- primary language: TypeScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 66/100 |
| topics | 0/100 |
| outlook | 51/100 |
| quality | 48/100 |
| recency | 20/100 |
| adoption | 63/100 |
| production | 50/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/TanStack/cli) · [← Back to Orchestration](./README.md)</sub>
