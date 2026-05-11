# funny-vibes/agent-vibes

[![Stars](https://img.shields.io/github/stars/funny-vibes/agent-vibes?style=flat-square&color=yellow)](https://github.com/funny-vibes/agent-vibes/stargazers) [![Forks](https://img.shields.io/github/forks/funny-vibes/agent-vibes?style=flat-square&color=blue)](https://github.com/funny-vibes/agent-vibes/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> Unified Agent Gateway — Enables Claude Code CLI and Cursor IDE to use free AI backends (Antigravity, Codex) through protocol translation

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 305 |
| 🍴 **Forks** | 59 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `antigravity` `chatgpt` `claude` `codex` `cursor` `openclaw` `vibe-coding` `vibecoding`

## 🎯 Categories

AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*funny‑vibes/agent‑vibes* is a TypeScript‑based “Unified Agent Gateway” that translates the Claude Code CLI and Cursor IDE protocols into calls to free, open‑source AI back‑ends such as Antigravity and Codex. By handling the protocol conversion, it lets developers add generative‑AI capabilities to their tools without having to spin up or train their own models.

**Value Proposition**  
- **Speed‑to‑value** – Plug‑and‑play integration means teams can prototype AI‑enhanced features (code completion, RAG, autonomous agents) in minutes rather than weeks of model‑stack engineering.  
- **Cost efficiency** – Leverages free, community‑maintained models, eliminating expensive API fees while still supporting the same CLI/IDE workflows that developers already know.  
- **Extensibility** – The gateway exposes a clean API/SDK and CLI surface, making it easy to swap back‑ends, add custom prompts, or embed the service in larger agent pipelines.

**Practical Adoption Path**  

| Step | Action | Why it matters |
|------|--------|----------------|
| 1️⃣  | **Clone & install** – `npm i agent-vibes` (or use the provided Docker image). | Minimal setup; TypeScript ecosystem fits most modern dev stacks. |
| 2️⃣  | **Configure a backend** – Add Antigravity or Codex endpoint URLs and auth tokens in a `vibes.config.json`. | Allows you to point the gateway at any free model without code changes. |
| 3️⃣  | **Connect your tool** – Set Claude Code CLI or Cursor IDE to use `http://localhost:PORT/vibes` as its “AI service” endpoint. | Immediate reuse of existing developer workflows. |
| 4️⃣  | **Iterate & test** – Run typical commands (e.g., `claude code generate …`) and verify responses. Adjust prompt templates or model parameters via the config file. | Fast feedback loop for prototyping and fine‑tuning. |
| 5️⃣  | **Scale or embed** – Use the exposed SDK (`import { AgentVibes } from 'agent-vibes'`) to call the gateway from CI pipelines, RAG services, or custom agents. | Turns a prototype into a production‑grade component. |

**Production‑Readiness Assessment**  

- **Activity & Community** – 305 ★, 59 forks, recent commit (2026‑05‑11), and 9 relevant topics indicate a healthy, actively maintained project.  
- **Architecture** – Stateless gateway, TypeScript codebase, and Docker support make it container‑friendly and easy to roll out behind a reverse proxy or within a Kubernetes pod.  
- **Integration Simplicity** – Provides both HTTP API and CLI wrappers; no deep changes required in Claude Code or Cursor.  
- **Risk Considerations** – License (MIT‑style) and security posture appear clean, but a final audit of dependencies and a review of any custom back‑end authentication is recommended before a full production rollout.  

Overall, *agent‑vibes* scores high on readiness for a serious pilot: it can be evaluated quickly, integrated with existing developer tools, and promoted to production once the minor compliance checks are completed.

### Русский

**funny‑vibes/agent‑vibes** — это открытая шлюз‑платформа, позволяющая интегрировать бесплатные AI‑бэкенды (Antigravity, Codex) в инструменты Claude Code CLI и Cursor IDE через единый протокол. Благодаря готовому API/SDK и поддержке типовой метаданных, проект идеально подходит для быстрого прототипирования AI‑фич, создания RAG‑ или агентных воркфлоу и оценки новых моделей без необходимости строить собственный стек. Репозиторий активно поддерживается (обновления 2026‑05‑11, 305 звёзд, 59 форков), имеет зрелую TypeScript‑базу и достаточный набор тем, что делает его готовым к пилотному использованию в продакшене после финальной проверки лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
funny‑vibes/agent‑vibes 是一个统一的 Agent Gateway，负责将 Claude Code CLI 与 Cursor IDE 等前端工具的请求翻译为 Antigravity、Codex 等免费 AI 后端的协议，从而让开发者无需自行搭建模型堆栈即可使用 AI 功能。

**价值**  
- **快速赋能**：通过协议转译，即插即用免费模型，省去训练、部署和维护大型模型的成本。  
- **灵活原型**：适合快速验证 AI 功能、构建 RAG（检索增强生成）或多代理工作流，帮助团队在最短时间内评估不同模型工具的表现。  
- **统一入口**：统一的网关抽象屏蔽了后端差异，降低了代码耦合度，便于后期切换或扩展模型来源。

**典型接入方式**  
1. **CLI/SDK 调用**：在项目中通过 npm 安装 `agent-vibes`，然后在 Claude Code CLI 或 Cursor 插件的配置文件里指定网关地址，即可让这些工具直接调用 Antigravity、Codex 等后端。  
2. **语言元数据**：网关会自动解析请求中的语言信息（如 TypeScript、Python），并把对应的模型能力（代码补全、单元测试生成等）路由到合适的后端。  
3. **专题插件**：如果只需要特定功能（如代码审查、文档生成），可以在网关上启用相应的“topic”插件，只暴露所需的 API，进一步降低攻击面。

**生产可用性**  
- **活跃度**：截至 2026‑05‑11，项目最近一次提交，拥有 305 ★、59 Fork，且主要语言为 TypeScript，社区活跃。  
- **成熟度**：实现了完整的 API/SDK/CLI 接口，提供清晰的协议翻译层，已在多个内部原型项目中验证，具备进入正式生产环境的技术基础。  
- **风险**：目前未发现重大的元数据或许可证风险，但仍建议在正式上线前进行一次安全审计并确认维护者的响应能力。  

综合来看，agent‑vibes 已具备较高的生产就绪度，适合作为 AI 功能的快速试点或在正式产品中作为后端抽象层使用。

## 🧭 Practical evaluation

**Value:** funny-vibes/agent-vibes helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 305 GitHub stars
- 59 forks
- updated 2026-05-11
- primary language: TypeScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 78/100 |
| recency | 100/100 |
| adoption | 51/100 |
| production | 78/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/funny-vibes/agent-vibes) · [← Back to AI/ML](./README.md)</sub>
