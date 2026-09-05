# BigCatNotFat/PacificOceanAI

[![Stars](https://img.shields.io/github/stars/BigCatNotFat/PacificOceanAI?style=flat-square&color=yellow)](https://github.com/BigCatNotFat/PacificOceanAI/stargazers) [![Forks](https://img.shields.io/github/forks/BigCatNotFat/PacificOceanAI?style=flat-square&color=blue)](https://github.com/BigCatNotFat/PacificOceanAI/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> AI-powered writing assistant for Overleaf LaTeX editor - Chrome/Edge extension with multi-model support (OpenAI, Claude, Gemini)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 175 |
| 🍴 **Forks** | 1 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-writing` `browser-extension` `chatgpt` `chrome-extension` `edge-extension` `latex` `llm` `openai` `overleaf` `privacy-first` `react`

## 🎯 Categories

AI/ML · Frontend

## 📝 Summary

### English

**Summary:** PacificOceanAI is an open-source Chrome/Edge extension that adds AI-powered writing assistance to the Overleaf LaTeX editor, supporting multiple AI models (OpenAI, Claude, Gemini). This project enables users to prototype AI features, build RAG or agent workflows, and evaluate model tooling without starting from scratch. It is a useful tool for internal workflows or proof-of-concepts, but requires careful dependency and maintenance checks before production.

**Value:** PacificOceanAI offers a convenient way to add AI capability to the Overleaf LaTeX editor, allowing users to leverage the strengths of multiple AI models. This can be particularly useful for researchers, academics, and developers who need to prototype AI features or build workflows that integrate with LaTeX documents.

**Practical Adoption Path:** To adopt PacificOceanAI, users can start by installing the Chrome/Edge extension and exploring its features. They can then experiment with different AI models, configure the extension to suit their needs, and integrate it with their existing workflows. For more complex use cases, users can evaluate the extension's API and build custom integrations. Before production deployment, users should carefully review the extension's dependencies, security posture, and maintenance requirements.

**Production Readiness:** PacificOceanAI has a medium level of production readiness, making it suitable for internal

### Русский

**BigCatNotFat/PacificOceanAI** — это расширение для Chrome/Edge, которое добавляет в редактор Overleaf возможности AI‑писателя (поддержка моделей OpenAI, Claude и Gemini). Оно идеально подходит для быстрого прототипирования функций ИИ, построения RAG‑ или агентных воркфлоу и оценки разных моделей, однако для production‑использования требуется небольшая проверка зависимостей, лицензии и безопасности, а также небольшое proof‑of‑concept‑внедрение. При наличии этих шагов проект может стать надёжным решением для внутренних или клиентских LaTeX‑рабочих процессов.

### 中文

**价值**  
BigCatNotFat/PacificOceanAI 为 Overleaf（LaTeX 在线编辑器）提供即插即用的 AI 写作助手，用户只需在 Chrome/Edge 浏览器装上扩展，即可在编辑页面直接调用 OpenAI、Claude、Gemini 等多模型进行文本补全、公式解释、参考文献生成等任务。它让团队在不搭建完整模型堆栈的情况下，快速原型化 AI 功能、实验 RAG（检索增强生成）或智能代理工作流，从而显著提升文档撰写效率和质量。

**典型接入方式**  
1. **浏览器扩展安装**：在 Chrome/Edge Web Store 下载并安装扩展。  
2. **API Key 配置**：在扩展的设置页填写对应模型的 API Key（OpenAI、Anthropic、Google Gemini 等），可一次配置多模型并在 UI 中切换。  
3. **页面注入**：扩展会在 Overleaf 编辑器页面注入按钮/快捷键，用户选中文本后点击即可触发 AI 生成或改写。  
4. **可选的 RAG/Agent 集成**：通过扩展提供的自定义脚本入口，接入内部文档检索服务或业务代理，实现更复杂的“文档‑‑>AI‑>文档”工作流。  

**生产可用性**  
- **成熟度**：目前在 GitHub 上已有 175+ 星，最近一次提交是 2026‑06‑27，代码基于 TypeScript，结构清晰，适合作为内部原型或小规模生产使用。  
- **依赖与维护**：依赖于浏览器扩展平台和外部模型 API，需定期检查 API 费用、配额以及模型版本兼容性；项目本身的维护者活跃度尚需进一步确认。  
- **安全与合规**：未发现显著的元数据泄露风险，但仍需审查许可证（MIT / Apache 等）以及对 API Key 的本地存储方式，确保符合组织的安全策略。  
- **上线建议**：先在测试环境做一个“选中文本 → AI 生成” 的最小可行验证（PoC），确认模型响应、费用、隐私合规后，再逐步推广到团队的 Overleaf 工作流中。  

综上，PacificOceanAI 适合作为快速验证 AI 写作功能的工具，具备中等的生产可用性；在完成依赖审计和安全加固后，可在内部或受控的生产环境中稳定使用。

## 🧭 Practical evaluation

**Value:** BigCatNotFat/PacificOceanAI helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 175 GitHub stars
- 1 forks
- updated 2026-06-27
- primary language: TypeScript
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 8/100 |
| stars | 48/100 |
| topics | 100/100 |
| outlook | 66/100 |
| quality | 66/100 |
| recency | 80/100 |
| adoption | 37/100 |
| production | 67/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/BigCatNotFat/PacificOceanAI) · [← Back to AI/ML](./README.md)</sub>
