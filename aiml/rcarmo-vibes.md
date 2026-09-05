# rcarmo/vibes

[![Stars](https://img.shields.io/github/stars/rcarmo/vibes?style=flat-square&color=yellow)](https://github.com/rcarmo/vibes/stargazers) [![Forks](https://img.shields.io/github/forks/rcarmo/vibes?style=flat-square&color=blue)](https://github.com/rcarmo/vibes/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> A simple mobile-focused chat app to talk to an agent via the ACP protocol

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 179 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | Go |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`acp` `agents` `claude` `codex` `copilot` `mistral`

## 🎯 Categories

AI/ML · Communication

## 📝 Summary

### English

**Project Summary:**

rcarmo/vibes is an open-source, mobile-focused chat app that enables communication with an agent via the ACP protocol, making it easier to add AI capabilities to existing projects. This project helps developers prototype AI features, build RAG (Reasoning and Action Graph) or agent workflows, and evaluate model tooling without starting from scratch. With its medium production readiness, it is suitable for internal workflows or prototypes, requiring further dependency and maintenance checks before production.

**Value:**

The primary value proposition of rcarmo/vibes lies in its ability to add AI capabilities without requiring a complete model stack. This makes it an ideal choice for developers who want to prototype AI features or build RAG or agent workflows without investing significant time and resources.

**Practical Adoption Path:**

To adopt rcarmo/vibes, developers can follow these steps:

1. Evaluate the project by reading the README and running a small proof of concept to understand its feasibility.
2. Assess the project's dependencies and maintenance requirements to ensure they align with your project's needs.
3. Prototype AI features or build RAG or agent workflows using rcarmo/vibes.
4. Integrate the project into your existing workflow, taking into account any necessary modifications or customizations

### Русский

Резюме проекта rcarmo/vibes:

Проект rcarmo/vibes представляет собой простую мобильную чат-приложение, позволяющую общаться с агентом по протоколу ACP. Это решение позволяет легко добавлять возможности искусственного интеллекта без создания полноценной модели стека. Проект подойдет для прототипирования функций AI, построения рабочих процессов с агентами и оценки инструментов для моделирования.

### 中文

**项目简介**  
rcarmo/vibes 是一款面向移动端的轻量级聊天应用，使用 ACP（Agent Communication Protocol）协议与后端 AI 代理进行对话。它提供了开箱即用的 UI 与协议实现，帮助开发者快速在移动产品中加入对话式 AI 功能。

**价值**  
- **快速原型**：无需从零搭建模型堆栈，直接使用现成的 ACP 客户端即可实现聊天、RAG（检索增强生成）或自定义 Agent 工作流。  
- **降低门槛**：通过 Go 语言实现的后端库，配合移动端 SDK，开发者可以在几行代码内完成 AI 能力的接入。  
- **评估与迭代**：提供完整的示例和 README，适合在内部评估不同模型、工具链或提示工程的效果。

**典型接入方式**  
1. **阅读 README**，确认项目依赖（Go 1.22+、Docker）以及 ACP 协议的配置方式。  
2. **启动后端服务**（`go run ./cmd/server` 或使用提供的 Docker Compose），并在 `config.yaml` 中填写目标模型的 API 密钥或本地模型路径。  
3. **在移动端**（iOS/Android）通过 Vibes SDK（或直接使用 HTTP/WebSocket）连接后端的 ACP 端点，调用 `sendMessage`/`receiveMessage` 即可实现聊天交互。  
4. **小范围 PoC**：先在测试环境部署单实例，验证协议兼容性、响应时延和错误处理后，再扩展到多实例或云原生部署。

**生产可用性**  
- **成熟度**：当前评分 61/100，GitHub 179 Stars，最近一次提交为 2026‑07‑07，代码活跃度一般。适合作为 **原型或内部工具**，但在直接面向客户的生产环境使用前，需要完成以下检查：  
  - 许可证合规（项目采用的开源许可证是否满足企业要求）  
  - 安全审计（依赖的 Go 包是否存在已知 CVE）  
  - 监控与容错（为后端服务添加健康检查、日志聚合、自动扩缩容）  
  - 维护计划（确认核心维护者的响应速度或自行 fork 形成长期维护分支）  

综上，rcarmo/vibes 能够显著缩短移动端 AI 功能的研发周期，推荐先在内部进行 PoC 验证，完成安全与运维准备后方可投入生产使用。

## 🧭 Practical evaluation

**Value:** rcarmo/vibes helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 179 GitHub stars
- 4 forks
- updated 2026-07-07
- primary language: Go
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 48/100 |
| topics | 75/100 |
| outlook | 67/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 39/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-07 · [View on GitHub](https://github.com/rcarmo/vibes) · [← Back to AI/ML](./README.md)</sub>
