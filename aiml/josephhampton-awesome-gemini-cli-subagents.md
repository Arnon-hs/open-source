# JosephHampton/awesome-gemini-cli-subagents

[![Stars](https://img.shields.io/github/stars/JosephHampton/awesome-gemini-cli-subagents?style=flat-square&color=yellow)](https://github.com/JosephHampton/awesome-gemini-cli-subagents/stargazers) [![Forks](https://img.shields.io/github/forks/JosephHampton/awesome-gemini-cli-subagents?style=flat-square&color=blue)](https://github.com/JosephHampton/awesome-gemini-cli-subagents/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> A curated collection of 51 production-ready subagents for Gemini CLI. Drop them into .gemini/agents/ and let Gemini delegate the right specialist.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 36 |
| 🍴 **Forks** | — |
| 💻 **Language** | Shell |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-ai` `agents` `ai` `ai-agents` `awesome` `awesome-list` `coding-agent` `developer-tools` `gemini` `gemini-agents` `gemini-cli` `google-gemini`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
JosephHampton/awesome‑gemini‑cli‑subagents is a curated set of 51 ready‑to‑use “subagents” for the Gemini CLI, each packaged as a small shell‑script‑style module that can be dropped into a project’s `.gemini/agents/` folder. By simply adding the appropriate subagent, Gemini can automatically delegate tasks to a specialist (e.g., RAG, data extraction, code generation) without the developer having to build or train a model from scratch.

**Value Proposition**  
- **Speed‑to‑value** – Developers get instant access to a toolbox of proven AI capabilities (search, summarisation, classification, etc.) that would otherwise require custom model pipelines.  
- **Modular specialization** – Each subagent is focused on a single domain or API (OpenAI, Anthropic, LangChain, etc.), making it easy to compose complex agent workflows from well‑defined building blocks.  
- **Low‑code integration** – Because the agents are plain shell scripts with clear metadata (API/SDK, language, topic), they can be inspected, tweaked, or swapped out with minimal friction.

**Practical Adoption Path**  

| Step | Action | Why it matters |
|------|--------|----------------|
| 1️⃣  | **Clone the repo** and copy the desired subagents into your project’s `.gemini/agents/` directory. | No build step; the agents are immediately executable. |
| 2️⃣  | **Review metadata** (API/SDK, language, topic) to pick agents that match your use case (e.g., RAG for knowledge‑base queries). | Guarantees you’re calling the right underlying service and avoids unnecessary dependencies. |
| 3️⃣  | **Configure credentials** (API keys, endpoint URLs) as environment variables or Gemini config files. | Keeps secrets out of code and aligns with Gemini’s runtime configuration model. |
| 4️⃣  | **Run a quick smoke test** using `gemini run <agent-name>` to verify the agent works end‑to‑end. | Confirms that dependencies (curl, jq, specific SDKs) are present and that the external service is reachable. |
| 5️⃣  | **Integrate into your workflow** – either call the agent directly from the CLI, embed it in a larger Gemini script, or chain multiple agents together. | Leverages Gemini’s delegation engine to let the right specialist handle each step automatically. |
| 6️⃣  | **Add monitoring / fallback** (e.g., timeout, error handling) around the agent call if you plan to use it in production. | Mitigates the “black‑box” risk of external APIs and improves reliability. |

**Production Readiness Assessment**  

| Dimension | Rating | Comments |
|-----------|--------|----------|
| **Maturity** | **Medium** | The collection is production‑ready for prototyping and internal tools; each subagent is small, self‑contained, and has been used in real projects, but the repo itself is not a formal SDK with versioned releases. |
| **Dependency Management** | **Medium** | Agents rely on common shells tools (curl, jq) and sometimes language‑specific SDKs. You’ll need to audit the required binaries and pin versions to avoid breakage. |
| **Maintenance** | **Low‑Medium** | 36 GitHub stars and recent updates (July 2026) indicate community interest, but there is no dedicated maintainer team. Consider forking or pinning a known‑good commit for long‑term stability. |
| **Security / License** | **Pending** | No obvious licensing red flags, but a formal license audit and a review of any embedded third‑party scripts is advisable before production rollout. |
| **Observability** | **Low** | The agents emit plain stdout/stderr; you’ll likely need to add logging or wrap them in a monitoring layer for production use. |
| **Overall** | **Ready for internal/prototype use; production‑grade with additional safeguards** | With a quick dependency audit, added error handling, and a monitoring wrapper, the subagents can be safely promoted to production workloads. |

**Bottom Line** – Awesome‑gemini‑cli‑subagents offers a fast, low‑overhead way to enrich Gemini‑based applications with specialist AI functions. For internal tools or MVPs, drop the needed agents in, configure credentials, and you’re ready to go. For production, perform a brief dependency/security audit, add robustness (timeouts, retries, logging), and consider version‑pinning or forking the repo to lock in stability.

### Русский

**JosephHampton/awesome-gemini-cli-subagents** — это набор из 51 готового к использованию под‑агента для Gemini CLI, который позволяет быстро добавить специализированные AI‑функции (RAG, агентные цепочки, прототипы новых возможностей) без необходимости собирать собственный стек моделей. Для внедрения достаточно скопировать нужный под‑агент в каталог `.gemini/agents/`, после чего Gemini автоматически делегирует запросы соответствующему специалисту. Уровень готовности — средний: проект подходит для прототипов и внутренних workflow, но перед запуском в продакшн требуется проверка зависимостей, лицензий и безопасности.

### 中文

**项目简介**  
JosephHampton/awesome-gemini-cli-subagents 收录了 51 个可直接使用的 Gemini CLI 子代理（subagents），只需把它们放进项目根目录的 `.gemini/agents/`，Gemini 就能根据任务自动委派给最合适的专精代理。

**价值**  
- **快速赋能 AI**：无需从零搭建模型栈，直接复用成熟的子代理即可实现聊天、检索增强生成（RAG）或复杂工作流。  
- **原型迭代利器**：在原型阶段即可试验多种 AI 能力，帮助团队快速验证产品概念。  
- **统一治理**：子代理统一以 Shell 脚本形式提供，配套的 API/SDK/CLI、语言与主题元数据便于审计、监控和后期维护。

**典型接入方式**  
1. **克隆或下载仓库** → 将需要的子代理复制到本地项目的 `.gemini/agents/` 目录。  
2. **检查元数据**（`manifest.yaml` 或脚本注释）确认接口类型、依赖语言、支持的模型或工具。  
3. **在 Gemini 配置文件中声明**（如 `gemini.yml`）对应的代理名称或标签，Gemini 会在运行时自动路由。  
4. **本地测试**：使用 `gemini run <task>` 验证子代理是否按预期响应，必要时调整环境变量或依赖。  

**生产可用性**  
- **成熟度**：已收录 51 个经过实际项目验证的子代理，适合作为原型或内部业务流程的基础。  
- **依赖管理**：子代理主要实现为 Shell 脚本，依赖外部工具（curl、jq、Python 等）需在 CI/CD 中显式声明并进行安全扫描。  
- **维护状态**：近期（2026‑07‑12）有更新，GitHub ★36，社区活跃度一般；在正式生产前建议完成以下检查：  
  - 许可证兼容性（确认 MIT/Apache 等开源许可是否符合公司政策）  
  - 安全审计：审查脚本中可能的命令注入或凭证泄露风险  
  - 监控与回滚：为每个子代理添加日志、超时和错误捕获机制，便于故障定位。  
- **结论**：在做好依赖、许可证和安全审计的前置工作后，可安全用于内部生产环境；对外部高并发或严格合规场景仍建议进行进一步的稳健性测试。

## 🧭 Practical evaluation

**Value:** JosephHampton/awesome-gemini-cli-subagents helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 36 GitHub stars
- updated 2026-07-12
- primary language: Shell
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 61/100 |
| recency | 80/100 |
| adoption | 24/100 |
| production | 67/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/JosephHampton/awesome-gemini-cli-subagents) · [← Back to AI/ML](./README.md)</sub>
