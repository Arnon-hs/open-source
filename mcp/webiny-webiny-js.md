# webiny/webiny-js

[![Stars](https://img.shields.io/github/stars/webiny/webiny-js?style=flat-square&color=yellow)](https://github.com/webiny/webiny-js/stargazers) [![Forks](https://img.shields.io/github/forks/webiny/webiny-js?style=flat-square&color=blue)](https://github.com/webiny/webiny-js/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-89%2F100-brightgreen?style=flat-square)](#)

> Open-source, self-hosted CMS platform on AWS serverless (Lambda, DynamoDB, S3). TypeScript framework with multi-tenancy, lifecycle hooks, GraphQL API, and AI-assisted development via MCP server. Built for developers at large organizations.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 8k |
| 🍴 **Forks** | 672 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 89/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-assisted-development` `aws` `aws-lambda` `cms` `graphql` `headless-cms` `lambda` `lambda-functions` `mcp` `multi-tenant` `nextjs` `nodejs`

## 🎯 Categories

MCP · AI/ML · Frontend · Backend · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Webiny JS is an open‑source, serverless CMS built on AWS (Lambda, DynamoDB, S3) that provides a TypeScript framework with multi‑tenancy, lifecycle hooks, a GraphQL API, and an AI‑assisted development layer (MCP server). It targets large‑scale development teams that need a highly extensible, self‑hosted platform for building content‑driven applications and for plugging AI agents into real‑world tools and data.  

**Value Proposition**  
- **Standardised AI‑tool integration** – Webiny’s MCP server implements the Model‑Context‑Protocol, giving developers a ready‑made, language‑agnostic bridge for connecting large‑language‑model agents to internal services, databases, and third‑party APIs.  
- **Serverless, developer‑first stack** – By leveraging AWS Lambda, DynamoDB and S3, the platform eliminates infrastructure overhead while offering TypeScript‑typed SDKs, CLI tooling, and GraphQL endpoints that accelerate feature delivery.  
- **Enterprise‑grade extensibility** – Multi‑tenant architecture, lifecycle hooks, and a plugin system let organizations tailor the CMS to complex workflows, compliance needs, and custom business logic without forking the core codebase.  

**Practical Adoption Path**  

| Phase | Activities | Key Deliverables |
|-------|------------|------------------|
| **Evaluation** | Spin up the official Docker/Serverless template in a sandbox AWS account; run the CLI `webiny create` wizard; explore the GraphQL Playground and MCP demo endpoint. | Proof‑of‑concept API that can ingest and retrieve content; basic AI‑agent call through MCP. |
| **Pilot Integration** | Add a custom plugin (e.g., a lifecycle hook that triggers an external microservice) and configure a tenant for a specific business unit. Use the TypeScript SDK to fetch data from the GraphQL API in an existing frontend. | Integrated CI/CD pipeline, documented plugin, tenant‑specific configuration, and a working AI‑assistant use case (e.g., “fetch latest marketing copy”). |
| **Production Roll‑out** | Harden security (IAM roles, VPC‑linked Lambdas, DynamoDB encryption), enable monitoring (CloudWatch, X‑Ray), and set up automated backups for S3/DynamoDB. Deploy via Infrastructure‑as‑Code (CDK or Terraform) and establish multi‑region failover if needed. | Production‑grade environment with SLA‑aligned observability, RBAC, and disaster‑recovery. |
| **Scale & Extend** | Add more tenants, integrate additional AI models via the MCP server, and publish reusable plugins to the internal marketplace. | Enterprise‑wide adoption, standardized AI‑tool protocol across teams, and a growing ecosystem of internal extensions. |

**Production Readiness**  
- **Activity & Community** – 7,974 ⭐ on GitHub, 672 🍴, recent commits (as of 2026‑05‑13) and a vibrant ecosystem of 18 topics indicate strong momentum.  
- **Stability** – The serverless core (Lambda/DynamoDB/S3) is a proven AWS stack; Webiny’s own CI/CD pipelines and automated tests are in place, giving confidence for high‑availability deployments.  
- **Extensibility & Observability** – Built‑in GraphQL schema introspection, TypeScript typings, and lifecycle hooks simplify debugging and monitoring; the MCP server adds a formal contract for AI‑agent interactions, reducing integration risk.  
- **Risks to Verify** – Final due‑diligence should confirm the OSS license compatibility, review the security posture of the MCP server (e.g., authentication, rate‑limiting), and ensure that the current maintainer team is actively responding to issues.  

Overall, Webiny JS scores 89/100 and is ready for a serious pilot in production environments, especially where organizations want a serverless CMS that doubles as a standard gateway for AI‑driven tooling.

### Русский

**Webiny (webiny/webiny-js)** — это открытая сервер‑лес CMS на AWS (Lambda, DynamoDB, S3), написанная на TypeScript и поддерживающая мульти‑тенантность, хуки жизненного цикла, GraphQL‑API и AI‑ассистент разработки через MCP‑сервер. Проект позволяет быстро подключать AI‑агентов к реальным инструментам и данным, стандартизировать интеграции и развертывать Model Context Protocol серверы, что делает его идеальным решением для крупных организаций, желающих построить собственную AI‑поддерживаемую инфраструктуру. С высокой готовностью к production (активные коммиты, 7 974 звёзд, 672 форка, обширный набор тем и SDK/CLI), Webiny готов к пилотному внедрению в корпоративных проектах.

### 中文

**项目简介**  
webiny/webiny-js 是一套基于 AWS Serverless（Lambda、DynamoDB、S3）的开源自托管 CMS，使用 TypeScript 构建，提供多租户、生命周期钩子、GraphQL API 与 AI 辅助开发（MCP 服务器）等能力，专为大型组织的开发者设计。

**价值主张**  
- **标准化 AI‑to‑Tool 接口**：通过统一的 Model Context Protocol（MCP）让 AI 助手能够安全、可靠地调用真实业务工具和数据。  
- **全栈即插即用**：前端（React/Vue）与后端（GraphQL、Lambda）均可通过同一 SDK/CLI 访问，降低集成成本。  
- **企业级可扩展性**：多租户、细粒度生命周期钩子以及无服务器弹性伸缩，满足大流量、复杂权限的生产需求。  

**典型接入方式**  
1. **使用 CLI 安装并部署**：`npx create-webiny-project` 自动生成完整的 Serverless 堆栈（Lambda、DynamoDB、S3）。  
2. **通过 SDK/GraphQL API 调用**：前端使用 `@webiny/app` 或自定义 SDK，后端通过 GraphQL 端点执行 CRUD、生命周期钩子等操作。  
3. **接入 MCP 服务器**：在项目根目录配置 `mcp.yml`，启动 MCP 服务后即可让 AI 代理通过标准协议调用已注册的业务工具（如内容发布、文件存储等）。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑13，拥有 7,974 星、672 Fork，最近一次提交在当日，社区和维护者活跃。  
- **成熟生态**：18 个 GitHub Topics 覆盖前端、后端、DevTools、AI/ML 等，已有多家大型企业在生产环境中使用。  
- **安全与合规**：基于 AWS 原生服务，天然具备 IAM、VPC、加密等安全机制；仍需自行审查许可证（MIT）及第三方依赖的安全报告。  

综合来看，webiny/webiny-js 在功能完整性、社区活跃度和 AWS Serverless 的可靠性方面均表现出色，适合作为 AI 助手与业务系统集成的生产级平台。

## 🧭 Practical evaluation

**Value:** webiny/webiny-js helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 7974 GitHub stars
- 672 forks
- updated 2026-05-13
- primary language: TypeScript
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 71/100 |
| stars | 83/100 |
| topics | 100/100 |
| outlook | 95/100 |
| quality | 91/100 |
| recency | 100/100 |
| adoption | 80/100 |
| production | 85/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/webiny/webiny-js) · [← Back to Mcp](./README.md)</sub>
