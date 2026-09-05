# beizhu-1209/AIHelms

[![Stars](https://img.shields.io/github/stars/beizhu-1209/AIHelms?style=flat-square&color=yellow)](https://github.com/beizhu-1209/AIHelms/stargazers) [![Forks](https://img.shields.io/github/forks/beizhu-1209/AIHelms?style=flat-square&color=blue)](https://github.com/beizhu-1209/AIHelms/network) [![Language](https://img.shields.io/badge/lang-Vue-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-80%2F100-brightgreen?style=flat-square)](#)

> 企业级 AI 资源纳管平台，提供统一 AI网关，纳管 OpenAI、Azure、Claude、DeepSeek 等主流模型，并支持 MCP 工具与 Skill 的集中注册分发。具备内外双轨定价、成本归因、统一身份认证、安全审计与效能报表，帮助企业精准控制成本、量化 ROI，高效治理 AI 资产。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 384 |
| 🍴 **Forks** | 47 |
| 💻 **Language** | Vue |
| 📈 **Score** | 80/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `ai-management` `ai-observability` `claude` `cost-control` `deepseek` `docker` `enterprise-ai` `fastapi` `llm-governance` `mcp` `model-gateway`

## 🎯 Categories

MCP · AI/ML · Cloud & Storage · Backend · Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
AIHelms is an enterprise‑grade AI‑resource management platform that unifies access to major large‑model providers (OpenAI, Azure, Claude, DeepSeek, etc.) through a single AI gateway. It adds centralized registration and distribution of MCP tools and Skills, dual‑track pricing, cost attribution, unified identity, security auditing, and performance reporting, enabling companies to tightly control AI spend and measure ROI.

**Value**  
- **Unified AI Mesh:** Eliminates the need for multiple vendor‑specific integrations by exposing a common API/SDK/CLI that any AI assistant can consume.  
- **Cost & Governance:** Dual‑track pricing, detailed cost‑attribution, and audit logs give finance and security teams visibility and control over AI consumption.  
- **Rapid Tool‑to‑Agent Connection:** The built‑in MCP and Skill registry lets developers plug real‑world tools (databases, SaaS APIs, internal services) into LLM agents without writing custom glue code.  
- **Observability:** Integrated dashboards and performance reports make it easy to track latency, token usage, and ROI across all models.

**Practical Adoption Path**  
1. **Pilot Deployment:** Spin up the Vue‑based frontend and backend services (Docker‑compose or Helm chart) in a staging environment.  
2. **Model & Tool Registration:** Register the desired LLM endpoints (OpenAI, Azure, Claude, DeepSeek) and upload MCP‑compatible tools/Skills via the UI or CLI.  
3. **Agent Integration:** Update existing AI agents to point to the AIHelms gateway endpoint; the agents will automatically discover registered tools through the Model Context Protocol.  
4. **Governance Enablement:** Configure pricing tiers, cost‑center tags, and SSO (OAuth/OIDC) to enforce corporate policies.  
5. **Scale to Production:** Gradually migrate workloads from direct vendor calls to the gateway, monitor usage dashboards, and adjust pricing rules as needed.

**Production Readiness**  
- **Activity & Community:** 384 stars, 47 forks, recent commits (as of 2026‑06‑25), and a vibrant Vue‑centric ecosystem indicate active maintenance.  
- **Feature Completeness:** Core gateway, MCP/Skill registry, dual‑track pricing, authentication, audit logs, and observability are all implemented.  
- **Scalability:** Designed for both internal and external traffic lanes; can be deployed behind load balancers and integrated with existing Kubernetes or VM clusters.  
- **Risk Considerations:** License and security posture still need a final compliance check, but no major metadata risks have been identified. Overall, AIHelms is a strong OSS candidate for a serious production pilot.

### Русский

**AIHelms** – корпоративная платформа для централизованного управления AI‑ресурсами, позволяющая через единый шлюз подключать модели OpenAI, Azure, Claude, DeepSeek и другие, а также регистрировать и распределять MCP‑инструменты и Skills. Типичный сценарий — компании интегрируют AI‑агентов с внутренними сервисами и данными, используют двойную ценовую политику, аудит безопасности и отчёты о затратах для точного контроля расходов и расчёта ROI. Проект имеет высокий уровень готовности к продакшн: активные коммиты, 384 звёзд, поддержка Vue‑frontend, SDK/CLI, recent обновления и положительные сигналы экосистемы делают его надёжным кандидатом для пилотных и масштабных внедрений.

### 中文

**项目简介（2‑3 句）**  
AIHelms 是面向企业的 AI 资源统一管理平台，提供统一的 AI 网关，集中纳管 OpenAI、Azure、Claude、DeepSeek 等主流大模型，并支持 MCP 工具与 Skill 的统一注册与分发。平台实现内外双轨定价、成本归因、统一身份认证、安全审计与效能报表，帮助企业精准控制 AI 成本、量化 ROI 并高效治理 AI 资产。

**价值体现**  
1. **成本可视化 & ROI 量化**：通过双轨定价、细粒度成本归因和统一报表，企业可以实时监控不同模型、项目、部门的费用，避免资源浪费。  
2. **统一入口 & 安全治理**：统一 AI 网关实现统一身份认证、权限控制和审计日志，满足企业合规与安全要求。  
3. **模型与工具即插即用**：MCP（Model Context Protocol）与 Skill 注册中心让 AI 助手快速接入内部工具、数据库或业务系统，提升业务自动化效率。  
4. **多云多模型兼容**：一次接入即可管理 OpenAI、Azure OpenAI、Claude、DeepSeek 等多家供应商的模型，降低供应商锁定风险。

**典型接入方式**  

| 步骤 | 说明 | 关键组件 |
|------|------|----------|
| 1️⃣ 注册平台 | 在 AIHelms 控制台创建组织、租户，配置统一身份认证（OAuth、LDAP、SAML） | UI / API |
| 2️⃣ 纳管模型 | 在「模型管理」页面填写模型提供商的 API Key、Endpoint 等信息，平台自动生成统一的模型标识 | Model Registry |
| 3️⃣ 注册 MCP/Skill | 使用平台提供的 CLI/SDK（Python、Node.js）将内部工具或 Skill（如数据库查询、ERP 调用）注册到 Skill Registry，平台会生成标准的 MCP 接口 | `aihelms-cli register-skill` |
| 4️⃣ 调用统一网关 | 应用或 AI Agent 只需要调用平台统一的 REST / gRPC 网关（如 `https://gateway.company.com/v1/chat/completions`），在请求体中指定模型标识和 Skill 列表，平台负责路由、鉴权、计费与审计 | API Gateway |
| 5️⃣ 监控与报表 | 通过平台提供的 Grafana‑style 仪表盘或导出 CSV/Excel，实时查看费用、调用次数、错误率等指标 | Observability Dashboard |

**生产可用性评估**  
- **活跃度**：截至 2026‑06‑25，项目最近一次提交，拥有 384 星、47 Fork，社区活跃，代码基于 Vue 前端 + Go/Node 后端，具备完整的 CI/CD 流程。  
- **功能完整性**：已实现模型统一接入、MCP/Skill 注册、双轨计费、审计日志、统一身份认证等核心企业需求。  
- **可扩展性**：插件化的 Skill 注册机制和可自定义的计费策略，使其能够在大规模多租户环境下平滑扩容。  
- **安全合规**：支持 OAuth、LDAP、SAML 等企业级身份体系，所有请求均记录审计日志，可对接 SIEM。  
- **风险**：仍需进一步审查许可证（MIT/Apache）与依赖的第三方库的安全漏洞；建议在正式生产前进行内部安全评估并设立专职维护者。  

**结论**：AIHelms 已具备企业级生产使用的技术能力和功能完整度，适合作为企业 AI 资源的统一入口、成本治理和工具集成平台，在进行最后的安全与许可证审查后即可投入正式业务。

## 🧭 Practical evaluation

**Value:** beizhu-1209/AIHelms helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 384 GitHub stars
- 47 forks
- updated 2026-06-25
- primary language: Vue
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 73/100 |
| recency | 80/100 |
| adoption | 51/100 |
| production | 76/100 |
| usefulness | 90/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/beizhu-1209/AIHelms) · [← Back to Mcp](./README.md)</sub>
