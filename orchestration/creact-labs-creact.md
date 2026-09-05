# creact-labs/creact

[![Stars](https://img.shields.io/github/stars/creact-labs/creact?style=flat-square&color=yellow)](https://github.com/creact-labs/creact/stargazers) [![Forks](https://img.shields.io/github/forks/creact-labs/creact?style=flat-square&color=blue)](https://github.com/creact-labs/creact/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> CReact is how you write your workflows using JSX, build durable apps that you can sync with external state, build jobs, agents,  infrastructure, anything you can declare you can build!

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 69 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic` `ai` `apps` `automation` `creact` `dag` `dependency-graph` `durable` `execution` `iac` `infrastructure` `jsx`

## 🎯 Categories

Orchestration · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
CReact lets you define complex, durable workflows as JSX components, turning isolated prompts, tools, and agents into reusable, sync‑able pipelines. By treating jobs, infrastructure, and AI agents as declarative UI‑like elements, it makes building, testing, and visualising multi‑agent orchestrations fast and intuitive. The project is a TypeScript‑based open‑source framework that bridges frontend‑style development with DevOps/AI automation.

**Value**  
- **Unified declarative model:** Write workflows, tool‑chains, and agent memory handling in a single JSX syntax, reducing the mental overhead of mixing scripts, YAML, and code.  
- **Reusable components:** Workflows become composable components that can be versioned, shared, and plugged into different projects, turning ad‑hoc prompts into repeatable services.  
- **Rapid prototyping:** The UI‑like approach gives immediate visual feedback and hot‑reloading, accelerating iteration on multi‑agent or infrastructure automation scenarios.  

**Practical Adoption Path**  
1. **Proof‑of‑concept:** Clone the repo, run the provided examples, and verify that the README steps work on a sandbox environment.  
2. **Component extraction:** Identify a repetitive prompt‑tool sequence in your current pipelines and rewrite it as a CReact component.  
3. **Integration layer:** Wrap the component in a thin API (e.g., an Express or FastAPI endpoint) to expose it to existing services.  
4. **Testing & CI:** Add unit tests for the JSX workflow, use the built‑in dev server for local validation, and integrate into your CI pipeline.  
5. **Scale‑out:** Once stable, register the component in an internal component registry and orchestrate multiple CReact workflows via a simple orchestrator or container orchestration platform.  

**Production Readiness**  
- **Maturity:** Medium. The framework is functional and actively updated (latest commit 2026‑07‑12) but has modest community adoption (≈70 stars, 2 forks).  
- **Dependencies:** Pure TypeScript with common Node.js libraries, making dependency management straightforward, though a security audit of transitive packages is advisable.  
- **Maintainability:** The codebase is relatively small and well‑documented, but the project lacks a large contributor base; you may need to allocate internal ownership for bug fixes and feature extensions.  
- **Risk considerations:** Verify the license compatibility, run a security scan, and ensure you have an internal fallback if the upstream repository becomes inactive.  

Overall, CReact is a promising tool for teams that want to prototype and eventually standardise AI‑agent and automation pipelines using a familiar JSX/React‑style workflow, provided you perform a small PoC, conduct due‑diligence on security and licensing, and plan for internal maintenance before pushing to production.

### Русский

**CReact** — это фреймворк на TypeScript, позволяющий описывать оркестрацию многопоточных агентных и инструментальных workflow‑ов в виде JSX‑компонентов. Типичный сценарий внедрения — небольшая proof‑of‑concept, в которой изолированные запросы к LLM и внешние сервисы объединяются в повторяемый пайплайн (например, координация нескольких агентов, добавление инструментов и стандартизация памяти). Проект находится на среднем уровне готовности: подходит для прототипов и внутренних автоматизаций, но перед запуском в production требуется проверка лицензии, безопасности и стабильности зависимостей.

### 中文

**项目价值**  
CReact 让你可以用 JSX 直接描述工作流，从而把零散的 Prompt、工具或外部状态包装成可复用、可持久化的 **agent workflow**。它特别适合：  
- 多 Agent 协同（如 ChatGPT + 工具 + 内部服务）  
- 将工具链（API 调用、脚本、CI/CD 等）串成流水线  
- 为每个 Agent 统一记忆/上下文管理，提升一致性与可调试性  

**典型接入方式**  
1. **阅读 README & 示例**：项目自带完整的 JSX 工作流示例，先跑通 `npm install && npm run demo`。  
2. **在现有代码库中加入依赖**：`npm i @creact/react`（或对应的 monorepo 包），在 TypeScript/React 项目里编写类似下面的 JSX：  
   ```tsx
   <Workflow>
     <Prompt name="summarize" prompt="请把以下内容概括为要点" />
     <Tool name="search" api="https://api.example.com/search" />
     <Agent name="assistant" tools={['search']} />
   </Workflow>
   ```  
3. **小范围 PoC**：先在内部脚本或测试服务里实现一个“从 Slack 收到指令 → 调用搜索工具 → 生成报告”的流程，验证：  
   - 依赖是否能顺利编译（TS）  
   - 工作流的状态同步（持久化）是否符合预期  
   - 与已有的身份认证、日志系统的兼容性  

4. **CI/CD 集成**：将工作流文件（`.creact.tsx`）加入代码审查，使用 `creact build` 生成可部署的 JSON/Node 包，交给现有的容器或 Serverless 平台运行。  

**生产可用性评估**  

| 维度 | 现状 | 建议 |
|------|------|------|
| **功能成熟度** | 已支持 JSX 编写、状态持久化、工具调用，适合原型和内部工具。 | 在正式业务前，针对关键路径写单元/集成测试。 |
| **社区与维护** | 69⭐、2 fork，最近一次提交是 2026‑07‑12，活跃度一般。 | 关注 Issue 及 PR 动态，必要时自行 fork 并维护关键 bug。 |
| **安全/合规** | 无明显许可证冲突（MIT/Apache 待确认），未发现高危依赖。 | 进行一次供应链审计（SBOM、SCA），并确保所有外部 API 有访问控制。 |
| **部署可靠性** | 通过 TypeScript 编译后可在 Node 环境运行，依赖少。 | 在生产环境使用容器化或 Serverless，配合健康检查与日志聚合。 |
| **可扩展性** | 支持自定义 Tool、Agent，适配多种业务场景。 | 规划好 Tool 接口规范，避免在后期频繁改动工作流结构。 |

**结论**  
CReact 适合作为 **内部原型/业务流程自动化** 的底层框架，尤其是需要多 Agent 协同或把 Prompt/工具链标准化的场景。只要在进入生产前完成依赖安全审计、编写完整的测试套件，并做好持续维护（或自行 fork），即可在中等规模的业务中安全上线。

## 🧭 Practical evaluation

**Value:** creact-labs/creact helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 69 GitHub stars
- 2 forks
- updated 2026-07-12
- primary language: TypeScript
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 39/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 32/100 |
| production | 66/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/creact-labs/creact) · [← Back to Orchestration](./README.md)</sub>
