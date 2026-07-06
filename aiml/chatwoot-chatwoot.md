# chatwoot/chatwoot

[![Stars](https://img.shields.io/github/stars/chatwoot/chatwoot?style=flat-square&color=yellow)](https://github.com/chatwoot/chatwoot/stargazers) [![Forks](https://img.shields.io/github/forks/chatwoot/chatwoot?style=flat-square&color=blue)](https://github.com/chatwoot/chatwoot/network) [![Language](https://img.shields.io/badge/lang-Ruby-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> Open-source live-chat, email support, omni-channel desk. An alternative to Intercom, Zendesk, Salesforce Service Cloud etc. 🔥💬

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 33.3k |
| 🍴 **Forks** | 7.8k |
| 💻 **Language** | Ruby |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-06-23 |
| 🔍 **Source** | github |

## 🏷️ Topics

`actioncable` `chat-widget` `conversation` `customer-support` `dashboard` `design` `docker` `docker-image` `heroku` `intercom` `javascript` `livechat`

## 🎯 Categories

AI/ML · Frontend · DevOps/Infra · Design

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Chatwoot is an open‑source omni‑channel customer‑support platform that provides live‑chat, email, and social‑media inboxes as a self‑hosted alternative to solutions like Intercom, Zendesk, or Salesforce Service Cloud. Its rich API/SDK/CLI surface makes it easy to plug in AI capabilities—such as retrieval‑augmented generation, automated agents, or custom model workflows—without building a stack from scratch. With a large, active community (33 k+ stars, 7 k+ forks) and frequent releases, it is production‑ready for pilots and full‑scale deployments.

**Value**  
- **Accelerated AI prototyping** – The built‑in messaging hooks let you attach LLM‑driven assistants, sentiment analysis, or ticket‑routing models directly to live‑chat flows, turning a standard support desk into an AI‑enhanced experience in days rather than months.  
- **Unified omni‑channel data** – All customer interactions are stored centrally, providing a single source of truth for training retrieval‑augmented generation (RAG) or recommendation models.  
- **Cost‑effective and extensible** – Being open source eliminates SaaS licensing fees while allowing full control over data, model choice, and deployment architecture.

**Practical Adoption Path**  
1. **Evaluation** – Spin up the official Docker compose or Helm chart in a staging environment; use the exposed REST API or Ruby SDK to send test messages.  
2. **AI Integration** – Develop a small microservice that consumes Chatwoot webhooks, calls your preferred LLM (e.g., OpenAI, Anthropic, or a self‑hosted model), and posts responses back via the API.  
3. **Pilot** – Enable the AI‑augmented inbox for a limited user segment, monitor key metrics (response time, resolution rate, CSAT), and iterate on prompt engineering or RAG pipelines.  
4. **Scale** – Deploy the AI service as a Kubernetes‑native component, configure role‑based access, and enable multi‑tenant inboxes for broader rollout.

**Production Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑06‑23), a vibrant contributor base, and extensive documentation indicate strong maintainership.  
- **Reliability** – Built on Ruby on Rails with a PostgreSQL backend; supports horizontal scaling via Docker/Kubernetes and offers built‑in webhooks, rate‑limiting, and SLA‑friendly logging.  
- **Security & Compliance** – Open‑source license (MIT) is permissive, but a final security audit is recommended to verify dependency hygiene and data‑privacy controls before handling sensitive customer data.  

Overall, Chatwoot offers a mature, extensible platform that can be quickly wired into AI workflows, making it a solid foundation for both experimental prototypes and production‑grade, AI‑powered support desks.

### Русский

**Chatwoot** — это открытая платформа для живого чата, поддержки по email и омниканального сервиса, позволяющая быстро добавить AI‑функциональность (RAG, агентные сценарии, прототипы) без построения модели с нуля. Типичный сценарий: интегрировать Chatwoot через его API/SDK, подключить нужный LLM и построить интеллектуальные ответы или автоматизацию запросов, получая готовый клиентский интерфейс и мощные аналитические инструменты. Проект обладает высокой готовностью к production: активные коммиты, более 33 тыс. звёзд, широкое сообщество и зрелая инфраструктура, что делает его надёжным выбором для пилотных и масштабных внедрений.

### 中文

**项目简介（2‑3 句）**  
Chatwoot 是一款开源的全渠道客服系统，提供实时聊天、邮件、社交媒体等多渠道支持，可直接替代 Intercom、Zendesk、Salesforce Service Cloud 等商业产品。它基于 Ruby 开发，社区活跃，拥有数万星标和数千叉。

**价值**  
- **快速赋能 AI**：内置 API/SDK，可在现有对话流中无缝接入大模型、检索增强生成（RAG）或自定义客服机器人，省去从零搭建模型栈的成本。  
- **原型与实验**：提供统一的信号层（API、CLI、语言元数据），适合快速原型化 AI 功能、评估不同模型工具链。  
- **降低运营成本**：开源免授权费，支持自托管，灵活扩展，适合中小企业和技术团队自行运营。

**典型接入方式**  
1. **API / SDK**：通过 RESTful API 或官方 Ruby / JavaScript SDK 将聊天窗口嵌入前端页面，后端可调用模型服务（如 OpenAI、Claude、Gemini）实现智能回复。  
2. **Webhook 与自定义插件**：在 Chatwoot 中配置 webhook，将对话事件推送到自建的 AI 微服务，返回生成的消息再回写到会话。  
3. **CLI / Docker 部署**：使用官方 Docker 镜像或 `chatwoot-cli` 快速启动本地或云端实例，配合 Kubernetes/Helm 进行弹性扩容。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23，项目最近一次提交，星标 33 276，fork 7 842，社区贡献持续。  
- **成熟的生态**：提供完整的文档、示例代码和多语言 SDK，支持 OAuth、SAML、Slack、WhatsApp 等多渠道集成。  
- **可扩展性**：基于 PostgreSQL + Redis，支持水平扩容；Docker/K8s 部署方案成熟，易于在企业内部或云端实现高可用。  
- **安全与合规**：采用 MIT 许可证，代码审计活跃，安全报告响应及时，适合作为正式生产环境的客服核心。  

综上，Chatwoot 具备高可用、易集成、社区活跃的特性，是在生产环境中快速引入 AI 客服能力的可靠 OSS 选项。

## 🧭 Practical evaluation

**Value:** chatwoot/chatwoot helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 33276 GitHub stars
- 7842 forks
- updated 2026-06-23
- primary language: Ruby
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 97/100 |
| stars | 96/100 |
| topics | 100/100 |
| outlook | 91/100 |
| quality | 98/100 |
| recency | 100/100 |
| adoption | 97/100 |
| production | 83/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/chatwoot/chatwoot) · [← Back to AI/ML](./README.md)</sub>
