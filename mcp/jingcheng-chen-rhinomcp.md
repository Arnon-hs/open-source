# jingcheng-chen/rhinomcp

[![Stars](https://img.shields.io/github/stars/jingcheng-chen/rhinomcp?style=flat-square&color=yellow)](https://github.com/jingcheng-chen/rhinomcp/stargazers) [![Forks](https://img.shields.io/github/forks/jingcheng-chen/rhinomcp?style=flat-square&color=blue)](https://github.com/jingcheng-chen/rhinomcp/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> RhinoMCP connects Rhino 3D to AI Agent through the Model Context Protocol (MCP)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 777 |
| 🍴 **Forks** | 82 |
| 💻 **Language** | Python |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

MCP · AI/ML

## 📝 Summary

### English

**Summary**  
RhinoMCP (jingcheng‑chen/rhinomcp) is a Python library that implements the Model Context Protocol (MCP) to let Rhino 3D communicate with AI agents, turning Rhino’s design tools and data into actionable resources for language models. By exposing a standard MCP server, it enables developers to plug AI assistants into real‑world CAD workflows with minimal custom glue code.  

**Value**  
The project provides a reusable, protocol‑based bridge between a popular 3D modeling environment and AI assistants, making it far easier to build “AI‑in‑the‑loop” design tools, automate repetitive modeling tasks, or prototype intelligent assistants that can query and manipulate Rhino geometry directly. Because MCP is a community‑driven standard, the same integration can be reused across different AI platforms and downstream tools, reducing duplication of effort.

**Practical adoption path**  

1. **Proof‑of‑concept** – Clone the repo, follow the README to spin up a local MCP server, and connect a simple OpenAI‑compatible agent (e.g., LangChain or Llama‑Index) to test basic commands such as “list layers” or “create a cylinder.”  
2. **Iterate on the API** – Extend the server with custom Rhino scripts or plug‑ins needed for your specific workflow, using the provided Python wrappers.  
3. **Containerize & CI** – Package the MCP server in a Docker image and add automated tests that validate the agent‑to‑Rhino round‑trip.  
4. **Production rollout** – Deploy the server behind a secure gateway, enforce authentication, and monitor logs for any malformed MCP messages before exposing it to end users.

**Production readiness**  
The library is moderately mature (777 ★, 82 forks, recent updates as of 2026‑06‑28) and suitable for prototypes or internal pipelines. It still requires a security review (authentication, sandboxing of Rhino commands) and a check on licensing/maintainer activity before being used in a customer‑facing product. With those safeguards in place, RhinoMCP can be a reliable component for production‑grade AI‑augmented CAD solutions.

### Русский

**RhinoMCP** — открытый Python‑проект, который реализует Model Context Protocol (MCP) и позволяет связывать Rhino 3D с AI‑ассистентами, превращая 3D‑модели в живой контекст для генеративных моделей. Типичный сценарий — запуск небольшого proof‑of‑concept: развернуть MCP‑сервер, подключить к нему AI‑агента и через единый протокол управлять Rhino‑инструментами и данными; затем масштабировать решение до внутреннего или клиентского продукта. Готовность к production — средняя: проект уже стабилен и активно поддерживается (777 ★, 82 fork, последние коммиты), но перед выпуском в продакшн требуется проверка лицензии, безопасности и зависимости.

### 中文

**项目简介**  
RhinoMCP（jingcheng-chen/rhinomcp）是一个开源库，基于 **Model Context Protocol (MCP)** 为 Rhino 3D 与 AI Agent（如 ChatGPT、Claude 等）之间搭建统一的通信桥梁，使 AI 能够直接调用 Rhino 的建模功能和数据。

---

### 价值点
1. **标准化接口**：通过 MCP 将 AI 助手与真实工具解耦，避免为每个工具单独写适配层。  
2. **快速原型**：开发者只需几行代码即可让 AI 在 Rhino 中执行建模、查询属性等操作，大幅缩短 AI‑工具集成的迭代周期。  
3. **生态兼容**：遵循 MCP 规范后，同一套 AI 逻辑可以无缝迁移到其他支持 MCP 的软件（如 Blender、Revit），实现“一次开发，多处复用”。  

---

### 典型接入方式
1. **准备工作**  
   - 确保本地或服务器上已安装 Rhino 7+ 与 Python（推荐 3.10+）。  
   - `pip install rhinocomp`（项目实际的 PyPI 包名）或直接克隆仓库并 `pip install -e .`。  

2. **启动 MCP 服务器**（在 Rhino 端）  
   ```python
   from rhinocomp.server import MCPServer
   server = MCPServer(host="0.0.0.0", port=5000)
   server.start()
   ```
   服务器会监听 MCP 消息并将请求转发给 Rhino 的 API。

3. **在 AI Agent 侧实现客户端**（示例使用 OpenAI Function Calling）  
   ```python
   import openai, requests, json

   def call_mcp(method, params):
       resp = requests.post("http://<rhino-host>:5000/mcp", json={"method": method, "params": params})
       return resp.json()

   # 在函数定义里把 call_mcp 包装成 OpenAI 可调用的函数
   ```

4. **验证**：在对话中让 AI 调用 `call_mcp("create_box", {"width":2,"height":1,"depth":3})`，观察 Rhino 中是否生成对应模型。  

> **小技巧**：先在 `README` 中的 “quick‑start” 示例跑通一次，确认网络、端口、Rhino 版本匹配后，再把调用封装进业务系统。

---

### 生产可用性评估
| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | 中等 | 代码已在 GitHub 获得 777 ⭐、82 🍴，最近一次提交是 2026‑06‑28，活跃度尚可。适合作为原型或内部工具的底层组件。 |
| **依赖与维护** | 需要审查 | 依赖 Rhino 的 COM/CPython 接口，部署时需确保 Rhino 许可证和对应的 Python 环境。建议在正式环境做依赖锁定（`requirements.txt`）并监控安全公告。 |
| **安全/合规** | 待确认 | 项目未明确声明许可证（需检查 `LICENSE` 文件），以及对外网络暴露的 API 需加鉴权（如 JWT、IP 白名单）后方可上线。 |
| **可扩展性** | 良好 | 基于 MCP 的消息模型天然支持多线程/异步扩展，且可以在同一服务器上同时服务多个 AI 实例。 |
| **上线建议** | **阶段性** | 1️⃣ 先在沙盒环境完成端到端 PoC；<br>2️⃣ 为 MCP 接口添加身份验证和请求审计；<br>3️⃣ 将服务器容器化（Docker）并加入 CI/CD；<br>4️⃣ 进行负载与容错测试后再投入生产。 |

**结论**：RhinoMCP 为将 AI 助手与 Rhino 3D 绑定提供了一个标准化、易上手的桥梁，适合作为 **原型验证** 或 **内部工作流自动化** 的基础设施。经适当的安全加固和运维监控后，可逐步推广到生产环境。

## 🧭 Practical evaluation

**Value:** jingcheng-chen/rhinomcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 777 GitHub stars
- 82 forks
- updated 2026-06-28
- primary language: Python

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 62/100 |
| topics | 0/100 |
| outlook | 67/100 |
| quality | 61/100 |
| recency | 80/100 |
| adoption | 58/100 |
| production | 67/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/jingcheng-chen/rhinomcp) · [← Back to Mcp](./README.md)</sub>
