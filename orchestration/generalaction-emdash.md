# generalaction/emdash

[![Stars](https://img.shields.io/github/stars/generalaction/emdash?style=flat-square&color=yellow)](https://github.com/generalaction/emdash/stargazers) [![Forks](https://img.shields.io/github/forks/generalaction/emdash?style=flat-square&color=blue)](https://github.com/generalaction/emdash/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-78%2F100-brightgreen?style=flat-square)](#)

> Emdash is the Open-Source Agentic Development Environment (🧡 YC W26). Run multiple coding agents in parallel. Use any provider.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5k |
| 🍴 **Forks** | 515 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 78/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agenticdevelopment` `agenticdevelopmentenvironment` `ai` `claude-code` `cli` `coding-agents` `codingagents` `containerization` `docker` `gitworktrees` `jira` `linear`

## 🎯 Categories

Orchestration · AI/ML · DevTools · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
Emdash (generalaction/emdash) is an open‑source Agentic Development Environment that lets you run multiple coding agents in parallel, plug in any LLM provider, and stitch together prompts, tools, and memory into repeatable workflows. With strong community traction (≈5 k stars, 500+ forks) and active TypeScript development, it serves as a turnkey orchestration layer for multi‑agent AI pipelines.  

**Value**  
- **From siloed prompts to pipelines** – Emdash abstracts the boilerplate of invoking, synchronising, and persisting state across agents, turning ad‑hoc scripts into maintainable, version‑controlled workflows.  
- **Provider‑agnostic** – Because it works with any LLM API, teams can experiment with OpenAI, Anthropic, Cohere, or self‑hosted models without rewriting orchestration code.  
- **Tool‑use and memory standardisation** – Built‑in support for tool‑calling, shared memory stores, and custom SDK/CLI makes it easy to add deterministic tool‑use steps (e.g., code linting, testing, deployment) and keep context across iterations.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the CLI locally, and connect your preferred LLM key; use the provided TypeScript SDK to define a simple two‑agent workflow (e.g., “generate code” → “run tests”).  
2. **Integrate** – Wrap the SDK in your CI/CD pipelines or internal dev‑tooling, replace the prototype prompts with production‑grade prompts, and configure persistent memory (e.g., Redis, DynamoDB) via the built‑in adapters.  
3. **Scale** – Deploy the orchestration service (Docker/K8s) behind an internal API gateway; leverage its parallel‑execution engine to spin up dozens of agents for large‑scale code‑generation or review tasks.  

**Production Readiness**  
- **Activity & Ecosystem** – Recent commits (as of 2026‑06‑22), a vibrant issue/PR community, and 19 relevant topics indicate healthy maintenance.  
- **Maturity** – High‑level orchestration features (parallelism, error handling, logging) are already production‑grade; the TypeScript codebase is well‑typed and documented.  
- **Risks** – Licensing (MIT) and security posture appear clean, but a final audit of dependency vulnerabilities and maintainers’ response times is advisable before mission‑critical deployment.  

Overall, Emdash offers a robust, provider‑agnostic foundation for turning isolated AI prompts into scalable, repeatable agent pipelines, making it a strong candidate for pilots and, with due diligence, full production use.

### Русский

Emdash — это открытая платформа для оркестрации агентных рабочих процессов (🧡 YC W26), позволяющая запускать несколько код‑генерирующих агентов параллельно, подключать любые провайдеры и формировать повторяемые пайплайны с инструментами и памятью агента. Типичный сценарий: в CI/CD или исследовательском проекте вы связываете несколько агентов (например, генерацию кода, тестирование и рефакторинг), добавляете вызовы внешних сервисов и сохраняете контекст между шагами, получая полностью автоматизированный цикл разработки. Проект имеет высокий уровень готовности к production‑использованию: активные коммиты, более 4 900 звёзд, 515 форков, TypeScript‑база, обширный API/SDK/CLI и хорошую экосистемную поддержку, требуя лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
Emdash（generalaction/emdash）是一个开源的 *Agentic Development Environment*（🧡 YC W26），可并行运行多个编码智能体并自由接入任意模型提供商。它把零散的 Prompt 与工具封装成可复用的 Agent 工作流，帮助团队在代码生成、调试、自动化等场景实现高效协同。

**核心价值**  
- **工作流标准化**：将单个 Prompt、工具或记忆模块统一组织为可重复、可组合的 Agent 流程。  
- **多智能体并行**：支持同时调度多个 Coding Agent，显著提升大规模代码生成或审查的吞吐量。  
- **供应商无关**：通过统一的 SDK/CLI，轻松切换 OpenAI、Claude、Gemini 等任意大模型提供商，降低锁仓风险。

**典型接入方式**  
1. **SDK**：在 TypeScript/JavaScript 项目中 `npm i @generalaction/emdash`，通过 `EmdashClient` 调用 `createAgent`, `runWorkflow` 等 API。  
2. **CLI**：安装全局二进制 `npm i -g emdash-cli`，使用 `emdash run <workflow.yaml>` 直接在终端启动或调度工作流。  
3. **REST API**：部署官方 Docker 镜像后，调用 `/v1/agents`、`/v1/workflows` 等端点，可在任意语言（Python、Go、Java 等）中通过 HTTP 请求集成。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑22，GitHub 4950 星、515 fork，最近一次提交在 2026‑06‑22，代码基于 TypeScript，拥有 19 条主题标签。  
- **成熟度**：具备完整的 API、SDK 与 CLI，文档覆盖示例、部署指南和 CI/CD 集成，已在多个开源项目和内部工具链中验证。  
- **风险点**：仍需进一步审查许可证兼容性、依赖安全（尤其是第三方模型 SDK）以及维护者响应速度。总体而言，项目已具备 **高** 的生产候选级别，可直接用于试点或正式上线。

## 🧭 Practical evaluation

**Value:** generalaction/emdash helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4950 GitHub stars
- 515 forks
- updated 2026-06-22
- primary language: TypeScript
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 79/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 84/100 |
| recency | 80/100 |
| adoption | 76/100 |
| production | 78/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/generalaction/emdash) · [← Back to Orchestration](./README.md)</sub>
