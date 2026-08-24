# sahajamit/promptwright

[![Stars](https://img.shields.io/github/stars/sahajamit/promptwright?style=flat-square&color=yellow)](https://github.com/sahajamit/promptwright/stargazers) [![Forks](https://img.shields.io/github/forks/sahajamit/promptwright?style=flat-square&color=blue)](https://github.com/sahajamit/promptwright/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Login-less, bring-your-own-key desktop agent that turns plain English into browser automation — and generates runnable Playwright, Cypress, and Selenium scripts.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 112 |
| 🍴 **Forks** | 24 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-agent` `browser-automation` `byok` `cypress` `electron` `playwright` `selenium` `test-automation`

## 🎯 Categories

Automation · AI/ML · DevTools

## 📝 Summary

### English

**Project Summary:**

Promptwright is an open-source, login-less desktop agent that automates browser interactions by converting plain English into executable scripts for Playwright, Cypress, and Selenium. This tool helps remove repetitive manual operations from workflows, making it ideal for automating tasks and integrating tools into repeatable flows. With a simple setup process, users can quickly connect tools and schedule operational tasks.

**Value Proposition:**

The primary value of Promptwright lies in its ability to automate repetitive tasks, freeing up time and resources for more strategic activities. By converting plain English into executable scripts, users can easily integrate tools and create repeatable workflows, making it a valuable asset for teams looking to streamline their operations.

**Practical Adoption Path:**

Adopting Promptwright involves a few steps:

1. **Evaluation:** Start by evaluating the project's feasibility through a small proof of concept, as suggested by the project's README.
2. **Setup:** Set up the Promptwright agent on your desktop, which is a relatively straightforward process.
3. **Scripting:** Write plain English scripts that can be converted into executable scripts for Playwright, Cypress, and Selenium.
4. **Integration:** Integrate the scripts into your workflow, connecting tools and scheduling operational tasks.

**Production Readiness:**

Promptwright

### Русский

Резюме проекта sahajamit/promptwright:

Этот open-source проект - это login-less агент, позволяющий автоматизировать браузерную навигацию с помощью натуральных английских команд. Он генерирует исполняемые скрипты для Playwright, Cypress и Selenium, что позволяет удалить повторяющиеся ручные операции из рабочего процесса.

Типовым сценарием внедрения является подключение инструментов в повторяющиеся потоки, удаление ручной работы и планирование операционных задач. Однако важно начать с небольшого proof of concept и проверки README, прежде чем приступать к интеграции.

Проект sahajamit/promptwright готов к production на среднем уровне, что делает его подходящим для прототипов или внутренних потоков данных. Однако необходимо проверить зависимость и поддержку проекта перед его использованием в производстве.

### 中文

**项目简介**  
`sahajamit/promptwright` 是一个无需登录、可自带密钥的桌面代理，能够把自然语言指令直接转化为浏览器自动化脚本，并自动生成可运行的 **Playwright、Cypress** 与 **Selenium** 代码。

**价值**  
- **消除重复手工操作**：把日常的点击、填表、数据抓取等步骤交给 AI 自动生成脚本，显著提升效率。  
- **快速构建可重复的工作流**：通过生成的脚本可以轻松将多个工具串联，实现端到端的自动化流程。  
- **灵活适配多种框架**：一次指令即可得到三大主流自动化框架的实现，降低学习成本并支持现有项目迁移。

**典型接入方式**  
1. **准备环境**：在本地或 CI 机器上安装 Node.js，克隆仓库并运行 `npm install`。  
2. **配置密钥**：在 `.env`（或系统环境变量）中写入你的 OpenAI/Claude 等 LLM API 密钥。  
3. **验证 README**：按照仓库自带的快速入门示例运行 `npm run demo`，确认能够把英文指令成功生成对应的 Playwright/Cypress/Selenium 脚本。  
4. **小规模 PoC**：挑选一个业务中最常见的手工任务（如登录后数据导出），用自然语言描述，让 PromptWright 生成脚本并在本地跑通。  
5. **集成到流程**：将生成的脚本加入现有的 CI/CD 或任务调度系统（如 GitHub Actions、Jenkins、Cron），实现定时或触发式执行。

**生产可用性**  
- **成熟度**：目前评分 67/100，适合作为原型或内部工具使用。代码活跃（最近更新 2026‑07‑10），Stars 112、Forks 24，说明社区有一定关注。  
- **依赖与维护**：核心实现基于 TypeScript，依赖较少，但在生产环境前应完成以下检查：  
  - 代码审计，确保没有未锁定的依赖版本或已知安全漏洞。  
  - 许可证兼容性（项目采用 MIT/Apache 等开源许可证，需要确认与贵司合规要求一致）。  
  - 维护者活跃度：虽然最近有提交，但仍建议关注后续 issue 响应速度。  
- **上线建议**：先在沙箱或内部环境做完整的 PoC，验证脚本的可靠性与错误恢复机制后，再逐步推广到生产。对关键任务可加上超时、重试以及日志审计层，以提升可靠性。

综上，PromptWright 能快速把业务语言转化为自动化脚本，适合作为提升内部效率的“AI 代码生成”工具，经过适当的安全与可靠性审查后即可在生产环境中使用。

## 🧭 Practical evaluation

**Value:** sahajamit/promptwright helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 112 GitHub stars
- 24 forks
- updated 2026-07-10
- primary language: TypeScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 59/100 |
| recency | 40/100 |
| adoption | 41/100 |
| production | 54/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-10 · [View on GitHub](https://github.com/sahajamit/promptwright) · [← Back to Automation](./README.md)</sub>
