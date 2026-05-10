# SAP/ai-sdk-js

[![Stars](https://img.shields.io/github/stars/SAP/ai-sdk-js?style=flat-square&color=yellow)](https://github.com/SAP/ai-sdk-js/stargazers) [![Forks](https://img.shields.io/github/forks/SAP/ai-sdk-js?style=flat-square&color=blue)](https://github.com/SAP/ai-sdk-js/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> SAP Cloud SDK for AI is the official Software Development Kit (SDK) for SAP AI Core, SAP Generative AI Hub, and Orchestration Service.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 110 |
| 🍴 **Forks** | 46 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-05-10 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `gen-ai` `javascript` `llm` `orchestration` `sap-ai-core` `sap-generative-ai-hub` `typescipt`

## 🎯 Categories

Orchestration · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
SAP / ai‑sdk‑js is the official TypeScript SDK for SAP AI Core, the Generative AI Hub, and the Orchestration Service. It lets developers stitch together isolated prompts, tools, and memory stores into repeatable, multi‑agent workflows, making it easy to build coordinated AI pipelines. With active maintenance, strong community signals, and a clean API/CLI surface, it is ready for pilot‑grade production use.

**Value**  
- **Workflow orchestration:** Turns ad‑hoc prompts into reusable agents that can call other agents, external tools, or data sources, enabling complex decision‑making pipelines.  
- **Standardised memory & tool integration:** Provides built‑in patterns for persisting context and invoking utilities (e.g., search, retrieval, or custom services), reducing boiler‑plate and ensuring consistency across projects.  
- **Vendor‑aligned ecosystem:** Directly targets SAP’s AI stack, so teams already invested in SAP Cloud Platform can leverage native authentication, telemetry, and governance without custom glue code.

**Practical Adoption Path**  
1. **Prototype:** Install the npm package, configure the SAP AI Core credentials, and use the provided CLI to generate a starter agent project.  
2. **Iterate:** Replace isolated prompts with SDK‑wrapped agents, add tool‑use definitions (e.g., retrieval‑augmented generation) and enable memory persistence via the SDK’s helper classes.  
3. **Integrate:** Hook the generated workflow into existing SAP services (e.g., S/4HANA, SuccessFactors) using the SDK’s TypeScript client or expose it as a micro‑service via the provided CLI.  
4. **Validate & Scale:** Run automated tests against the SDK’s mock adapters, then promote the workflow to a containerised or serverless runtime in SAP Business Technology Platform (BTP) for production.

**Production Readiness**  
- **Activity & Adoption:** 110 GitHub stars, 46 forks, recent commits (as of 2026‑05‑10) and a growing ecosystem of examples indicate healthy community interest.  
- **Maturity:** The SDK offers a stable API surface, comprehensive TypeScript typings, and a CLI for deployment, which lowers integration risk.  
- **Risk Considerations:** License compliance, security posture, and maintainer responsiveness still need a final audit, but no major red flags have been identified. Overall, the project is mature enough for a serious pilot and can be promoted to production once the final compliance checks are completed.

### Русский

SAP/ai-sdk-js — это официальный JavaScript‑SDK для SAP AI Core, Generative AI Hub и Orchestration Service, позволяющий превратить разрозненные подсказки и инструменты в повторяемые агентные рабочие процессы, включая координацию нескольких агентов, построение конвейеров с использованием внешних инструментов и стандартизацию памяти агентов. Проект активно поддерживается (обновления 2026‑05‑10, 110 звёзд, 46 форков, TypeScript), имеет чётко описанные API/CLI и готов к использованию в пилотных и production‑сценариях при условии окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
SAP/ai-sdk-js 是 SAP 官方发布的 JavaScript/TypeScript SDK，统一封装了 SAP AI Core、Generative AI Hub 与 Orchestration Service 的接口，帮助开发者把零散的 Prompt 与工具组装成可复用的智能体工作流。

**价值**  
- 将分散的 Prompt、工具和记忆机制标准化，快速构建多代理协同、工具调用与记忆管理的 AI 工作流。  
- 提供统一的 API/SDK/CLI，降低跨 SAP AI 产品的集成成本，加速业务场景原型到生产的转化。  

**典型接入方式**  
1. **安装 SDK**：`npm install @sap/ai-sdk`（或使用 Yarn、pnpm）。  
2. **配置凭证**：在代码或 CI 环境中提供 SAP AI Core 的访问令牌或服务账号。  
3. **创建客户端**：使用 SDK 提供的 `AiClient`、`Orchestrator` 等类实例化对应服务。  
4. **编排工作流**：通过 SDK 调用 `createAgent`, `addTool`, `setMemory` 等方法，定义多代理的执行顺序和工具链。  
5. **运行与监控**：利用 SDK 的日志、追踪和错误处理接口，结合 SAP Observability 进行生产监控。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑10，项目最近一次提交，星标 110、fork 46，持续维护。  
- **技术成熟度**：基于 TypeScript，提供完整类型定义，易于在现代前端/后端项目中集成。  
- **生态兼容**：兼容 Node.js、浏览器以及 SAP Cloud 环境，可通过 CLI 与 CI/CD 流程无缝对接。  
- **风险**：需进一步审查许可证（默认 Apache‑2.0）和安全依赖，但整体安全姿态良好，已具备在生产环境进行正式试点的条件。

## 🧭 Practical evaluation

**Value:** SAP/ai-sdk-js helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 110 GitHub stars
- 46 forks
- updated 2026-05-10
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 74/100 |
| recency | 100/100 |
| adoption | 43/100 |
| production | 77/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-10 · [View on GitHub](https://github.com/SAP/ai-sdk-js) · [← Back to Orchestration](./README.md)</sub>
