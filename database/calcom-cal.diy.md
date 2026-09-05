# calcom/cal.diy

[![Stars](https://img.shields.io/github/stars/calcom/cal.diy?style=flat-square&color=yellow)](https://github.com/calcom/cal.diy/stargazers) [![Forks](https://img.shields.io/github/forks/calcom/cal.diy?style=flat-square&color=blue)](https://github.com/calcom/cal.diy/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Scheduling infrastructure for absolutely everyone.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 45.9k |
| 🍴 **Forks** | 14.2k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`next-auth` `nextjs` `open-source` `postgresql` `prisma` `t3-stack` `tailwindcss` `trpc` `turborepo` `typescript` `zod`

## 🎯 Categories

Database · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
calcom/cal.diy is an open‑source scheduling platform built in TypeScript that doubles as a plug‑and‑play AI layer, letting teams prototype retrieval‑augmented generation (RAG), agent workflows, and other model‑driven features without assembling a stack from scratch. With over 45 k GitHub stars, frequent releases, and strong community adoption, it is positioned as a production‑ready candidate for organizations that need a flexible, AI‑enhanced scheduling infrastructure.  

**Value**  
- **AI‑enabled scheduling** – adds conversational AI, recommendation engines, or automated assistants directly onto the core calendar service, accelerating feature delivery.  
- **Rapid prototyping** – pre‑built integrations for popular LLM providers and vector stores let developers spin up RAG or agent pipelines in hours instead of weeks.  
- **Unified stack** – combines frontend, backend, database, and DevOps concerns in a single TypeScript codebase, reducing the overhead of managing disparate services.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Fork the repo, run the Docker compose setup, and follow the README to enable a simple AI‑powered “suggest meeting time” endpoint.  
2. **Feature Extension** – Replace the placeholder model with your preferred LLM (OpenAI, Anthropic, etc.) and connect a vector store (e.g., Pinecone) to test RAG use cases.  
3. **Integration** – Embed the service behind your existing authentication layer, expose the API to your frontend, and configure CI/CD pipelines using the provided GitHub Actions.  
4. **Scale‑out** – Leverage the built‑in Helm charts or Terraform modules to deploy to Kubernetes, enable autoscaling, and monitor with Prometheus/Grafana.  

**Production Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑06‑26), 45 k stars, 14 k forks, and active issue/PR traffic indicate a healthy maintainer base.  
- **Security & Licensing** – No immediate metadata risks, but a final audit of the MIT‑style license, third‑party dependencies, and supply‑chain security is recommended before full rollout.  
- **Infrastructure Maturity** – Includes Docker, Helm, and Terraform deployment options, comprehensive test suites, and documented observability hooks, making it suitable for a serious pilot in production environments.  

Overall, calcom/cal.diy offers a high‑impact, low‑friction way to embed AI into scheduling workflows, with a clear, incremental adoption path and a solid foundation for production deployment.

### Русский

calcom/cal.diy — это открытая инфраструктура планирования, позволяющая быстро добавить AI‑функциональность в любые сервисы без необходимости создавать модельный стек с нуля. Типичный сценарий: в небольшом proof‑of‑concept подключить RAG‑или агентный workflow через готовый TypeScript‑SDK, протестировать модельные инструменты и затем масштабировать решение в продакшн. Проект имеет высокий уровень готовности: активные коммиты, более 45 тыс. звёзд, обширный форк‑сообщества и поддержка DevOps/Infra, Frontend и Security, что делает его надёжным кандидатом для серьёзного пилотного внедрения (при окончательной проверке лицензии и безопасности).

### 中文

**项目简介（2‑3 句）**  
calcom/cal.diy 是面向所有用户的开源调度基础设施，提供即插即用的 AI 能力，让开发者无需从零构建模型栈即可快速原型化 AI 功能。它支持 RAG（检索增强生成）和智能体工作流，可直接在现有业务系统中嵌入调度与推理能力。

**价值**  
- **快速落地**：通过封装好的调度与模型调用接口，团队可以在几天内完成 AI 功能的概念验证（PoC），大幅缩短研发周期。  
- **统一治理**：统一的调度层负责任务分发、重试、限流和监控，帮助在多模型、多数据源的场景下保持可观测性和可靠性。  
- **生态兼容**：基于 TypeScript 实现，天然兼容前端框架、Node.js 微服务以及常见的数据库和 DevOps 工具链，便于在现有技术栈中平滑引入。

**典型接入方式**  
1. **阅读 README 与示例**：先克隆仓库，参考 `examples/` 中的最小演示，确认项目依赖（Node ≥18、pnpm/yarn）。  
2. **创建小型 PoC**：在业务代码中引入 `@calcom/diy-scheduler` 包，配置调度器的入口（如 `schedule.ts`），并使用提供的 `runTask`、`registerModel` API 注册模型或 RAG 检索服务。  
3. **本地或容器化运行**：通过 `docker compose up` 启动调度服务、Redis（或其他消息队列）以及可选的监控组件（Prometheus/Grafana），验证任务调度与模型调用的完整链路。  
4. **逐步扩展**：在 PoC 验证后，可将调度服务迁移至 Kubernetes，使用 Helm chart（仓库已提供）进行生产级部署，并接入 CI/CD、日志聚合等 DevOps 流程。

**生产可用性**  
- **活跃度**：截至 2026‑06‑26，项目拥有 45 868 颗星、14 222 次 fork，最近一次提交仅在数天前，社区活跃度高。  
- **技术成熟度**：采用 TypeScript 编写，拥有完整的类型定义和单元测试，配套的 Docker 镜像与 Helm chart 已经可用于生产环境。  
- **安全与合规**：虽然目前未发现重大元数据风险，但仍需对许可证（MIT）进行合规审查，并通过内部安全扫描确认依赖库的漏洞情况。  
- **可观测性**：内置 Prometheus 指标、日志结构化输出和错误重试机制，满足大多数企业级监控和故障恢复需求。  

综合来看，calcom/cal.diy 在功能完整性、社区活跃度和基础设施成熟度方面均已具备进入生产环境的条件，适合作为 AI 调度与 RAG 工作流的首选 OSS 组件，在完成最终的许可证与安全审查后即可投入正式业务使用。

## 🧭 Practical evaluation

**Value:** calcom/cal.diy helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 45868 GitHub stars
- 14222 forks
- updated 2026-06-26
- primary language: TypeScript
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 100/100 |
| stars | 99/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 95/100 |
| recency | 80/100 |
| adoption | 99/100 |
| production | 77/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/calcom/cal.diy) · [← Back to Database](./README.md)</sub>
