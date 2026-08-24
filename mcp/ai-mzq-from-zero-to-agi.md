# AI-mzq/From-Zero-to-AGI

[![Stars](https://img.shields.io/github/stars/AI-mzq/From-Zero-to-AGI?style=flat-square&color=yellow)](https://github.com/AI-mzq/From-Zero-to-AGI/stargazers) [![Forks](https://img.shields.io/github/forks/AI-mzq/From-Zero-to-AGI?style=flat-square&color=blue)](https://github.com/AI-mzq/From-Zero-to-AGI/network) [![Language](https://img.shields.io/badge/lang-Jupyter%20Notebook-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> 从零走向AGI之路！！！旨在深入了解通用人工智能（AGI）的发展路径，从最基础的概念起，逐步构建完整的知识体系。涵盖AI Agent、RAG、MCP、具身智能、大语言模型、多模态、数字人、AI绘画、AI视频等！！

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 224 |
| 🍴 **Forks** | 24 |
| 💻 **Language** | Jupyter Notebook |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML

## 📝 Summary

### English

**Project Summary**
From-Zero-to-AGI is an open-source project aiming to comprehensively understand the development path of General Artificial Intelligence (AGI). It covers various AI-related topics, including AI agents, RAG, MCP, embodied intelligence, and more. The project helps connect AI assistants to real tools and data through a standard protocol.

**Value Proposition**
The value proposition of From-Zero-to-AGI lies in its ability to standardize integrations between AI agents and tools, enabling a seamless connection between AI assistants and real-world data. This standard protocol facilitates the development of more efficient and effective AI systems.

**Practical Adoption Path**
To adopt From-Zero-to-AGI, users should start with a small proof of concept and carefully review the README documentation. This will help evaluate the feasibility of integration and ensure a smooth onboarding process. As the project is still in development, it is recommended to use it in prototypes or internal workflows, where dependency and maintenance checks can be performed before production.

**Production Readiness**
From-Zero-to-AGI has a medium production readiness score, indicating that it is suitable for use in prototypes or internal workflows. However, before deploying it in production, users should conduct thorough reviews of the license, security posture, and active maintain

### Русский

**AI‑mzq/From‑Zero‑to‑AGI** — открытый набор Jupyter‑ноутбуков, который шаг за шагом формирует полную образовательную и практическую экосистему AGI: от базовых концепций и моделей больших языков до интеграции AI‑агентов с инструментами (RAG, MCP, цифровыми персонажами, генерацией изображений и видео). Типичный сценарий внедрения — быстрое прототипирование соединения AI‑ассистентов с реальными сервисами через стандартный Model Context Protocol, позволяющее запустить Proof‑of‑Concept и затем развить его в масштабируемый сервис. Готовность к production — средняя: проект достаточно стабилен для внутренних прототипов, но требует проверки лицензии, обеспечения безопасности и контроля зависимостей перед выпуском в продакшн.

### 中文

**价值**  
- **统一标准**：项目通过 **Model Context Protocol（MCP）** 为 AI Agent、RAG、工具链等提供统一的通信协议，解决了“AI 助手如何安全、可靠地调用外部工具和数据”这一痛点。  
- **完整知识体系**：从最基础的概念到多模态、数字人、AI 绘画/视频等前沿技术，形成一套可循序渐进的学习与实验路径，帮助研发团队快速搭建并验证自己的 AGI 原型。  
- **快速原型**：提供可直接运行的 Jupyter Notebook 示例，降低了从概念验证到 MVP 的门槛，适合内部实验、Hackathon 以及教学演示。

**典型接入方式**  

| 步骤 | 操作 | 关键点 |
|------|------|--------|
| 1️⃣ 环境准备 | `git clone https://github.com/AI-mzq/From-Zero-to-AGI.git` → `conda create -n agi python=3.10` → `pip install -r requirements.txt` | 项目主要依赖 Jupyter、transformers、langchain 等常用库。 |
| 2️⃣ 启动 MCP 服务器 | 在 `mcp_server/` 目录运行 `python server.py`（或使用 Docker：`docker compose up -d`） | 服务器遵循 OpenAPI 规范，默认监听 `http://localhost:8000`。 |
| 3️⃣ 接入 AI Agent | 在 Notebook 中引入 `from mcp_client import MCPClient`，实例化 `client = MCPClient(endpoint="http://localhost:8000")`，随后使用 `client.invoke_tool(tool_name, args)` 调用外部工具。 | 客户端封装了请求签名、超时重试等细节，接入成本低。 |
| 4️⃣ 集成业务系统 | 将 MCP 端点配置到业务后台（如 Flask、FastAPI），或通过 webhook 将工具结果回传给 Agent。 | 推荐使用 JWT 或 API‑Key 做身份校验，防止未授权调用。 |
| 5️⃣ 迭代扩展 | 按需在 `tools/` 目录新增自定义工具（Python 脚本或微服务），并在 `mcp_schema.yaml` 中声明接口。 | 通过自动生成的 SDK（`openapi-generator`）保持前后端一致。 |

**生产可用性评估**  

| 维度 | 现状 | 建议 |
|------|------|------|
| **成熟度** | ★★☆☆☆（GitHub ★224，活跃更新至 2026‑07‑03） | 适合作为 **原型/内部实验** 环境；在生产前需完成代码审计和单元测试。 |
| **依赖管理** | 依赖主要是开源 ML 框架（transformers、torch）和 LangChain，版本更新频繁。 | 使用 `conda-lock` 或 `pip-tools` 锁定依赖版本，防止突发兼容性问题。 |
| **安全性** | 项目本身未提供完整的身份认证/审计机制。 | 在部署层加入 API‑Gateway（如 Kong、Traefik）进行鉴权、流量控制和日志审计。 |
| **可扩展性** | MCP 采用 OpenAPI，天然支持多语言 SDK 与微服务化部署。 | 通过 Docker‑Compose 或 Kubernetes 部署，可水平扩展工具服务。 |
| **运维成本** | 需要维护 MCP 服务器、模型推理服务以及对应的 GPU/CPU 资源。 | 建议使用云厂商的托管模型服务（如 AWS SageMaker、Azure ML）降低模型运维负担。 |

**结论**  
- **价值**：提供统一、可扩展的协议层，使 AI Agent 能够安全、标准化地调用外部工具和数据，配合完整的 AGI 学习路线图，帮助团队快速从概念走向可交付的原型。  
- **接入方式**：克隆仓库 → 部署 MCP 服务器（本地或容器） → 在 Notebook/业务代码中使用 MCP 客户端调用工具 → 按需扩展自定义工具。  
- **生产可用性**：当前适合 **原型/内部使用**；在正式生产环境需完成安全加固、依赖锁定、监控告警以及容器化部署等步骤后方可上线。

## 🧭 Practical evaluation

**Value:** AI-mzq/From-Zero-to-AGI helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 224 GitHub stars
- 24 forks
- updated 2026-07-03
- primary language: Jupyter Notebook

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 50/100 |
| topics | 0/100 |
| outlook | 53/100 |
| quality | 46/100 |
| recency | 40/100 |
| adoption | 46/100 |
| production | 50/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/AI-mzq/From-Zero-to-AGI) · [← Back to Mcp](./README.md)</sub>
