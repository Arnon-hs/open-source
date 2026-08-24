# Rustam-Z/hamroh

[![Stars](https://img.shields.io/github/stars/Rustam-Z/hamroh?style=flat-square&color=yellow)](https://github.com/Rustam-Z/hamroh/stargazers) [![Forks](https://img.shields.io/github/forks/Rustam-Z/hamroh?style=flat-square&color=blue)](https://github.com/Rustam-Z/hamroh/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> "hamroh" is a AI agent harness framework for running your own persistent AI companion on Telegram — one you fully own, control, can extend, one that learns from you.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 36 |
| 🍴 **Forks** | 15 |
| 💻 **Language** | Python |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `ai-assistant` `nanoclaw` `openclaw`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Summary:**
Rustam-Z/hamroh is an open-source framework for building and running a persistent AI companion on Telegram, allowing users to create a customized AI agent that learns from them. This framework helps developers add AI capabilities without starting from scratch, making it ideal for prototyping and internal workflows. With its Python-based implementation and medium production readiness, hamroh offers a feasible path for evaluating and integrating AI features.

**Value:**
The primary value proposition of Rustam-Z/hamroh lies in its ability to simplify the process of adding AI capabilities to projects, making it easier for developers to create and customize AI agents. This framework provides a head start on building AI features, enabling developers to focus on extending and refining the AI model rather than starting from a blank slate.

**Practical Adoption Path:**
Developers can adopt Rustam-Z/hamroh by following these steps:

1. Evaluate the framework's feasibility by reading the README and performing a small proof of concept.
2. Assess the framework's production readiness by reviewing its dependencies, maintenance requirements, and security posture.
3. Integrate the framework into their project, leveraging its pre-built AI capabilities to streamline the development process.
4. Customize and extend the AI agent to meet their specific needs, using the

### Русский

**Rustam‑Z/hamroh** — это фреймворк‑обёртка для создания собственного постоянного AI‑компаньона в Telegram, полностью контролируемого и расширяемого пользователем, который учится на его данных. Он позволяет быстро добавить AI‑функциональность (прототипировать RAG‑ или агентные сценарии, оценивать инструменты моделей) без необходимости собирать стек с нуля; рекомендуется начать с небольшого proof‑of‑concept и проверки README. Готовность к продакшну – средняя: проект подходит для прототипов и внутренних workflow, но требует проверки зависимостей, лицензии и поддержки перед масштабным внедрением.

### 中文

**项目简介**  
“hamroh”是一个面向 Telegram 的 AI 代理框架，帮助你快速搭建并拥有一个可持续学习、可自行扩展的私人 AI 伴侣。它提供了现成的模型、记忆与工具链，让开发者无需从零构建即可实现对话、RAG（检索增强生成）和自定义工作流。

**价值**  
- **快速落地**：直接复用已有的模型堆栈和 Telegram 接入层，几小时即可得到可交互的 AI 伴侣。  
- **完全可控**：所有数据、记忆和扩展插件都在你的服务器上，避免第三方平台的隐私泄露。  
- **可扩展**：框架设计为插件化，支持自定义工具、检索库和业务逻辑，适配各种教育、客服或个人助理场景。

**典型接入方式**  
1. **准备环境**：克隆仓库，使用 `requirements.txt` 安装 Python 依赖（推荐在虚拟环境或 Docker 中）。  
2. **配置 Telegram Bot**：在 BotFather 创建 Bot，获取 `BOT_TOKEN` 并在 `.env` 中填写。  
3. **选择模型**：在 `config.yaml` 中指定本地模型路径或 OpenAI/Claude 等云模型的 API KEY。  
4. **启动服务**：运行 `python run.py`（或通过 Docker Compose 启动），机器人即开始监听 Telegram 消息。  
5. **扩展功能**：编写符合 `AgentPlugin` 接口的插件，实现检索、工具调用或自定义指令，然后在配置文件中注册即可。

**生产可用性**  
- **成熟度**：当前评分 63/100，适合作为原型或内部工作流使用。代码已更新至 2026‑07‑01，拥有 36 星、15 Fork，社区活跃度一般。  
- **依赖与维护**：核心依赖为 Python 生态（`transformers`、`langchain` 等），需自行管理模型下载和安全补丁；建议在容器化环境中运行并加入 CI/CD 监控。  
- **上线建议**：在生产环境部署前，先完成小规模 PoC，验证模型响应时延、记忆持久化和安全策略；随后进行负载测试、日志审计和权限硬化，方可进入正式业务。  

总体而言，**hamroh** 是一个“即插即用”且可高度定制的 AI 代理框架，适合快速验证 AI 功能或在受控环境中提供持续学习的个人助理；在完成依赖审计和运维准备后，可平滑迁移至生产使用。

## 🧭 Practical evaluation

**Value:** Rustam-Z/hamroh helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 36 GitHub stars
- 15 forks
- updated 2026-07-01
- primary language: Python
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 30/100 |
| stars | 33/100 |
| topics | 50/100 |
| outlook | 52/100 |
| quality | 47/100 |
| recency | 40/100 |
| adoption | 32/100 |
| production | 50/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/Rustam-Z/hamroh) · [← Back to AI/ML](./README.md)</sub>
