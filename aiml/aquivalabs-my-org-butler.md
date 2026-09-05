# aquivalabs/my-org-butler

[![Stars](https://img.shields.io/github/stars/aquivalabs/my-org-butler?style=flat-square&color=yellow)](https://github.com/aquivalabs/my-org-butler/stargazers) [![Forks](https://img.shields.io/github/forks/aquivalabs/my-org-butler?style=flat-square&color=blue)](https://github.com/aquivalabs/my-org-butler/network) [![Language](https://img.shields.io/badge/lang-Apex-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> AI Agent for the Salesforce Utility Bar. Performs tasks for the user & answers questions about the org. Uses the trusted Salesforce Agentforce under the hood.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 82 |
| 🍴 **Forks** | 16 |
| 💻 **Language** | Apex |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentforce` `agentic-ai` `salesforce`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary**  
Aquivalabs’ *my‑org‑butler* is an AI‑powered Salesforce Utility Bar agent that can execute routine tasks and answer org‑specific questions by leveraging the trusted Salesforce Agentforce framework. It lets teams prototype AI‑enhanced features, build Retrieval‑Augmented Generation (RAG) or agent‑driven workflows, and evaluate model tooling without having to assemble a full model stack from scratch.

**Value**  
- **Fast AI enablement** – The Butler bundles pre‑built prompts, retrieval logic, and Agentforce integration, so developers can add conversational or task‑automation capabilities to a Salesforce org with minimal model‑training effort.  
- **Low‑cost experimentation** – Because the core logic lives in Apex and the heavy lifting is offloaded to Agentforce, teams can quickly spin up prototypes, test RAG pipelines, or explore agent‑based automation before committing to a larger AI investment.  
- **Leverages existing Salesforce security** – Agentforce runs within the Salesforce trusted execution environment, preserving data residency and compliance requirements that are often a barrier to external AI services.

**Practical Adoption Path**  
1. **Discovery & Planning** – Clone the repo, review the Apex classes and Utility Bar configuration, and map the provided intents to your org’s business processes.  
2. **Sandbox Validation** – Deploy the package to a sandbox, enable the Utility Bar component, and run the built‑in test suite. Because integration signals are sparse, manually verify that the Butler can access the required objects, fields, and external services (e.g., Agentforce credentials).  
3. **Iterative Customisation** – Extend the prompt library or add new Apex handlers for org‑specific tasks, then test end‑to‑end flows in the sandbox.  
4. **Pilot Roll‑out** – Promote the customised version to a limited set of internal users (e.g., admin or support team) and collect feedback on accuracy, latency, and UI experience.  
5. **Production Hardening** – Conduct a formal security review, configure monitoring (API usage, error rates), and set up a CI/CD pipeline for Apex changes before moving to production.

**Production Readiness**  
The project sits at a **medium** readiness level: it is stable enough for internal prototypes and limited‑scope workflows, but it requires careful validation of integration points (metadata, Agentforce credentials, and any external APIs) before a full production launch. The recent update (2026‑05‑12), solid GitHub star count (82) and active fork community indicate healthy maintenance, yet teams should perform dependency checks, establish robust monitoring, and allocate resources for ongoing Apex maintenance to ensure long‑term reliability.

### Русский

**aquivalabs/my-org-butler** — AI‑агент, интегрированный в Utility Bar Salesforce, который автоматически выполняет задачи и отвечает на вопросы о вашей организации, используя проверенный движок Agentforce. Он позволяет быстро прототипировать AI‑функции, построить RAG‑ или агентные рабочие процессы и оценить инструменты моделей без необходимости создавать стек с нуля; однако перед внедрением требуется ручная проверка интеграции, так как метаданные дают ограниченные сигналы. Проект находится на среднем уровне готовности – подходит для прототипов и внутренних workflow, но требует дополнительного аудита зависимостей и поддержки перед переходом в продакшн.

### 中文

**项目简介**  
aquivalabs / my‑org‑butler 是一款基于 Salesforce 官方 Agentforce 的 AI Agent，嵌入在 Utility Bar 中，能够帮助用户执行日常操作并实时回答组织（Org）相关的问题。它让开发者无需从零搭建模型堆栈，即可在 Salesforce 中快速原型化 AI 功能、构建 RAG（检索增强生成）或多步骤 Agent 工作流。

**价值体现**  
- **快速赋能**：只需少量配置，即可在现有 Org 中加入对话式 AI，省去模型训练、部署的时间成本。  
- **低门槛实验**：适合内部原型、概念验证或评估不同模型工具链的效果。  
- **可扩展**：基于 Agentforce，后期可平滑迁移到更复杂的业务流程或生产级别的自动化。

**典型接入方式**  
1. **在 Salesforce Setup 中启用 Agentforce**（确保已购买或获取相应许可）。  
2. **部署 my‑org‑butler 的 Apex 包**，该包会在 Utility Bar 中自动注册一个自定义组件。  
3. **手动检查并映射元数据**：因为项目的元数据发现信号较少，推荐在 Sandbox 或 Scratch Org 中运行 `sfdx force:source:push` 后，使用 `Setup → Utility Bar` 确认组件位置，并根据业务需求在 Apex/Lightning 中添加自定义触发器或 API 调用。  
4. **配置 Prompt / Retrieval 参数**（可在自定义设置或自定义元数据类型中完成），完成后即可在 Utility Bar 中与 Butler 对话。

**生产可用性**  
- **成熟度**：Medium。项目已获得 82 星、16 Fork，最近更新于 2026‑05‑12，适合作为原型或内部工作流的 AI 能力。  
- **上线前检查**：  
  - 验证 Agentforce 许可证与配额是否满足预期调用量。  
  - 评估自定义 Apex 代码的治理、测试覆盖率以及与现有触发器的兼容性。  
  - 在预生产环境完成端到端的功能和性能测试，确认集成路径（尤其是元数据映射）无遗漏。  
- **后期维护**：需要定期跟进 Apex 包的更新以及 Salesforce 平台的安全补丁，确保依赖的 Agentforce API 版本保持兼容。  

综上，aquivalabs/my-org-butler 为希望在 Salesforce 中快速实验 AI 功能的团队提供了即插即用的解决方案，但在正式生产环境部署前，务必进行手动元数据审查和完整的集成测试。

## 🧭 Practical evaluation

**Value:** aquivalabs/my-org-butler helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 82 GitHub stars
- 16 forks
- updated 2026-05-12
- primary language: Apex
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 41/100 |
| topics | 38/100 |
| outlook | 63/100 |
| quality | 58/100 |
| recency | 80/100 |
| adoption | 38/100 |
| production | 61/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/aquivalabs/my-org-butler) · [← Back to AI/ML](./README.md)</sub>
