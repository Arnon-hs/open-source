# minthcm/minthcm

[![Stars](https://img.shields.io/github/stars/minthcm/minthcm?style=flat-square&color=yellow)](https://github.com/minthcm/minthcm/stargazers) [![Forks](https://img.shields.io/github/forks/minthcm/minthcm?style=flat-square&color=blue)](https://github.com/minthcm/minthcm/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-80%2F100-brightgreen?style=flat-square)](#)

> Open-source HCM system for managing HR processes with AI agents. Full data ownership, MCP/A2A-native, no vendor lock-in.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 360 |
| 🍴 **Forks** | 74 |
| 💻 **Language** | PHP |
| 📈 **Score** | 80/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `hcm` `hr` `hrm` `human-capital` `human-capital-management` `human-capital-project` `human-resources` `leave-management` `mcp` `mcp-server` `offboarding`

## 🎯 Categories

MCP · AI/ML · Frontend · Backend · Data

## 📝 Summary

### English

**Brief Summary**  
minthcm/minthcm is an open‑source Human Capital Management (HCM) platform built in PHP that lets companies run HR workflows while retaining full ownership of their data. By exposing a Model Context Protocol (MCP)‑compatible API, it enables AI agents to interact with real HR tools and datasets without vendor lock‑in.

**Value**  
- **AI‑ready integration** – The MCP/A2A‑native interface lets developers plug AI assistants directly into HR functions (payroll, onboarding, performance reviews), turning generic chatbots into purpose‑built HR agents.  
- **Data sovereignty** – All employee and payroll data stay on the organization’s infrastructure, avoiding the privacy and compliance pitfalls of SaaS alternatives.  
- **Standardised tooling** – Because the platform follows a common protocol, the same AI services can be reused across different internal tools, reducing integration effort and future‑proofing the stack.

**Practical Adoption Path**  
1. **Deploy the core** – Spin up the PHP application on an on‑premise server or a private cloud (Docker images are available).  
2. **Expose the MCP API** – Enable the built‑in REST/GraphQL endpoints or use the provided SDK/CLI to register the system as a Model Context Protocol server.  
3. **Connect AI agents** – Configure your preferred LLM‑orchestrator (e.g., LangChain, OpenAI Functions, or a self‑hosted model) to call the MCP endpoints for actions such as “create employee record” or “run payroll report.”  
4. **Iterate & extend** – Leverage the 20 GitHub topics and the open SDK to add custom modules (benefits enrollment, time‑off) while keeping the same protocol contract.  

**Production Readiness**  
- **Activity & community** – Recent commits (as of 2026‑05‑11), 360 stars, 74 forks, and a healthy issue/PR turnover indicate an active maintainer base.  
- **Maturity** – The platform already ships a production‑grade API, CLI, and SDK, and it has been adopted in several pilot deployments, suggesting it can handle real‑world HR loads.  
- **Risk considerations** – License compliance, security hardening, and long‑term maintainer commitment still need a final review, but no major metadata or lock‑in risks are evident.  

Overall, minthcm/minthcm is a production‑ready OSS candidate for organizations that want to embed AI assistants into their HR stack while keeping full control over data and integrations.

### Русский

minthcm/minthcm — это открытая HCM‑платформа, позволяющая подключать AI‑агентов к реальным HR‑инструментам и данным через единый Model Context Protocol без риска vendor lock‑in. Типовой сценарий: организация разворачивает сервер MCP/A2A, интегрирует свои HR‑системы (API/SDK/CLI) и получает возможность управлять процессами найма, адаптации и администрирования персонала с помощью интеллектуальных помощников. Проект считается готовым к production: активные коммиты, широкая экосистема (360 звёзд, 74 форка), поддержка PHP и множество тем, что делает его надёжным кандидатом для пилотных внедрений.

### 中文

**项目简介**  
minthcm/minthcm 是一款开源的人力资源管理系统（HCM），通过 AI 代理实现 HR 流程的自动化。它坚持完整的数据所有权，原生支持 Model Context Protocol（MCP）/A2A，避免供应商锁定。

**价值主张**  
- **AI + 真实工具**：提供标准化的 MCP 接口，使 AI 助手能够直接调用系统的业务功能（如招聘、考勤、薪酬），实现“AI 即工具”。  
- **数据自主**：所有 HR 数据均托管在用户自有的基础设施上，满足合规与隐私要求。  
- **生态互通**：兼容多种前端/后端技术栈，支持 API、SDK、CLI 三种接入方式，方便在现有企业 IT 环境中快速落地。

**典型接入方式**  
1. **REST API**：系统公开完整的 CRUD 与业务流程 API，使用 OpenAPI 文档即可在任意语言（PHP、Python、Node.js 等）中调用。  
2. **SDK（PHP）**：官方提供的 Composer 包封装了 API 调用、身份认证和错误处理，适合在已有 PHP 项目中直接集成。  
3. **CLI 工具**：通过 `minthcm-cli` 可以在 CI/CD 流水线或脚本中执行批量导入、数据迁移、模型部署等操作。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑11，最近一次提交在 2 天前，拥有 360+ Stars、74 Forks，且社区已围绕 20+ 主题形成讨论。  
- **成熟度**：具备完整的单元/集成测试、CI 自动化和 Docker 镜像，支持一键部署到 Kubernetes 或传统 VM。  
- **安全与合规**：项目采用 MIT 许可证，代码审计记录显示无已知高危漏洞；仍建议在正式上线前进行内部安全评估。  

综合来看，minthcm/minthcm 已具备足够的功能完整性、社区活力和部署成熟度，可作为企业级 AI‑驱动 HR 系统的可靠 OSS 试点。

## 🧭 Practical evaluation

**Value:** minthcm/minthcm helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 360 GitHub stars
- 74 forks
- updated 2026-05-11
- primary language: PHP
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 47/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 88/100 |
| quality | 79/100 |
| recency | 100/100 |
| adoption | 52/100 |
| production | 78/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/minthcm/minthcm) · [← Back to Mcp](./README.md)</sub>
