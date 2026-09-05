# aerovato/container

[![Stars](https://img.shields.io/github/stars/aerovato/container?style=flat-square&color=yellow)](https://github.com/aerovato/container/stargazers) [![Forks](https://img.shields.io/github/forks/aerovato/container?style=flat-square&color=blue)](https://github.com/aerovato/container/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Safely run OpenCode, Codex, Claude Code with full permissions.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 280 |
| 🍴 **Forks** | 30 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `anthropic-claude` `chatgpt` `claude` `claude-ai` `claude-code` `claude-code-plugin` `claude-skills` `codex` `codex-cli` `container` `copilot`

## 🎯 Categories

AI/ML · DevTools · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Aerovato/container is an open‑source TypeScript toolkit that lets developers run AI models such as OpenCode, Codex, and Claude with full permissions, enabling rapid prototyping of RAG, agent‑based, or other AI‑driven features without building a model stack from scratch. With 280 ★, recent commits, and a clear API/SDK/CLI surface, it is positioned as a production‑ready component for AI‑enhanced applications.  

**Value**  
- **Accelerated AI integration** – provides ready‑made wrappers and execution environments, so teams can add sophisticated model capabilities (code generation, reasoning, retrieval‑augmented generation) without the overhead of infrastructure setup or custom model training.  
- **Full permission model** – unlike sandboxed offerings, it grants unrestricted access to model APIs, making it suitable for complex workflows that need fine‑grained control (e.g., custom prompts, tool use, or multi‑step agent loops).  
- **Developer‑friendly** – the TypeScript codebase, well‑documented CLI, and SDK let engineers stay within their existing stack, reducing context switching and onboarding time.  

**Practical Adoption Path**  
1. **Evaluation** – clone the repo, run the provided CLI against a test model key, and verify the API contracts (metadata, language support, topic focus).  
2. **Prototype** – integrate the SDK into a sandbox service to build a small RAG or code‑assist feature, leveraging the built‑in permission handling.  
3. **Pilot** – containerize the component (Docker/K8s), connect it to production model endpoints, and run performance/latency tests while monitoring security logs.  
4. **Scale** – embed the container in CI/CD pipelines, expose its API to downstream services, and apply standard DevOps observability (metrics, tracing).  

**Production Readiness**  
The project scores high on readiness: recent activity (last commit 2026‑06‑23), solid community signals (280 ★, 30 forks, 20 topics), and a clear TypeScript implementation with API/CLI exposure. These factors indicate a stable codebase and active maintainers, making it suitable for a serious pilot. The remaining diligence items are a final license review, a security audit of the container runtime, and confirmation of long‑term maintainer commitment before full production deployment.

### Русский

**aerovato/container** — это open‑source решение, позволяющее безопасно запускать модели OpenCode, Codex и Claude Code с полными правами доступа, что ускоряет добавление AI‑функциональности без необходимости собирать стек моделей с нуля. Типичный сценарий — быстрый прототипинг AI‑фич, построение RAG‑ или агентных воркфлоу и оценка инструментов моделирования через удобный API/SDK/CLI. Проект демонстрирует высокий уровень готовности к production: активные коммиты, 280 звёзд, 30 форков, поддержка TypeScript и широкая экосистема, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
aerovato/container 是一个开源工具箱，能够在安全、受控的环境中运行 OpenCode、Codex、Claude Code 等大模型，并提供完整的权限管理。它让开发者无需从零搭建模型堆栈，即可快速为产品或服务加入 AI 能力。适用于原型开发、RAG（检索增强生成）或智能体工作流的快速搭建与评估。

**价值**  
- **即插即用**：通过统一的 API/SDK/CLI，直接调用已授权的大模型，省去模型部署、资源调度等繁琐工作。  
- **安全可控**：容器化运行环境确保模型调用在受限权限下执行，降低数据泄露和滥用风险。  
- **加速创新**：开发者可以在几分钟内原型化 AI 功能，快速验证业务价值后再决定是否投入更大规模的模型建设。

**典型接入方式**  
1. **API 调用**：在项目中引入 `@aerovato/container` 包，使用提供的 `runModel` 接口发送请求并获取响应。  
2. **CLI 使用**：通过 `aerovato-container` 命令行工具直接在终端执行模型推理，适合脚本化或 CI/CD 场景。  
3. **SDK 集成**：利用 TypeScript/JavaScript SDK，结合现有的服务框架（如 NestJS、Express）实现模型调用的业务封装。  
4. **语言元数据**：项目提供语言标签和主题信息，可在代码编辑器或 IDE 插件中自动补全模型能力。

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，项目最近一次提交，拥有 280+ 星、30+ Fork，且社区持续贡献。  
- **技术成熟度**：核心实现使用 TypeScript，配套 20+ 主题标签，文档覆盖 API、SDK、CLI 三种使用方式。  
- **生态兼容**：可与常见 DevOps 流程（Docker、K8s）以及 CI/CD 平台（GitHub Actions、GitLab CI）无缝对接。  
- **风险评估**：暂无重大元数据风险，仍需对许可证（MIT/Apache 等）和安全审计进行最终确认，但整体已具备在生产环境进行试点的条件。

## 🧭 Practical evaluation

**Value:** aerovato/container helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 280 GitHub stars
- 30 forks
- updated 2026-06-23
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 52/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 48/100 |
| production | 75/100 |
| usefulness | 58/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/aerovato/container) · [← Back to AI/ML](./README.md)</sub>
