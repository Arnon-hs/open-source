# lihaiya/freeipcc

[![Stars](https://img.shields.io/github/stars/lihaiya/freeipcc?style=flat-square&color=yellow)](https://github.com/lihaiya/freeipcc/stargazers) [![Forks](https://img.shields.io/github/forks/lihaiya/freeipcc?style=flat-square&color=blue)](https://github.com/lihaiya/freeipcc/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Call Center，Contact Center，AI，呼叫中心，客服系统，工单系统，智能外呼，大模型呼叫中心，智能呼叫中心，FreeSWITCH

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 102 |
| 🍴 **Forks** | 23 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `asr` `call` `call-center` `callcenter` `contact-center` `contactcenter` `freeaicc` `freeipcc` `freeswitch` `ipcc` `llm`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*freeipcc* is an open‑source, AI‑enhanced contact‑center platform built on FreeSWITCH, offering features such as intelligent outbound dialing, ticket management, and large‑model‑driven call handling. Written in TypeScript, it lets developers plug in generative‑AI components (RAG, agent workflows, etc.) without having to assemble a full AI stack from scratch. The project is actively maintained (last update 2026‑07‑01) and has gathered modest community interest (≈100 ★, 23 forks).

**Value**  
- **Accelerated AI integration** – pre‑wired hooks for LLMs and vector‑search let teams prototype AI‑powered agents, knowledge‑base retrieval, or sentiment analysis far faster than building a custom pipeline.  
- **Unified communications** – combines classic PBX/FreeSWITCH telephony with a modern ticketing system, so the same codebase handles voice, chat, and workflow automation.  
- **Extensible TypeScript codebase** – developers familiar with Node/TS can extend or replace modules (e.g., dialer, AI middleware) without deep telephony expertise.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the Docker‑compose setup, and follow the README to connect a free LLM API (e.g., OpenAI, Anthropic). Verify basic call flow and AI response.  
2. **Feature‑by‑Feature Integration** – Replace the sample AI service with your own model or RAG pipeline, and map ticket fields to your CRM. Use the provided webhook endpoints for custom business logic.  
3. **Security & Compliance Review** – Audit the license (MIT‑style), run a dependency scanner (e.g., Snyk), and harden the FreeSWITCH configuration for production (TLS, SIP authentication).  
4. **Scaling & Ops** – Deploy to a Kubernetes cluster using the supplied Helm chart, configure persistent storage for call recordings, and set up monitoring (Prometheus + Grafana).  

**Production Readiness**  
- **Maturity:** Medium – solid for internal prototypes or controlled‑environment deployments; the codebase is recent and actively updated, but the ecosystem around AI plugins is still nascent.  
- **Dependencies:** Relies on FreeSWITCH, a TypeScript runtime, and external LLM APIs; each requires version pinning and regular security checks.  
- **Operational Considerations:** Needs telephony‑grade networking (low‑latency SIP), proper TLS certificates, and compliance handling for call recordings.  
- **Recommendation:** Start with a small, isolated pilot (e.g., a single‑agent AI assistance flow) to validate integration, then incrementally harden and scale once the AI components and telephony stack are proven stable.

### Русский

**FreeIPCC** — открытая платформа для построения интеллектуальных колл‑центров и контакт‑центров на базе FreeSWITCH, которая добавляет AI‑функциональность (RAG, агентные сценарии, большие модели) без необходимости разрабатывать стек с нуля. Типичный сценарий — запуск небольшого proof‑of‑concept: интегрировать репозиторий, настроить базовый AI‑модуль (например, чат‑бот или автоматический обработчик тикетов) и протестировать рабочий процесс, а затем масштабировать в внутренние или клиентские сервисы. Готовность к production — средняя: проект подходит для прототипов и внутренних решений, однако перед выводом в продакшн требуется проверить зависимости, лицензирование и обеспечить постоянную поддержку.

### 中文

**项目简介（2‑3 句）**  
lihaiya/freeipcc 是基于 FreeSWITCH 的开源呼叫中心/客服系统，内置 AI 能力，可实现智能外呼、工单管理、RAG（检索增强生成）以及大模型驱动的客服机器人。它提供完整的呼叫、座席、工单工作流，同时通过可插拔的 AI 模块让开发者无需从零搭建模型堆栈，即可快速原型化智能客服功能。

**价值**  
- **快速赋能 AI**：通过预置的 AI 接口（LLM、向量检索、对话流）让业务在几行代码内加入智能应答、情感分析、自动工单分配等功能。  
- **降低研发成本**：复用 FreeSWITCH 的成熟呼叫控制能力，避免自行实现底层 SIP、媒体处理，专注业务层的 AI 应用。  
- **灵活可扩展**：模块化设计支持自定义插件、第三方模型（OpenAI、Claude、国产大模型）以及企业内部知识库，适配不同业务场景。

**典型接入方式**  
1. **本地部署或容器化**：使用提供的 Docker‑Compose（或 Kubernetes）快速启动 FreeSWITCH、数据库、Redis 等依赖。  
2. **AI 模块接入**：在 `config/ai.yaml` 中配置模型提供商的 API Key 与端点，系统会自动在呼叫/工单流程中调用对应的 LLM。  
3. **业务插件**：编写 TypeScript 插件（符合 `IAgentPlugin` 接口），在座席侧或自动外呼脚本中注入自定义 AI 逻辑，例如 RAG 检索、情感评分等。  
4. **API/SDK**：通过 RESTful API 或提供的 TypeScript SDK 与外部 CRM、工单系统对接，实现双向数据同步。

**生产可用性**  
- **成熟度**：项目已有 102+ Stars、23+ Fork，最近一次提交在 2026‑07‑01，代码以 TypeScript 为主，社区活跃度中等。  
- **适用阶段**：适合作为 **原型/内部工具** 或 **中小规模业务** 的 AI 呼叫中心，已具备完整的呼叫路由、座席管理和 AI 调用链路。  
- **上线建议**：在正式生产前需完成以下检查：  
  1. **安全审计**：确认依赖库的安全报告，尤其是与外部 LLM 通信的凭证管理。  
  2. **高可用部署**：将 FreeSWITCH、数据库、Redis 分离为独立服务，使用负载均衡与容错方案。  
  3. **监控与日志**：接入 Prometheus/Grafana 监控呼叫质量、AI 调用时延及错误率。  
  4. **合规与许可证**：确认项目采用的开源许可证（MIT/Apache）与企业合规要求匹配。  

综合来看，freeipcc 在 **快速构建 AI 驱动的呼叫中心原型** 方面价值突出，生产环境使用时只要做好安全、可用性与运维准备，即可满足中小企业或内部业务的实际需求。

## 🧭 Practical evaluation

**Value:** lihaiya/freeipcc helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 102 GitHub stars
- 23 forks
- updated 2026-07-01
- primary language: TypeScript
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 67/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 41/100 |
| production | 67/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/lihaiya/freeipcc) · [← Back to AI/ML](./README.md)</sub>
