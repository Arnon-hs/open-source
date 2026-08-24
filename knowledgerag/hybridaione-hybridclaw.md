# HybridAIOne/hybridclaw

[![Stars](https://img.shields.io/github/stars/HybridAIOne/hybridclaw?style=flat-square&color=yellow)](https://github.com/HybridAIOne/hybridclaw/stargazers) [![Forks](https://img.shields.io/github/forks/HybridAIOne/hybridclaw?style=flat-square&color=blue)](https://github.com/HybridAIOne/hybridclaw/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Enterprise-ready self-hosted AI assistant runtime with sandboxed execution, secure credentials, approvals, and memory

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 118 |
| 🍴 **Forks** | 11 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-agents` `anthropic` `chatgpt` `claude-code` `clawdbot` `clawhub` `codex` `enterprise-ai` `gdpr` `hermes` `hermes-agent`

## 🎯 Categories

Knowledge/RAG · AI/ML

## 📝 Summary

### English

**Brief summary**  
HybridAIOne / hybridclaw is an open‑source, self‑hosted runtime that lets enterprises run AI assistants in a sandboxed environment with built‑in credential protection, approval workflows and persistent memory. It indexes internal knowledge bases and augments search, enabling assistants to ground their responses in up‑to‑date corporate documents.

**Value**  
- **Secure, controllable AI** – sandboxed execution and encrypted credential storage keep sensitive data inside the organization’s perimeter.  
- **Knowledge‑centric** – automatic indexing and RAG (retrieval‑augmented generation) turn static documents into searchable, answerable content, improving employee productivity and reducing time spent hunting information.  
- **Governance** – approval pipelines and audit logs give teams visibility and control over what the assistant can do and what data it can access.

**Practical adoption path**  
1. **Proof‑of‑concept** – clone the repo, follow the README to spin up the Docker‑compose stack, and connect a small knowledge source (e.g., a Markdown folder).  
2. **Pilot integration** – expose a limited API to a single internal tool or chat channel, configure credential providers and approval rules, and measure retrieval accuracy and latency.  
3. **Scale‑out** – add more data sources (Confluence, SharePoint, etc.), configure role‑based access, and integrate with existing CI/CD pipelines for automated updates and monitoring.

**Production readiness**  
The project scores a medium readiness level: it is actively maintained (last commit 2026‑06‑22), has modest community traction (118 ★, 11 forks) and is written in TypeScript, which eases integration with modern web stacks. Before production use, teams should verify the license, perform a security audit of the sandbox implementation, and establish dependency‑update policies, but the core functionality is solid enough for internal prototypes and controlled workflows.

### Русский

HybridAIOne / hybridclaw — это готовый к корпоративному использованию self‑hosted рантайм AI‑ассистента с изолированным выполнением кода, безопасным хранением учётных данных, механизмом одобрений и долговременной памятью; он позволяет делать внутренние базы знаний доступными для поиска и контекстного использования ассистентами, улучшая поиск по документам и «заземляя» ответы на реальные данные. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, следуя README, чтобы оценить интеграцию и проверить зависимости, а затем постепенно расширять покрытие знаний. Уровень готовности — средний: проект подходит для прототипов и внутренних рабочих процессов, но перед запуском в продакшн требуется проверка лицензии, безопасности и активного сопровождения.

### 中文

**价值**  
HybridAIOne/hybridclaw 为企业提供一套可自托管的 AI 助手运行时，具备沙箱化执行、凭证安全、审批流程和持久记忆等特性。它能够把内部知识库（文档、FAQ、数据库等）索引后供助手实时检索，使得企业内部的知识变得可搜索、可调用，从而提升员工自助查询效率、降低人工客服成本，并为业务流程自动化提供可靠的“知识即服务”层。

**典型接入方式**  

1. **准备环境**：在内部服务器或容器平台（Docker/K8s）上部署 hybridclaw，按照 README 完成凭证（API Key、数据库连接等）配置。  
2. **索引知识库**：使用提供的 CLI 或 API 将文档、Wiki、Confluence、SharePoint 等来源的内容导入并生成向量索引。  
3. **集成助手**：在业务系统或聊天机器人中调用 hybridclaw 的 REST/GraphQL 接口，发送用户查询，系统会在已索引的知识库中检索并返回带有来源引用的答案；如需人工审批或敏感操作，可通过内置的审批工作流进行拦截。  
4. **迭代验证**：先在小范围（如单个部门或少量文档）做 PoC，检查检索准确率、响应时延以及安全审计日志，确认后逐步扩大覆盖范围。

**生产可用性**  
- **成熟度**：GitHub 118 ★、11 Fork，最近一次提交在 2026‑06‑22，代码基于 TypeScript，社区活跃度中等。  
- **适用场景**：非常适合作为原型、内部工具或部门级别的知识助理；在完成依赖审计（容器镜像、第三方库）和安全评估（凭证管理、沙箱隔离）后，可用于生产环境的内部工作流。  
- **注意事项**：在正式投产前建议进行：  
  1. 许可证合规检查（项目采用的开源许可证）。  
  2. 安全审计，确保沙箱隔离和凭证存储符合企业合规要求。  
  3. 监控与日志治理，确保能够追踪审批、异常调用等关键事件。  

综上，HybridAIOne/hybridclaw 为企业内部知识检索提供了“一站式”解决方案，接入成本相对低，适合先做小范围验证，再逐步扩展到生产环境。

## 🧭 Practical evaluation

**Value:** HybridAIOne/hybridclaw helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 118 GitHub stars
- 11 forks
- updated 2026-06-22
- primary language: TypeScript
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 27/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 39/100 |
| production | 54/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/HybridAIOne/hybridclaw) · [← Back to Knowledgerag](./README.md)</sub>
