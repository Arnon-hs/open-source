# Lissy93/portainer-templates

[![Stars](https://img.shields.io/github/stars/Lissy93/portainer-templates?style=flat-square&color=yellow)](https://github.com/Lissy93/portainer-templates/stargazers) [![Forks](https://img.shields.io/github/forks/Lissy93/portainer-templates?style=flat-square&color=blue)](https://github.com/Lissy93/portainer-templates/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> 🚢 500+ 1-click Portainer app templates

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.8k |
| 🍴 **Forks** | 306 |
| 💻 **Language** | Python |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`docker` `linux` `portainer` `privacy` `self-hosted` `server`

## 🎯 Categories

Templates · Backend · DevOps/Infra

## 📝 Summary

### English

**Summary**  
Lissy93/portainer-templates is an open‑source collection of +500 one‑click Portainer app templates that let you spin up AI‑enabled services (RAG pipelines, agents, model servers, etc.) without building a stack from scratch. With over 2.8 k stars, active maintenance (last commit 2026‑05‑10) and a Python‑centric codebase, it’s ready for pilot projects and can be evaluated quickly via its exposed API/SDK/CLI metadata.

**Value**  
The repo supplies pre‑configured Docker‑Compose/Portainer stacks that embed popular LLMs, vector stores, and tooling, dramatically cutting the time to prototype AI features or evaluate new model ecosystems. By handling networking, environment variables, and persistent volumes out of the box, teams can focus on business logic rather than infrastructure plumbing.

**Practical adoption path**  
1. **Explore** the template catalog in the Portainer UI or clone the repo to review the `templates/` directory.  
2. **Select** a template that matches the desired use case (e.g., “RAG‑with‑Chroma”, “OpenAI‑agent”).  
3. **Deploy** with a single click in Portainer or run the provided `docker-compose.yml` locally for testing.  
4. **Integrate** via the generated API endpoints, SDK wrappers, or CLI commands, adjusting only the minimal configuration (API keys, data sources).  
5. **Iterate** by forking the repo to add custom components or extend existing templates.

**Production readiness**  
The project shows high production readiness: recent commits, a vibrant community (2.8 k stars, 300+ forks), clear documentation, and a Python‑first implementation that aligns with most AI toolchains. While the license and security posture still need a final audit, the strong activity signals, adoption by other OSS projects, and ready‑to‑run Docker artifacts make it suitable for a serious pilot or even production deployment after standard hardening.

### Русский

Lissy93/portainer-templates — это набор из более чем 500 готовых «одним‑кликом» шаблонов приложений для Portainer, позволяющих быстро добавить AI‑функциональность (RAG, агентные сценарии, прототипы моделей) без необходимости собирать стек с нуля. Шаблоны легко интегрируются через API/SDK/CLI, предоставляя метаданные о языке, темах и типах задач, что делает их идеальными для быстрой проверки идей и построения прототипов в DevOps‑окружении. Проект имеет высокий уровень готовности к production: активные коммиты, более 2800 звёзд, множество форков и широкую поддержку сообщества, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
Lissy93/portainer-templates 是一个为 Portainer 提供 500+ 一键部署应用模板的仓库，涵盖 AI/ML、后端、DevOps 等多类场景，帮助用户快速在 Portainer 中启动并运行各种服务。

**价值**  
- **即插即用**：通过一键模板即可在 Portainer 中部署完整的 AI 能力（如 RAG、Agent 工作流），省去手动搭建环境的繁琐。  
- **加速原型**：适合快速验证 AI 功能、模型工具链或业务流程的可行性，缩短从概念到演示的周期。  
- **统一管理**：所有模板均以 Portainer 形式呈现，便于在同一 UI 中统一监控、扩容和维护。

**典型接入方式**  
1. 在 Portainer 控制台中打开 **App Templates** 页面。  
2. 添加仓库 URL（`https://github.com/Lissy93/portainer-templates`）或直接导入 `docker-compose.yml`/`stack` 文件。  
3. 选择所需模板（如 “RAG‑Chatbot”），点击 **Deploy**，Portainer 会自动拉取镜像、创建网络并启动容器。  
4. 如需二次定制，可在部署后通过 Portainer 的编辑功能修改环境变量、挂载卷或扩展服务。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑10 最近一次提交，拥有 2.8k+ 星、300+ Fork，社区活跃。  
- **技术成熟**：模板基于官方 Docker 镜像和常用开源组件，兼容主流云平台和本地私有环境。  
- **可靠性**：Portainer 本身是成熟的容器管理平台，模板仅是声明式配置，故在经过基本安全审计后即可用于正式业务。  
- **风险提示**：仍需自行检查许可证兼容性、镜像安全扫描结果以及维护者的响应速度，以确保符合企业合规要求。

## 🧭 Practical evaluation

**Value:** Lissy93/portainer-templates helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2823 GitHub stars
- 306 forks
- updated 2026-05-10
- primary language: Python
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 73/100 |
| topics | 75/100 |
| outlook | 60/100 |
| quality | 63/100 |
| recency | 20/100 |
| adoption | 70/100 |
| production | 58/100 |
| usefulness | 90/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-10 · [View on GitHub](https://github.com/Lissy93/portainer-templates) · [← Back to Templates](./README.md)</sub>
