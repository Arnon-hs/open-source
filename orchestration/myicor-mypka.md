# myICOR/myPKA

[![Stars](https://img.shields.io/github/stars/myICOR/myPKA?style=flat-square&color=yellow)](https://github.com/myICOR/myPKA/stargazers) [![Forks](https://img.shields.io/github/forks/myICOR/myPKA?style=flat-square&color=blue)](https://github.com/myICOR/myPKA/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> AI-powered Personal Knowledge Assistance in a folder. Built on the ICOR methodology. Plain markdown. Any LLM. Yours forever.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 241 |
| 🍴 **Forks** | 68 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic` `ai-agents` `ai-team` `claude-code` `claude-cowork` `cursor` `gemini-cli` `icor` `knowledge-management` `local-first` `logseq-alternative` `markdown`

## 🎯 Categories

Orchestration · AI/ML · Documents · Productivity · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
myICOR / myPKA is an open‑source, TypeScript‑based framework that lets you embed an AI‑powered personal knowledge assistant directly into a folder, using the ICOR methodology and any LLM of your choice. It converts isolated prompts and tools into repeatable, orchestrated agent workflows, exposing a clean API/SDK/CLI for easy integration. With active maintenance, 241 ★ on GitHub and strong ecosystem signals, it’s ready for serious pilot projects.  

**Value**  
- **Workflow orchestration:** Turns ad‑hoc prompts into durable pipelines, letting multiple agents share memory, invoke tools, and coordinate actions without custom glue code.  
- **Flexibility:** Works with any LLM (OpenAI, Anthropic, local models) and can be driven from plain markdown, making it language‑agnostic for downstream teams.  
- **Developer productivity:** Provides ready‑made APIs, SDKs and a CLI, so teams can focus on domain logic rather than building prompt‑management infrastructure.

**Practical Adoption Path**  
1. **Prototype:** Clone the repo, run the CLI to spin up a local instance, and point it at a markdown file that defines a simple knowledge‑assistant use‑case.  
2. **Integrate:** Replace the placeholder LLM with your preferred model via the provided API configuration; hook into existing CI/CD pipelines using the TypeScript SDK.  
3. **Scale:** Deploy the service as a container (Docker/K8s) and connect it to your internal toolchain (e.g., ticketing, search, or monitoring APIs) to build multi‑agent pipelines.  
4. **Govern:** Use the built‑in observability hooks to log agent actions, memory updates, and tool calls for audit and debugging.

**Production Readiness**  
- **Activity & Adoption:** Recent commits (as of 2026‑06‑22), 241 ★, 68 forks, and 20 relevant topics indicate a healthy community.  
- **Architecture:** Clear API/SDK/CLI surface, TypeScript codebase, and modular design make it straightforward to embed in existing stacks.  
- **Readiness Level:** Rated “high” for OSS candidates; suitable for a pilot in a controlled environment and, after standard security/license review, can be promoted to production.  
- **Remaining Checks:** Confirm licensing compatibility, perform a security audit of dependencies, and verify that maintainers are still actively responding to issues before full‑scale rollout.

### Русский

myICOR / myPKA — это open‑source система персонального помощника знаний, которая превращает разрозненные подсказки и инструменты в повторяемые агентные рабочие потоки на основе методологии ICOR. Типичный сценарий: встраивание в существующий проект через API/SDK/CLI для организации многокомпонентных LLM‑агентных пайплайнов, управления инструментами и стандартизации памяти агентов. Проект находится в высокой готовности к production: активные коммиты, 241 звезда, 68 форков, поддержка TypeScript и обширная экосистема делают его надёжным кандидатом для пилотных внедрений.

### 中文

**项目简介**  
myICOR/myPKA 是一个基于 ICOR 方法论的 AI 驱动个人知识助理，所有内容以纯 Markdown 存放，可自由接入任意大语言模型（LLM），并以开源方式长期维护。

**价值主张**  
- **把碎片化的 Prompt 与工具串联**：将单独的提示、脚本或外部工具包装成可复用的 Agent 工作流，提升效率并降低出错率。  
- **多 Agent 编排**：支持在同一文件夹内协调多个 Agent 的协作，轻松实现复杂的多步骤任务。  
- **标准化记忆与工具链**：提供统一的记忆模型和工具调用约定，帮助团队在不同项目间共享经验与实现。  

**典型接入方式**  
1. **API/SDK**：通过项目提供的 HTTP API 或 TypeScript SDK 调用工作流入口，传入上下文即得到执行结果。  
2. **CLI**：使用内置的命令行工具在本地或 CI 环境快速触发指定的 Prompt/Workflow。  
3. **语言元数据**：在 Markdown 文件头部声明使用的 LLM、所需工具或上下文标签，系统会自动解析并加载对应实现。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑22，仓库拥有 241 ⭐、68 🍴，最近一次提交在同一天，表明项目仍在积极维护。  
- **技术成熟**：核心使用 TypeScript 编写，提供完整的类型定义，易于在现有前端/后端代码库中集成。  
- **生态兼容**：公开的 API/SDK、CLI 与常见的 LLM（OpenAI、Claude、Gemini 等）均可对接，且支持自定义模型。  
- **风险点**：需要进一步审查许可证细节、依赖的安全漏洞以及维护者的长期可用性；但就当前信号来看，已具备在生产环境中进行试点的条件。

## 🧭 Practical evaluation

**Value:** myICOR/myPKA helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 241 GitHub stars
- 68 forks
- updated 2026-06-22
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 51/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 49/100 |
| production | 71/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/myICOR/myPKA) · [← Back to Orchestration](./README.md)</sub>
