# adenaufal/anti-slop-writing

[![Stars](https://img.shields.io/github/stars/adenaufal/anti-slop-writing?style=flat-square&color=yellow)](https://github.com/adenaufal/anti-slop-writing/stargazers) [![Forks](https://img.shields.io/github/forks/adenaufal/anti-slop-writing?style=flat-square&color=blue)](https://github.com/adenaufal/anti-slop-writing/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Stop your AI from writing like AI. A universal system prompt eliminating every known LLM style tell — works with Claude Code, Gemini CLI, Codex CLI, Copilot, Cursor, and any web AI.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 92 |
| 🍴 **Forks** | 6 |
| 💻 **Language** | Unknown |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-07-06 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skill` `ai` `ai-detection` `anti-slop` `authentic-writing` `chatgpt` `claude` `content-writing` `copilot` `gemini` `llm` `prompt-engineering`

## 🎯 Categories

AI/ML · DevTools · Security

## 📝 Summary

### English

Here's a brief summary and analysis of the open-source project:

**Summary:** adenaufal/anti-slop-writing is an open-source system prompt designed to eliminate known AI writing styles, allowing users to add AI capabilities without starting from a blank model stack. This project is compatible with various AI tools, including Claude Code, Gemini CLI, and Copilot. It's ideal for prototyping AI features, building RAG or agent workflows, and evaluating model tooling.

**Value Proposition:** The project's value lies in its ability to help users integrate AI capabilities into their workflows without the need for extensive model training or setup. This can save time and resources, making it an attractive option for developers and businesses looking to explore AI-powered features.

**Practical Adoption Path:** To adopt this project, users can start by evaluating its feasibility through a small proof of concept and reviewing the README documentation. Once satisfied, they can integrate the system prompt into their existing workflows, beginning with prototyping AI features or building RAG or agent workflows. This approach allows users to test the waters before committing to a larger-scale implementation.

**Production Readiness:** The project is considered "Medium" in terms of production readiness, indicating that it's suitable for internal workflows or prototyping but requires additional checks and maintenance before being

### Русский

Резюме:

Проект adenaufal/anti-slop-writing представляет собой инструмент для предотвращения написания текста на стиле AI. Он позволяет добавлять функциональность AI без необходимости создания собственного моделирующего стека. Этот проект идеально подходит для прототипирования функций AI, создания RAG или агентных потоков, а также оценки инструментов моделирования. Проект имеет средний уровень готовности к production, что означает, что он может быть использован для внутренних потоков или прототипов, но требует проверки зависимостей и поддержки перед выпуском в production.

### 中文

**项目简介（2‑3 句）**  
adenaufal/anti‑slop‑writing 是一套通用的系统提示（system prompt），通过去除所有已知的大语言模型写作痕迹，让 AI 的输出更像人类而不是“机器”。它可直接在 Claude Code、Gemini CLI、Codex CLI、Copilot、Cursor 以及各类网页 AI 中使用，无需重新训练模型。

**价值**  
- **提升可用性**：在已有模型上叠加提示即可获得更自然、去“AI痕迹”的文本，省去从头构建或微调模型的成本。  
- **加速原型**：适用于快速验证 AI 功能、构建 RAG/Agent 工作流或评估不同模型工具的场景。  
- **跨平台**：一次编写提示，可在多种 LLM 接口复用，降低集成维护成本。

**典型接入方式**  
1. **准备 Prompt**：在项目根目录或 CI 中保存 `anti_slop_prompt.txt`（或直接在代码中定义）。  
2. **在调用 LLM 时注入**：  
   - **CLI**（如 `gemini-cli`、`codex-cli`）：在命令行加 `--system-prompt "$(cat anti_slop_prompt.txt)"`。  
   - **API/SDK**（如 OpenAI、Claude SDK）：在请求体的 `system` 或 `messages[0]` 中填入该提示。  
   - **IDE 插件**（Copilot、Cursor）：通过插件的自定义系统提示或在 `.vscode/settings.json` 中配置 `ai.prompt`。  
3. **验证**：运行一次对话或生成任务，检查输出是否去除了常见的“AI 风格”标记（如 “As an AI …”）。

**生产可用性**  
- **成熟度**：GitHub 92 星、6 Fork，最近一次提交于 2026‑07‑06，活跃度尚可。  
- **适用范围**：适合内部原型、研发工具链或对输出自然度有较高要求的业务流程。  
- **风险与准备**：  
  - 需要自行审查许可证（MIT/Apache 等）以及依赖的安全性。  
  - 由于提示本身不涉及模型代码，故对底层模型的安全风险影响有限，但仍应在生产环境进行 **小范围 POC** 并监控生成质量。  
  - 在正式上线前，建议将提示写入版本受控文件、加入 CI 检查，并做好回滚方案（如保留原始系统提示）。  

**结论**  
anti‑slop‑writing 为在现有 LLM 上快速实现“人类化”输出提供了低成本、跨平台的解决方案，适合作为原型或内部工具的加速器。经过一次小规模验证并完成许可证与安全审查后，即可在生产环境中稳妥使用。

## 🧭 Practical evaluation

**Value:** adenaufal/anti-slop-writing helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 92 GitHub stars
- 6 forks
- updated 2026-07-06
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 21/100 |
| stars | 42/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 71/100 |
| recency | 100/100 |
| adoption | 36/100 |
| production | 73/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/adenaufal/anti-slop-writing) · [← Back to AI/ML](./README.md)</sub>
