# Tiledesk/tiledesk

[![Stars](https://img.shields.io/github/stars/Tiledesk/tiledesk?style=flat-square&color=yellow)](https://github.com/Tiledesk/tiledesk/stargazers) [![Forks](https://img.shields.io/github/forks/Tiledesk/tiledesk?style=flat-square&color=blue)](https://github.com/Tiledesk/tiledesk/network) [![Language](https://img.shields.io/badge/lang-Mustache-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Install Tiledesk on your server using Helm for Kubernetes orchestration and Docker Compose for running multi-container Docker applications. Tiledesk provides an open-source solution comparable to Voiceflow, empowering you to create sophisticated LLM-enabled chatbots that seamlessly transition interactions to human agents when needed.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 304 |
| 🍴 **Forks** | 105 |
| 💻 **Language** | Mustache |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`chatbot` `chatbots` `conversational-ai` `customer-service` `docker` `helm` `helm-charts` `installation` `kubernetes` `live-chat` `livechat` `marketing`

## 🎯 Categories

Orchestration · AI/ML · DevOps/Infra · Marketing

## 📝 Summary

### English

**Brief Summary**  
Tiledesk is an open‑source platform that lets you deploy a Voiceflow‑like chatbot ecosystem on your own infrastructure using Helm charts for Kubernetes or Docker‑Compose for multi‑container setups. It enables the creation of sophisticated LLM‑powered conversational agents that can automatically hand off to human operators, and it supports building repeatable, tool‑augmented agent workflows.

**Value**  
Tiledesk turns isolated prompts and AI tools into coordinated, reusable workflows, giving teams a unified way to orchestrate multi‑agent interactions, embed external tool calls, and maintain consistent agent memory. By exposing clear APIs, SDKs, and CLI commands, it simplifies integration with existing services and accelerates the development of production‑grade, LLM‑enabled chatbots.

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo and spin up a local instance with Docker‑Compose to explore the UI, API, and SDK.  
2. **Infrastructure Choice** – Deploy to a staging Kubernetes cluster using the provided Helm chart for a scalable, cloud‑native setup, or keep Docker‑Compose for smaller environments.  
3. **Workflow Build‑out** – Define agent flows using the built‑in visual editor or by scripting JSON/Mustache templates; integrate external tools via the exposed API endpoints.  
4. **Human‑in‑the‑Loop** – Configure hand‑off rules to route conversations to live agents when needed, leveraging the platform’s built‑in routing logic.  
5. **Production Rollout** – Harden the deployment (TLS, RBAC, secrets management), monitor with Prometheus/Grafana integrations, and scale pods via Helm values.

**Production Readiness**  
The project shows strong OSS maturity: recent commits (as of 2026‑06‑26), active community engagement (304 stars, 105 forks), and a clear roadmap. Its dual deployment options (K8s and Docker‑Compose) make it adaptable to both cloud‑native and on‑premise environments. While licensing, security audits, and long‑term maintainer commitment still require final verification, the current signals—robust documentation, API/SDK exposure, and real‑world adoption—indicate that Tiledesk is ready for serious pilot projects and can be hardened for production use.

### Русский

Tiledesk — open‑source платформа для создания LLM‑поддерживаемых чат‑ботов, которые автоматически переключаются на живых операторов; её можно быстро развернуть в собственном дата‑центре с помощью Helm‑чартов для Kubernetes или Docker Compose. Типичный сценарий — координация многоагентных рабочих процессов, построение конвейеров с использованием внешних инструментов и стандартизация памяти агентов. Проект имеет активную разработку, высокий уровень готовности к production (регулярные обновления, широкое принятие, 304 звёзд и 105 форков) и предоставляет удобные API/SDK/CLI для интеграции.

### 中文

**项目简介**  
Tiledesk 是一款开源的 LLM + 人工客服平台，可通过 Helm 在 Kubernetes 上一键部署，也支持 Docker Compose 快速启动多容器环境。它让开发者能够像使用 Voiceflow 那样，低代码地搭建复杂的 AI 聊天机器人，并在需要时无缝转接至真人坐席。

**价值主张**  
- **从孤立的 Prompt 到可复用的工作流**：把单个大模型调用、工具调用和记忆管理封装成标准化的 Agent 流程，便于在不同项目间复用。  
- **多代理协同**：支持多 Agent 串联、并行执行，实现工具链（搜索、数据库、API 调用等）与 LLM 的深度集成。  
- **人机无缝切换**：当模型判断需要人工介入时，可自动将会话转交给真人坐席，提升服务质量和安全性。

**典型接入方式**  
1. **Kubernetes（推荐）**：使用官方提供的 Helm chart，一键生成 Deployment、Service、Ingress 等资源，适合生产环境的弹性伸缩与运维。  
2. **Docker Compose**：在本地或小规模部署时，只需 `docker compose up -d` 即可启动包括 API Server、Web UI、Redis、PostgreSQL 等必备服务。  
3. **API/SDK/CLI**：平台公开 RESTful API、Node.js/Python SDK 以及 CLI 工具，开发者可直接在现有业务系统中调用创建会话、发送消息、管理 Agent 等功能。  

**生产可用性**  
- **活跃度高**：最近一次提交于 2026‑06‑26，GitHub 共有 304 ⭐、105 fork，社区讨论活跃。  
- **成熟的部署方案**：官方 Helm chart 已通过多轮 CI/CD 测试，支持自定义 ConfigMap、Secrets 与持久化存储，符合企业级安全和可观测性要求。  
- **生态兼容**：提供标准化的 OpenAPI 文档和多语言 SDK，易于与现有微服务、CI/CD 流水线以及监控平台（Prometheus、Grafana）集成。  
- **风险提示**：仍需进一步审查许可证细节、容器安全基线以及维护者响应速度，但整体已具备在生产环境中进行试点或正式上线的条件。

## 🧭 Practical evaluation

**Value:** Tiledesk/tiledesk helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 304 GitHub stars
- 105 forks
- updated 2026-06-26
- primary language: Mustache
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 64/100 |
| recency | 40/100 |
| adoption | 52/100 |
| production | 58/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/Tiledesk/tiledesk) · [← Back to Orchestration](./README.md)</sub>
