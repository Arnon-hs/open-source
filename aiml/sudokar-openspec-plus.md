# sudokar/openspec-plus

[![Stars](https://img.shields.io/github/stars/sudokar/openspec-plus?style=flat-square&color=yellow)](https://github.com/sudokar/openspec-plus/stargazers) [![Forks](https://img.shields.io/github/forks/sudokar/openspec-plus?style=flat-square&color=blue)](https://github.com/sudokar/openspec-plus/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-46%2F100-brightgreen?style=flat-square)](#)

> OpenSpec Plus — Agentic skills that enhance OpenSpec's Spec-Driven Development through better discovery, requirements, design decisions, execution planning and execution. Works with Claude Code, OpenCode, Github Copilot and any other AI coding agents

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 24 |
| 🍴 **Forks** | 1 |
| 💻 **Language** | Unknown |
| 📈 **Score** | 46/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-skills` `ai` `ai-assisted-development` `ai-code-generation` `ai-code-quality` `claude-code` `code-quality` `coding` `coding-agent` `devin` `github-copilot` `opencode`

## 🎯 Categories

AI/ML · DevTools · Design

## 📝 Summary

### English

**Project Summary:**

OpenSpec Plus is an open-source project that enhances Spec-Driven Development by leveraging AI coding agents, such as Claude Code, OpenCode, and Github Copilot, to improve discovery, requirements, design decisions, execution planning, and execution. This project offers a value proposition by enabling developers to add AI capabilities without starting from a blank model stack. By utilizing OpenSpec Plus, users can prototype AI features, build RAG or agent workflows, and evaluate model tooling.

**Value:**

The value proposition of OpenSpec Plus lies in its ability to integrate AI coding agents with Spec-Driven Development, streamlining the development process by leveraging AI capabilities. This allows developers to focus on more complex tasks, while AI agents handle routine and repetitive tasks, enhancing overall productivity and efficiency.

**Practical Adoption Path:**

To adopt OpenSpec Plus, developers need to manually inspect the project before integrating it into their workflow. The integration path may not be immediately obvious from the metadata, so users should be prepared to validate the setup cost before committing to the project. Once integrated, OpenSpec Plus can be used to prototype AI features, build RAG or agent workflows, and evaluate model tooling.

**Production Readiness:**

OpenSpec Plus is considered production-ready with a medium level of

### Русский

OpenSpec Plus — набор агентных навыков, расширяющих Spec‑Driven Development в OpenSpec: улучшенный поиск требований, проектирование, планирование и исполнение, работающий с Claude Code, OpenCode, GitHub Copilot и другими AI‑кодерами. Он позволяет быстро прототипировать AI‑фичи, создавать RAG‑ и агентные пайплайны и оценивать инструменты моделей без необходимости строить собственный стек с нуля; однако перед внедрением требуется ручная проверка метаданных, так как пути интеграции неочевидны. Готовность к продакшну — средняя: подходит для прототипов и внутренних воркфлоу, но требует проверки зависимостей и обслуживания перед масштабированием.

### 中文

**项目简介（2‑3 句）**  
OpenSpec Plus 为 OpenSpec 的规范驱动开发注入智能体能力，提供更高效的需求发现、设计决策、执行计划与实际执行。它可与 Claude Code、OpenCode、GitHub Copilot 以及其他 AI 编码助理无缝协作，让开发者在已有规范基础上快速构建 AI 功能。

**价值**  
- **快速赋能 AI**：无需从零搭建模型堆栈，直接在 OpenSpec 项目中植入智能体，显著缩短原型开发周期。  
- **全链路支持**：从需求捕获、设计评审到代码生成、执行调度全流程覆盖，提升团队对规范的执行力与可追溯性。  
- **多平台兼容**：兼容 Claude Code、OpenCode、GitHub Copilot 等主流 AI 编码工具，降低学习成本并可复用已有 AI 投资。

**典型接入方式**  
1. **准备 OpenSpec 项目**：确保项目已经使用 OpenSpec 进行规范化描述。  
2. **安装 OpenSpec Plus**：在项目根目录执行 `npm install @openspec/plus`（或对应语言的包管理器）。  
3. **配置 AI 代理**：在 `openspec.plus.config.js` 中声明要使用的 AI 代理，例如 Claude Code 的 API Key、OpenCode 的 endpoint 或 Copilot 的 token。  
4. **启用智能体插件**：在 OpenSpec 编译/运行脚本中加入 `openspec-plus` 插件，例如  
   ```bash
   openspec build --plugin openspec-plus
   ```  
5. **手动审查生成产物**：首次运行后，检查生成的需求文档、设计建议和代码片段，确保符合业务预期后再正式提交。  

**生产可用性**  
- **成熟度**：当前评分 56/100，属于 **中等** 稳定性。适合原型、内部工具或实验性业务流程。  
- **上线前检查**：  
  - **依赖审计**：确认 AI 代理的服务 SLA、费用模型以及访问权限。  
  - **元数据完整性**：项目的 OpenSpec 元数据需完整，否则集成信号稀疏会导致功能缺失。  
  - **安全合规**：审查生成代码是否符合内部安全规范，尤其是涉及外部 API 调用的部分。  
- **运维成本**：需要定期更新 OpenSpec Plus 版本以及所依赖的 AI 代理 SDK，保持兼容性。  

**结论**  
OpenSpec Plus 为已有规范化项目提供“一键式” AI 能力，能够显著提升需求到实现的闭环效率。对于需要快速验证 AI 功能、构建 RAG/Agent 工作流的团队非常有价值；在正式生产环境使用前，建议完成依赖、合规和手动审查等检查，以降低集成风险。

## 🧭 Practical evaluation

**Value:** sudokar/openspec-plus helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 24 GitHub stars
- 1 forks
- updated 2026-07-01
- 20 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 8/100 |
| stars | 30/100 |
| topics | 100/100 |
| outlook | 51/100 |
| quality | 51/100 |
| recency | 40/100 |
| adoption | 24/100 |
| production | 49/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/sudokar/openspec-plus) · [← Back to AI/ML](./README.md)</sub>
