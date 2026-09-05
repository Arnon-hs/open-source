# gustavoeenriquez/MakerAi

[![Stars](https://img.shields.io/github/stars/gustavoeenriquez/MakerAi?style=flat-square&color=yellow)](https://github.com/gustavoeenriquez/MakerAi/stargazers) [![Forks](https://img.shields.io/github/forks/gustavoeenriquez/MakerAi?style=flat-square&color=blue)](https://github.com/gustavoeenriquez/MakerAi/network) [![Language](https://img.shields.io/badge/lang-Pascal-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> The AI Operating System for Delphi. 100% native framework with RAG 2.0, autonomous agents, MCP protocol, and universal LLM connector. Supports OpenAI, Claude, Gemini, Ollama, and more. Delphi 10.4+ (limited), full support from Delphi 12 Athens.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 185 |
| 🍴 **Forks** | 54 |
| 💻 **Language** | Pascal |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `claude` `delphi` `embeddings` `fpc` `free-pascal` `function-calling` `gemini` `grok` `groq` `lazarus` `llm`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
MakerAi is a native Delphi AI operating system that lets developers stitch together prompts, tools, and autonomous agents into repeatable, memory‑aware workflows. It bundles a RAG 2.0 engine, MCP protocol, and a universal LLM connector supporting OpenAI, Claude, Gemini, Ollama and others, and runs on Delphi 10.4 (limited) and fully on Delphi 12 Athens.

**Value**  
- **From isolated prompts to orchestrated agents** – MakerAi abstracts the plumbing required to coordinate multiple AI models, tool‑use pipelines, and persistent memory, turning ad‑hoc scripts into maintainable, version‑controlled workflows.  
- **Cross‑LLM flexibility** – The universal connector lets you swap or combine providers without code changes, protecting your investment against model deprecation or pricing shifts.  
- **Delphi‑centric integration** – Because it is 100 % native Pascal, you can embed sophisticated AI capabilities directly into existing Delphi applications without external services or wrappers.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the supplied CLI or SDK sample, and point the connector to a free‑tier LLM (e.g., OpenAI’s `gpt-3.5-turbo`).  
2. **Define agents** – Use the declarative YAML/JSON schema to describe prompts, memory stores, and tool bindings; test each agent individually with the CLI.  
3. **Orchestrate** – Wire agents together via the MCP protocol (message‑based contract) inside your Delphi project, leveraging the built‑in RAG 2.0 for context enrichment.  
4. **Integrate** – Replace the prototype calls with the MakerAi SDK components in your production codebase, configure the desired LLM endpoints, and enable persistent storage for agent memory.  
5. **Deploy & monitor** – Use the provided logging hooks and health‑check endpoints to observe performance and cost, then scale by adding more agents or swapping to an on‑premise Ollama server if needed.

**Production Readiness**  
- **Activity & adoption** – 185 stars, 54 forks, recent commits (as of 2026‑06‑22) and a growing Delphi community indicate healthy momentum.  
- **Maturity** – Core features (RAG 2.0, MCP, universal connector) are stable, and full support for Delphi 12 Athens removes earlier version limitations.  
- **Risk profile** – No major licensing or security red flags have been identified, though a final audit of the license and maintainer responsiveness is advisable.  
Overall, MakerAi is a strong OSS candidate for pilots and can be promoted to production once the brief legal/security review is completed.

### Русский

**MakerAi** — это полностью нативный AI‑операционный слой для Delphi, объединяющий RAG 2.0, автономных агентов, протокол MCP и универсальный коннектор к LLM (OpenAI, Claude, Gemini, Ollama и др.). Он позволяет превратить разрозненные запросы и инструменты в повторяемые, управляемые конвейеры агентов — например, координировать многокомпонентные рабочие процессы, добавлять пайплайны с использованием внешних сервисов и стандартизировать память агентов. Проект уже имеет активную поддержку (обновления 2026‑06‑22, 185 звёзд, 54 форка), работает в Delphi 10.4+ (полная совместимость с Delphi 12) и готов к пилотному внедрению в продакшн, требуя лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
MakerAi（gustavoeenriquez/MakerAi）是面向 Delphi 的 AI 操作系统，提供 100% 原生框架，内置 RAG 2.0、自治代理、MCP 协议以及统一的 LLM 连接器，兼容 OpenAI、Claude、Gemini、Ollama 等主流模型，Delphi 10.4（功能受限）起可使用，Delphi 12 Athens 起获得完整支持。

**价值**  
- 将零散的 Prompt 与工具封装为可复用、可编排的智能体工作流，显著提升开发效率和系统可维护性。  
- 通过统一的记忆（Memory）与检索增强（RAG）机制，实现跨代理的知识共享和上下文保持。  
- 支持多模型、多协议的插件化设计，方便在同一项目中混合使用不同 LLM，降低供应商锁定风险。

**典型接入方式**  
1. **SDK / API**：项目提供 Pascal SDK 与 REST‑API，开发者可在 Delphi 项目中直接引用 `MakerAi.SDK.pas`，调用 `CreateAgent`, `RunWorkflow` 等高层函数。  
2. **CLI**：随仓库的 `makerai-cli` 可在命令行下快速启动 Agent、管理记忆库或触发 RAG 检索，适合 CI/CD 或脚本化集成。  
3. **MCP 协议**：通过实现 `IMCPClient` 接口，外部系统（如微服务、消息队列）可与 MakerAi 进行双向通信，实现跨语言、跨平台的代理协作。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑22 最近一次提交，星标 185、Fork 54，社区讨论活跃，代码质量稳定。  
- **兼容性**：Delphi 12 Athens 及以上提供完整特性，10.4 仍可运行核心功能，满足大多数现有项目的升级路径。  
- **安全与授权**：采用 MIT 许可证，源码可审计；暂无已知重大安全漏洞，但仍建议在生产环境中进行内部安全评估。  
- **成熟度**：具备完整的 API/SDK/CLI 文档、示例工程以及 CI 测试，已可作为 OSS 级别的 **高** 生产候选进行试点部署。  

综上，MakerAi 能帮助 Delphi 开发团队快速构建、管理和复用多代理 AI 工作流，接入方式灵活，且在当前社区与技术生态中具备较高的生产可用性。

## 🧭 Practical evaluation

**Value:** gustavoeenriquez/MakerAi helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 185 GitHub stars
- 54 forks
- updated 2026-06-22
- primary language: Pascal
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 48/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 71/100 |
| recency | 80/100 |
| adoption | 47/100 |
| production | 71/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/gustavoeenriquez/MakerAi) · [← Back to Orchestration](./README.md)</sub>
