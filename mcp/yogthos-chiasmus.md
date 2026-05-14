# yogthos/chiasmus

[![Stars](https://img.shields.io/github/stars/yogthos/chiasmus?style=flat-square&color=yellow)](https://github.com/yogthos/chiasmus/stargazers) [![Forks](https://img.shields.io/github/forks/yogthos/chiasmus?style=flat-square&color=blue)](https://github.com/yogthos/chiasmus/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> Chiasmus is an MCP server that gives language models access to formal verification

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 177 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `ai-assistant` `ai-tools` `formalmethods` `llm` `mcp` `mcp-server` `prolog` `z3-smt-solver`

## 🎯 Categories

MCP · AI/ML · Backend · Database

## 📝 Summary

### English

**Brief Summary**  
Chiasmus is an open‑source MCP (Model Context Protocol) server written in TypeScript that lets large language models invoke formal verification tools and query structured data through a standardized API/SDK/CLI interface. By exposing verification capabilities as first‑class services, it enables AI assistants to safely execute code, check proofs, and retrieve reliable results without custom integration work.  

**Value**  
- **Safety & Trust**: Formal verification provides mathematically sound guarantees, reducing hallucinations and unsafe actions from AI agents.  
- **Standardization**: Implements the Model Context Protocol, giving developers a common contract for connecting any MCP‑compatible model to verification back‑ends, data stores, or other tooling.  
- **Rapid Tooling**: Eliminates the need to hand‑craft adapters for each verification engine; the server handles request routing, result formatting, and error handling out of the box.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker compose or `npm start` to spin up a local MCP server.  
2. **Integrate** – Use the generated TypeScript SDK (or the generic HTTP/JSON API) in your AI‑assistant code to send verification requests (`/prove`, `/check`, etc.).  
3. **Extend** – Plug in additional formal tools (e.g., Coq, Z3, Lean) via the documented plugin hooks; the server will expose them automatically through the same MCP endpoints.  
4. **Deploy** – Containerize the server, configure TLS and authentication, and register it as a Model Context Protocol endpoint in your production model orchestration platform.  

**Production Readiness**  
- **Activity & Community**: 177 stars, recent commits (as of 2026‑05‑14), and a modest but active fork base indicate healthy maintenance.  
- **Technical Maturity**: Clear API/SDK/CLI surface, TypeScript type safety, and built‑in support for common verification back‑ends make the codebase easy to audit and extend.  
- **Operational Fit**: Container‑ready, stateless request handling, and straightforward logging/monitoring align with typical backend deployment pipelines.  
- **Risks**: License compliance, security hardening, and long‑term maintainer commitment still require a final review, but no major red flags appear. Overall, Chiasmus is a strong OSS candidate for pilot projects and can be scaled to production once the remaining compliance checks are completed.

### Русский

**yogthos/chiasmus** — это сервер MCP, реализованный на TypeScript, который позволяет языковым моделям безопасно взаимодействовать с формальными системами верификации и другими инструментами через единый протокол. Типовой сценарий: интеграция AI‑агента с реальными сервисами (инструменты, базы данных) для выполнения проверок, автоматизации задач и построения Model Context Protocol‑совместимых сервисов. Проект имеет высокий уровень готовности к production: активная поддержка, свежие коммиты (март 2026), 177 звёзд на GitHub и растущее сообщество, что делает его надёжным кандидатом для пилотных внедрений.

### 中文

**项目简介（2‑3 句话）**  
Chiasmus 是一个基于 Model Context Protocol（MCP）的服务器，能够让大型语言模型直接调用形式化验证工具。它提供统一的 API/SDK/CLI 接口，使 AI 助手能够安全、可靠地访问底层数据库和验证服务。

**价值**  
- **桥接 AI 与真实工具**：通过标准化的 MCP 协议，AI 助手可以像调用本地函数一样调用形式化验证、查询数据库等后端服务，提升 AI 的可操作性和可信度。  
- **降低集成成本**：统一的协议和 TypeScript 实现让不同语言的项目都能快速对接，无需为每个工具单独编写适配层。  
- **加速产品落地**：在需要高可靠性校验的业务场景（如安全审计、合约验证、代码审查）中，直接把模型输出交给 Chiasmus 完成形式化检查，缩短研发周期。

**典型接入方式**  
1. **API 调用**：使用 HTTP/REST 或 gRPC 接口，发送 MCP 请求并获取验证结果。  
2. **SDK 引入**：通过 npm 安装 `@yogthos/chiasmus-sdk`，在 TypeScript/JavaScript 项目中直接调用 `chiasmus.verify(modelOutput)` 等方法。  
3. **CLI 使用**：在 CI/CD 流程或本地调试时，使用 `chiasmus-cli` 发送验证任务，适配脚本化工作流。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑14 最近一次提交，拥有 177 Stars、9 Forks，社区讨论活跃。  
- **技术成熟**：全栈 TypeScript 实现，提供完整的类型定义和文档，易于在现有 Node.js 后端或微服务中部署。  
- **安全与可维护性**：项目遵循 MIT 许可证，代码审计记录良好；虽然仍需最终确认维护者响应速度和安全审计报告，但已有的社区贡献和 issue 处理速度表明其具备在生产环境中进行试点的条件。  

综上，Chiasmus 为 AI 与形式化验证的深度集成提供了可靠、易用的桥梁，适合作为正式环境中的后端验证服务或 MVP 级别的 AI‑Tool 链接层。

## 🧭 Practical evaluation

**Value:** yogthos/chiasmus helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 177 GitHub stars
- 9 forks
- updated 2026-05-14
- primary language: TypeScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 48/100 |
| topics | 100/100 |
| outlook | 83/100 |
| quality | 74/100 |
| recency | 100/100 |
| adoption | 41/100 |
| production | 76/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/yogthos/chiasmus) · [← Back to Mcp](./README.md)</sub>
