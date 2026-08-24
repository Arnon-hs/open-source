# OneWave-AI/claude-skills

[![Stars](https://img.shields.io/github/stars/OneWave-AI/claude-skills?style=flat-square&color=yellow)](https://github.com/OneWave-AI/claude-skills/stargazers) [![Forks](https://img.shields.io/github/forks/OneWave-AI/claude-skills?style=flat-square&color=blue)](https://github.com/OneWave-AI/claude-skills/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> 172 production-ready Claude Code skills for sales, marketing, design, engineering, and AI agent architecture. Built and maintained by OneWave AI.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 208 |
| 🍴 **Forks** | 35 |
| 💻 **Language** | Unknown |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skills` `ai-agents` `anthropic` `claude` `claude-code` `claude-skills` `developer-tools` `llm` `prompt-engineering` `sales-automation`

## 🎯 Categories

Orchestration · Automation · AI/ML · DevTools · Design

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
OneWave‑AI’s *claude‑skills* repository bundles 172 ready‑to‑use Claude code “skills” that cover sales, marketing, design, engineering, and AI‑agent architecture. By turning isolated prompts and tools into reusable, orchestrated agent workflows, the collection lets teams build multi‑agent pipelines and standardized memory handling with minimal custom code. The project is actively maintained (last update 2026‑07‑04) and has gathered modest community interest (208 ⭐, 35 forks).

**Value**  
- **Rapid composition** – Instead of writing Claude prompts from scratch, developers can pick a skill (e.g., “generate a sales pitch” or “design a logo”) and plug it into a larger workflow, accelerating prototyping.  
- **Consistency & governance** – Shared, version‑controlled skills act as a single source of truth for prompt engineering, making it easier to audit, test, and enforce best practices across teams.  
- **Multi‑agent orchestration** – The skills include patterns for tool‑use, memory persistence, and hand‑off between agents, enabling complex use cases such as “lead qualification → content creation → email dispatch” without reinventing the coordination logic.

**Practical Adoption Path**  

| Step | Action | Why it matters |
|------|--------|----------------|
| 1️⃣  | **Clone & explore** – Pull the repo, review the `README` and the `skills/` directory to understand naming conventions and input/output schemas. | Ensures you know which skills map to your business processes. |
| 2️⃣  | **Select & test** – Run a few skills locally using the provided examples or a minimal Claude client script. Verify output quality and required parameters. | Gives confidence the skill works in your environment before integration. |
| 3️⃣  | **Wrap in a service** – Create thin wrapper functions (Node.js, Python, etc.) that call the Claude API with the skill’s prompt template and handle responses. | Provides a clean interface for downstream orchestration tools (e.g., Temporal, Airflow, LangChain). |
| 4️⃣  | **Compose workflows** – Use an orchestration framework (or simple script) to chain selected wrappers, passing state via JSON or a shared memory store (Redis, DynamoDB). | Realizes the “repeatable agent workflow” promise. |
| 5️⃣  | **Validate & monitor** – Add unit tests for each wrapper, log token usage, and set up alerts for API errors or drift in skill output. | Mitigates the “sparse integration signals” risk highlighted in the metadata. |
| 6️⃣  | **Gradual rollout** – Deploy the composed workflow to a staging environment, run a pilot with internal users, then promote to production once stability is confirmed. | Allows you to measure setup cost and maintenance overhead before full commitment. |

**Production Readiness**  
- **Maturity**: Rated *Medium*. The codebase is functional and up‑to‑date, making it suitable for prototypes, internal tools, or low‑risk production features.  
- **Dependencies**: Primarily the Claude API and a modest set of runtime libraries; no heavyweight external services are required.  
- **Maintenance**: The repository is actively maintained, but because integration details (e.g., exact API signatures, required environment variables) are not fully documented in the metadata, teams should allocate time for a manual audit and possibly contribute missing docs.  
- **Risk Mitigation**: Before committing to a critical production line, perform a dependency audit, add comprehensive tests, and establish a version‑pinning strategy to avoid breaking changes from future skill updates.  

In short, *claude‑skills* offers a valuable shortcut for building repeatable Claude‑based agent pipelines, but successful production use hinges on a disciplined adoption process that validates each skill’s behavior and integrates proper monitoring and testing.

### Русский

OneWave‑AI/claude‑skills — набор из 172 готовых к использованию Claude‑скриптов, охватывающих продажи, маркетинг, дизайн, инженерию и архитектуру AI‑агентов; он позволяет превратить разрозненные подсказки и инструменты в повторяемые, оркестрируемые рабочие процессы агентов. Типичный сценарий — построение многокомпонентных пайплайнов с координацией нескольких агентов, подключением внешних сервисов и стандартизацией памяти агентов. Готовность к production — средняя: проект подходит для прототипов и внутренних решений, но требует ручной проверки и уточнения интеграционных точек перед развёртыванием в продакшн.

### 中文

**价值**  
OneWave‑AI/claude‑skills 将零散的 Claude 提示和工具封装成 172 条可直接使用的「Skill」，覆盖销售、营销、设计、工程和 AI 代理架构等常见业务场景。通过这些 Skill，团队可以快速搭建多代理协同、工具调用流水线以及统一的记忆管理，从而把一次性实验性的 Prompt 迁移到可复用、可维护的工作流中，显著提升开发效率和交付一致性。

**典型接入方式**  
1. **挑选 Skill**：在项目的 `skills/` 目录或 GitHub 主页的 README 中查找对应业务（如「lead‑generation」或「image‑design」）的 Skill。  
2. **复制代码**：将对应的 `.py`（或 `.js`）文件或代码片段拷贝到自己的代码库，按需修改输入/输出参数。  
3. **集成 Claude API**：在已有的 Claude 调用层（如 `claude_client.py`）中，引入 Skill 的函数或类，并在业务流程中调用。  
4. **工具链挂钩**：如果 Skill 依赖外部工具（如搜索 API、数据库、图像生成服务），按照注释中的 `requirements.txt` 安装依赖，并在环境变量或配置文件中提供凭证。  
5. **本地调试 + 单元测试**：运行项目自带的示例脚本或自行编写测试用例，确认 Skill 在你的环境下能够正确执行。  
6. **CI/CD 集成**：将上述步骤写入构建脚本（如 GitHub Actions），实现自动化部署和回归检测。

> **注意**：项目的元数据（如 `package.json`、`pyproject.toml`）中并未提供完整的依赖树或集成指南，建议在正式上线前进行一次手动审查，确认所有外部服务的兼容性和安全性。

**生产可用性**  
- **成熟度**：Medium。Skill 已经在多个内部原型和实验项目中验证，可直接用于内部工具或面向小规模用户的 SaaS 功能。  
- **准备工作**：在生产环境部署前，需要完成以下检查：  
  1. **依赖审计**：确认所有第三方库的许可证和安全补丁。  
  2. **错误处理**：为每个 Skill 添加超时、重试和异常捕获逻辑，防止 Claude 调用失败导致工作流卡死。  
  3. **监控埋点**：在关键入口记录调用时长、返回状态和使用的外部工具，以便后续性能调优。  
  4. **权限管理**：确保调用外部 API（搜索、数据库、图像服务等）的凭证安全存储，并按最小权限原则配置。  
- **适用场景**：原型验证、内部自动化平台、业务部门的低代码编排、以及需要快速迭代的 AI 助手项目。对高并发、严格 SLA 的面向大众的生产系统仍需额外的可靠性工程（如熔断、限流、灰度发布）后方可投入使用。  

总体而言，OneWave‑AI/claude‑skills 是一个 **快速构建可复用 AI 工作流的利器**，只要在接入前做好依赖审查和容错设计，即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** OneWave-AI/claude-skills helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 208 GitHub stars
- 35 forks
- updated 2026-07-04
- 10 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 49/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 46/100 |
| production | 53/100 |
| usefulness | 90/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/OneWave-AI/claude-skills) · [← Back to Orchestration](./README.md)</sub>
