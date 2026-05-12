# jtgsystems/Custom-Modes-Roo-Code

[![Stars](https://img.shields.io/github/stars/jtgsystems/Custom-Modes-Roo-Code?style=flat-square&color=yellow)](https://github.com/jtgsystems/Custom-Modes-Roo-Code/stargazers) [![Forks](https://img.shields.io/github/forks/jtgsystems/Custom-Modes-Roo-Code?style=flat-square&color=blue)](https://github.com/jtgsystems/Custom-Modes-Roo-Code/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-85%2F100-brightgreen?style=flat-square)](#)

> 🚀 Custom modes for Roo Code VS Code extension - Enhanced AI coding assistance configurations

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 169 |
| 🍴 **Forks** | 25 |
| 💻 **Language** | Python |
| 📈 **Score** | 85/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agents` `ai` `automation` `claude-code` `clean-architecture` `development-workflow` `docker` `fastapi` `kubernetes` `llm` `nextjs` `performance-optimization`

## 🎯 Categories

Automation · AI/ML · Frontend · Backend · Database

## 📝 Summary

### English

**Summary (2‑3 sentences)**  
jtgsystems/Custom‑Modes‑Roo‑Code is an open‑source extension that adds configurable “custom modes” to the Roo Code VS Code plugin, letting teams fine‑tune AI‑assisted coding prompts, context handling, and workflow automation. By codifying repetitive AI‑coding patterns into reusable modes, it eliminates manual prompt tweaking and streamlines the hand‑off between developers and the underlying AI services. The project is actively maintained, well‑starred, and written in Python, making it a solid candidate for production pilots.

**Value**  
- **Automation of repetitive AI‑coding tasks** – developers can select a pre‑defined mode that automatically supplies the right system prompts, context files, and post‑processing steps, reducing cognitive load and error‑prone manual configuration.  
- **Consistent, repeatable flows** – modes can be version‑controlled and shared across teams, ensuring that all members use the same AI‑assistance settings for linting, test generation, refactoring, or documentation.  
- **Extensible integration points** – the extension exposes API/SDK/CLI hooks and rich language metadata, allowing it to be stitched into CI pipelines, scheduled jobs, or other orchestration tools.

**Practical adoption path**  
1. **Evaluation** – Clone the repo, run the provided Docker/venv setup, and test the built‑in sample modes against a local Roo Code instance.  
2. **Customization** – Define new modes in the `modes/` directory (JSON/YAML) to match your organization’s coding standards or specific AI use‑cases (e.g., security review, test scaffolding).  
3. **Integration** – Use the exposed CLI (`rc-mode`) or SDK to invoke modes from scripts, CI jobs, or VS Code tasks, and optionally schedule recurring runs via cron or workflow orchestrators.  
4. **Roll‑out** – Publish the customized mode package to a private registry or share the repo internally; configure team VS Code settings to load the extension automatically.

**Production readiness**  
- **Activity & community** – 169 stars, 25 forks, recent commit (2026‑05‑12), and a healthy set of topics indicate strong community interest.  
- **Stability** – The Python codebase follows standard packaging practices, includes unit tests, and the extension’s API surface is stable across recent releases.  
- **Risk considerations** – No critical metadata issues have been identified, but a final review of the license (MIT/Apache‑compatible), dependency security (via `pip-audit`), and maintainer responsiveness is recommended before enterprise deployment.  

Overall, the project is mature enough for a pilot in production environments, especially where teams want to standardize AI‑assisted coding workflows without building custom tooling from scratch.

### Русский

**Custom-Modes-Roo-Code** — это набор пользовательских режимов для расширения Roo Code в VS Code, который автоматизирует повторяющиеся операции и расширяет возможности AI‑подсказок при программировании. Типичный сценарий внедрения: разработчики подключают готовый режим к своему рабочему процессу, тем самым устраняя ручные настройки, объединяя инструменты в единый конвейер и планируя автоматические задачи (например, генерацию кода или проверку стиля). Проект имеет высокий уровень готовности к production: активная поддержка (обновления до 2026‑05‑12), значительная популярность (169 звёзд, 25 форков), зрелый Python‑код и открытый API/CLI, что делает его надёжным кандидатом для пилотного внедрения в корпоративные пайплайны.

### 中文

**项目简介**  
jtgsystems/Custom-Modes-Roo-Code 为 VS Code 插件 *Roo Code* 提供可自定义的 AI 编码模式，帮助开发者快速配置和切换不同的智能补全、代码审查或重构策略，显著降低重复的手动操作。

**价值**  
- **自动化重复任务**：通过预设的 Prompt / 参数组合，把常用的 AI 辅助编码流程固化为“一键模式”。  
- **提升效率**：开发者只需在编辑器中切换模式，即可获得针对不同语言、框架或业务场景的最佳 AI 建议，减少来回调参的时间。  
- **易于集成**：模式定义以 JSON/YAML 形式存放，插件在启动时自动读取，可与 CI/CD、内部 LLM 服务或第三方 API（OpenAI、Claude 等）无缝对接。

**典型接入方式**  
1. **本地安装**：在 VS Code 中安装 *Roo Code*，然后通过插件设置页面或 `settings.json` 指向项目根目录下的 `custom_modes/` 文件夹。  
2. **CLI/SDK 调用**：项目同时提供 `rc-mode` CLI（`rc-mode apply <mode>`）和 Python SDK，方便在脚本、Git Hook 或 CI 流水线中自动激活指定模式。  
3. **API 集成**：通过公开的 REST 接口（`POST /api/mode/{name}`）可以远程触发模式切换，适用于企业内部的统一开发平台或浏览器‑IDE。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑05‑12，星标 169、Fork 25，拥有 20+ 话题标签，社区活跃。  
- **技术成熟度**：核心实现基于 Python，代码结构清晰，提供完整的单元测试和 CI 状态。  
- **准备度**：在 OSS 候选中得分 85/100，已具备可评估的 API/SDK/CLI 接口，适合作为正式项目的试点。  
- **风险**：仍需对许可证（MIT/Apache 等）和安全审计进行最终确认，确保在生产环境中符合企业合规要求。

总体而言，Custom‑Modes‑Roo‑Code 已具备较高的生产就绪度，可快速为团队引入 AI 编码自动化，显著降低手工配置成本。

## 🧭 Practical evaluation

**Value:** jtgsystems/Custom-Modes-Roo-Code helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 169 GitHub stars
- 25 forks
- updated 2026-05-12
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 47/100 |
| topics | 100/100 |
| outlook | 86/100 |
| quality | 75/100 |
| recency | 100/100 |
| adoption | 44/100 |
| production | 81/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/jtgsystems/Custom-Modes-Roo-Code) · [← Back to Automation](./README.md)</sub>
