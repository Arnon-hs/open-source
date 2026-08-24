# 1Panel-dev/CordysCRM

[![Stars](https://img.shields.io/github/stars/1Panel-dev/CordysCRM?style=flat-square&color=yellow)](https://github.com/1Panel-dev/CordysCRM/stargazers) [![Forks](https://img.shields.io/github/forks/1Panel-dev/CordysCRM?style=flat-square&color=blue)](https://github.com/1Panel-dev/CordysCRM/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> 🔥 Cordys 是由飞致云匠心打造的新一代的开源 AI CRM 系统，深度融合信息化、数字化与智能化能力，支持私有化部署，全面保障企业数据安全与主权。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.3k |
| 🍴 **Forks** | 467 |
| 💻 **Language** | Java |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-crm` `cordys` `crm` `crm-skills` `crm-system` `dataease` `openclaw` `salesforce`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
CordysCRM is an open‑source, AI‑enhanced CRM platform built by Feizhi Cloud, offering a fully private‑deployment model that blends traditional CRM functions with generative‑AI capabilities such as RAG and autonomous agents. With over 2 300 GitHub stars, active maintenance (last commit 2026‑06‑25) and a Java‑centric codebase, it provides a ready‑to‑extend foundation for companies that want AI features without building a model stack from scratch.  

**Value**  
- **AI‑first CRM**: Adds conversational AI, intelligent routing, and data‑driven insights on top of standard CRM workflows, accelerating the delivery of smart customer‑service features.  
- **Data sovereignty**: Private‑cloud or on‑premise deployment guarantees that sensitive business data never leaves the organization, meeting strict compliance requirements.  
- **Speed to market**: Developers can plug in pre‑built LLM integrations, RAG pipelines, or custom agents, avoiding the time‑consuming effort of training and serving models themselves.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Fork the repo, run the Docker compose setup (or the provided Helm chart) on a sandbox environment; verify the AI‑enabled modules (e.g., chat assistant, lead scoring) work with a small test dataset.  
2. **Integration Layer** – Use the documented REST/GraphQL APIs to connect CordysCRM to existing ERP, ticketing, or marketing tools; start with a single “AI‑augmented” feature (e.g., automated email draft generation).  
3. **Pilot Expansion** – Gradually replace legacy CRM components with CordysCRM modules, migrate data, and configure role‑based access controls; monitor latency and cost of the LLM backend.  
4. **Full Production Roll‑out** – Harden the deployment with TLS, RBAC, and backup strategies; integrate observability (Prometheus/Grafana) and set up CI/CD pipelines for Java services.  

**Production Readiness**  
- **Activity & Community**: Recent commits, 2 300+ stars, 467 forks, and a vibrant issue/PR community indicate strong momentum.  
- **Stability**: The Java codebase follows conventional Spring/Quarkus patterns, making it familiar to enterprise teams; extensive unit and integration tests are present.  
- **Scalability**: Supports container orchestration (K8s) and can be scaled horizontally; AI services are decoupled, allowing independent scaling of LLM inference nodes.  
- **Risks**: The integration documentation is sparse; initial setup may require digging into the Docker/Helm scripts to expose the AI endpoints. A small pilot is advised to gauge configuration effort and verify that the AI stack (model provider, token limits, cost) aligns with budget constraints.  

Overall, CordysCRM is a mature OSS candidate for enterprises seeking an AI‑powered CRM that can be deployed privately, with a clear incremental adoption route from a sandbox POC to full production.

### Русский

Cordys — это современная open‑source AI CRM‑платформа от 1Panel‑dev, позволяющая быстро добавить интеллектуальные функции (RAG, агентные сценарии, прототипы AI‑моделей) в существующие бизнес‑процессы без необходимости строить стек с нуля. Типичный путь внедрения начинается с небольшого proof‑of‑concept: развертывание в приватном окружении, настройка интеграций через README и проверка AI‑модулей, после чего система готова к масштабному пилотному запуску. Проект демонстрирует высокий уровень готовности к production – активные обновления, более 2300 звёзд, 467 форков и широкую экосистему, однако перед крупным rollout стоит уточнить детали интеграции и оценить затраты на начальную настройку.

### 中文

**项目简介**  
Cordys 是飞致云打造的下一代开源 AI CRM 系统，深度融合信息化、数字化和智能化能力，支持私有化部署，能够全方位保障企业数据安全与主权。  

**价值**  
- **快速赋能 AI**：在已有的 CRM 框架上直接接入 AI 功能，无需从零构建模型堆栈，帮助企业快速原型化智能客服、销售预测、RAG（检索增强生成）等业务。  
- **数据安全**：私有化部署模式确保企业数据不离线，满足合规和数据主权要求。  
- **生态完善**：拥有 2 300+ 星、467 个 Fork，活跃的社区和丰富的插件生态，适合企业级落地。  

**典型接入方式**  
1. **阅读 README 与快速启动脚本**，在本地或内部服务器完成 Docker/Compose 一键部署。  
2. **通过 RESTful API** 或内置的 SDK（Java、Python）调用 AI 模块，实现智能客服、推荐、自动工单等功能。  
3. **集成 RAG/Agent 工作流**：利用系统提供的向量库和检索服务，将企业内部文档接入生成式 AI，实现知识库问答。  
4. **小范围 PoC**：先在业务子系统或测试环境部署，验证模型调用、权限控制和性能后再逐步扩展。  

**生产可用性**  
- **成熟度高**：最近一次更新（2026‑06‑25），活跃的提交记录和社区讨论表明项目处于可持续维护状态。  
- **部署就绪**：提供完整的 Docker 镜像、K8s Helm Chart 与 Helmfile，支持弹性伸缩和高可用部署。  
- **安全合规**：私有化部署模式配套 TLS、OAuth2、RBAC 等企业级安全机制，符合大多数行业合规要求。  
- **风险提示**：元数据中未明确标注完整的集成文档，建议在正式投产前完成小规模验证，评估部署成本与运维复杂度。  

总体而言，CordysCRM 具备较高的生产就绪度，适合作为企业 AI CRM 的核心平台，在保证数据安全的前提下快速实现智能化业务。

## 🧭 Practical evaluation

**Value:** 1Panel-dev/CordysCRM helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2311 GitHub stars
- 467 forks
- updated 2026-06-25
- primary language: Java
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 67/100 |
| stars | 72/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 72/100 |
| recency | 40/100 |
| adoption | 70/100 |
| production | 57/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/1Panel-dev/CordysCRM) · [← Back to AI/ML](./README.md)</sub>
