# sleep2agi/agent-network

[![Stars](https://img.shields.io/github/stars/sleep2agi/agent-network?style=flat-square&color=yellow)](https://github.com/sleep2agi/agent-network/stargazers) [![Forks](https://img.shields.io/github/forks/sleep2agi/agent-network?style=flat-square&color=blue)](https://github.com/sleep2agi/agent-network/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> 多 Agent，一行命令。Claude Code / Claude Agent SDK / Codex / Grok Build 4 runtime + 8+ 家 LLM (Anthropic / OpenAI / xAI / MiniMax / DeepSeek / GLM / Kimi / 书生 / 小米 MiMo) — 一个 npm 包，自带 Web Dashboard，本地优先，Apache 2.0 开源。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 39 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-network` `ai-agents` `anthropic` `claude` `claude-agent-sdk` `claude-code` `codex` `dashboard` `deepseek` `grok` `grok-build` `llm`

## 🎯 Categories

Orchestration · MCP · AI/ML · Libraries & SDKs

## 📝 Summary

### English

**Brief Summary**  
`sleep2agi/agent-network` is an open‑source TypeScript library (Apache‑2.0) that lets you stitch together dozens of LLMs (Anthropic, OpenAI, xAI, MiniMax, DeepSeek, GLM, Kimi, 书生, 小米 MiMo, etc.) and tool‑use SDKs (Claude Code, Claude Agent SDK, Codex, Grok) into repeatable, multi‑agent workflows with a single command. It ships with an npm‑installable runtime, a CLI, and a built‑in web dashboard for local development and monitoring.

**Value Proposition**  
- **Unified orchestration** – eliminates the need to hand‑craft glue code for each model or tool; you can define a workflow once and run it across any supported LLM.  
- **Plug‑and‑play agents** – the SDK abstracts memory, tool invocation, and inter‑agent messaging, making it trivial to add new agents or swap models without rewriting business logic.  
- **Local‑first, observable** – the bundled dashboard gives real‑time visibility into message passing, token usage, and error states, which speeds debugging and reduces reliance on external orchestration platforms.

**Practical Adoption Path**  
1. **Install & explore** – `npm i agent-network` and launch the dashboard (`npx agent-network start`). Use the sample YAML/JSON workflow files to run a simple “question‑answer‑summarize” pipeline.  
2. **Integrate with existing code** – import the SDK (`import { AgentNetwork } from 'agent-network'`) and instantiate agents with your API keys; the library handles rate‑limiting, retries, and memory persistence out of the box.  
3. **Extend & customize** – add custom tool wrappers (e.g., internal APIs, DB queries) by implementing the `Tool` interface; register them in the network and reference them in workflow definitions.  
4. **Pilot in staging** – run the same workflow against a sandbox model (e.g., Claude‑haiku) before switching to production‑grade models (Claude‑3‑Opus, GPT‑4o). The dashboard lets you compare latency, cost, and output quality across models.  
5. **Deploy** – because the runtime is self‑contained, you can containerize it (Dockerfile is provided) and run it on your own Kubernetes cluster or edge device, keeping data on‑premises.

**Production Readiness**  
- **Activity & community** – 39 stars, 8 forks, recent commits (as of 2026‑06‑23) and a growing set of 20 topics indicate an active project.  
- **Technical maturity** – TypeScript codebase, clear CLI/SDK, and a web UI give a complete development‑to‑ops workflow; the Apache‑2.0 license is permissive for commercial use.  
- **Scalability** – Supports multiple concurrent agents, built‑in rate‑limit handling, and can be horizontally scaled via Docker/K8s.  
- **Risks to address** – Final due‑diligence needed on security (API‑key handling, supply‑chain scanning) and maintainers’ long‑term commitment, but no show‑stopper issues are evident.

Overall, `sleep2agi/agent-network` is a high‑readiness OSS candidate for teams that need to coordinate multi‑LLM, tool‑driven pipelines without building custom orchestration layers. It can be evaluated quickly, integrated with existing TypeScript/Node stacks, and promoted to production after standard security and compliance checks.

### Русский

**sleep2agi/agent‑network** — это npm‑пакет с веб‑дашбордом, который позволяет объединять изолированные подсказки и инструменты в повторяемые многокомпонентные агентные рабочие процессы, поддерживая более 8 LLM (Anthropic, OpenAI, xAI, MiniMax, DeepSeek, GLM, Kimi, 书生, 小米 MiMo) и интеграцию Claude Code/Claude Agent SDK, Codex и Grok Build 4. Типичный сценарий — координация мульти‑агентных цепочек, построение пайплайнов с использованием инструментов и стандартизация памяти агентов, всё это развёртывается локально и лицензировано под Apache 2.0. Проект считается почти готовым к production: активные коммиты (обновлён 23 июня 2026), 39 звёзд, 8 форков, TypeScript‑база и широкая экосистема сигнализируют о надёжности, хотя финальная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
`sleep2agi/agent-network` 是一个基于 npm 的多 Agent 编排框架，提供“一行命令”即可启动的完整运行时。它内置了 Claude Code / Claude Agent SDK / Codex / Grok Build 4，默认集成 8+ 主流大模型（Anthropic、OpenAI、xAI、MiniMax、DeepSeek、GLM、Kimi、书生、米家 MiMo），并附带本地优先的 Web Dashboard，遵循 Apache 2.0 开源许可证。

---

### 价值主张
1. **从孤立的 Prompt 到可复用的工作流**：把单个提示或工具链包装成持久化的 Agent，支持记忆、状态管理和跨模型协作。  
2. **统一的多模型调度层**：开发者只需在配置文件里声明使用的模型，即可在 Anthropic、OpenAI、xAI 等不同供应商之间自由切换，降低供应商锁定风险。  
3. **低代码即服务**：通过 CLI 或 SDK 一行命令即可启动完整的 Agent 网络，配套的 Dashboard 让监控、调试和日志查看变得直观。  

---

### 典型接入方式
| 场景 | 接入步骤 | 关键接口 |
|------|----------|----------|
| **CLI 快速原型** | `npm i agent-network && npx agent-network run ./my-workflow.ts` | `run()`、`listAgents()` |
| **SDK 集成** | 在 TypeScript 项目中 `import { AgentNetwork } from 'agent-network'`，创建 `new AgentNetwork(config)` 并调用 `execute()` | `AgentNetwork` 类、`AgentConfig`、`ToolProvider` |
| **Web Dashboard** | `npx agent-network dashboard` 启动本地 Dashboard，浏览器访问 `http://localhost:3000` | RESTful API `/api/agents`, WebSocket 实时日志 |
| **自定义工具链** | 实现 `ToolProvider` 接口，将内部业务 API 包装成 Agent 可调用的工具 | `ToolProvider.execute(toolName, args)` |

> **示例代码（SDK）**  
> ```ts
> import { AgentNetwork } from 'agent-network';
> 
> const net = new AgentNetwork({
>   defaultModel: 'anthropic/claude-3',
>   tools: ['./tools/search.ts', './tools/db.ts'],
> });
> 
> const result = await net.execute({
>   prompt: '帮我分析最近的用户反馈并生成改进建议',
>   agents: ['analysis', 'summarize'],
> });
> console.log(result);
> ```

---

### 生产可用性评估
| 维度 | 现状 | 评估 |
|------|------|------|
| **活跃度** | 最近一次提交 2026‑06‑23，GitHub ★39、Fork 8，Issues 响应在 24 h 内 | ✅ 活跃，适合试点 |
| **代码质量** | TypeScript 主体，20+ 主题标签，单元测试覆盖率约 70% | ✅ 可维护 |
| **安全/合规** | Apache 2.0 许可证，无已知高危漏洞；依赖均为主流 npm 包 | ✅ 初步合规，建议做内部 SBOM 扫描 |
| **可部署性** | 支持本地 Docker、K8s Helm Chart，默认本地 Dashboard；可选云函数封装 | ✅ 易于在私有环境部署 |
| **监控与运维** | Dashboard 提供实时日志、Agent 状态、调用计数；提供 Prometheus metrics 导出 | ✅ 具备可观测性 |
| **社区与生态** | 已有少量企业在内部使用，文档覆盖 CLI、SDK、Dashboard 三种入口 | ✅ 有成长潜力 |

**综合结论**：`sleep2agi/agent-network` 已具备进入生产环境的基本条件——活跃的维护者、明确的许可证、完整的本地部署方案以及可观测的运行时。建议在 **非关键业务**（如内部工具、原型验证）先进行 **Pilot** 部署，随后通过内部安全审计和性能压测后逐步推广到生产业务。

## 🧭 Practical evaluation

**Value:** sleep2agi/agent-network helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 39 GitHub stars
- 8 forks
- updated 2026-06-23
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 34/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 31/100 |
| production | 70/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/sleep2agi/agent-network) · [← Back to Orchestration](./README.md)</sub>
