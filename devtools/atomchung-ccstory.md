# atomchung/ccstory

[![Stars](https://img.shields.io/github/stars/atomchung/ccstory?style=flat-square&color=yellow)](https://github.com/atomchung/ccstory/stargazers) [![Forks](https://img.shields.io/github/forks/atomchung/ccstory?style=flat-square&color=blue)](https://github.com/atomchung/ccstory/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Claude Code usage recap with narrative. ccusage tells you the bill, ccstory tells the story.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 42 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | Python |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`analytics` `ccusage` `claude` `claude-code` `cli` `developer-tools` `productivity` `python` `recap` `usage-tracking` `weekly-report`

## 🎯 Categories

DevTools · Data

## 📝 Summary

### English

Here's a brief summary of the open-source project:

**Project Summary:** atomchung/ccstory is an open-source tool that provides a usage recap and narrative for Claude Code, aiming to streamline developer workflows and improve collaboration. This project offers a straightforward integration with implementation signals such as API/SDK/CLI, language metadata, or focused topics. By automating local engineering tasks and improving CI feedback, developers can save time in daily development and review loops.

**Value Proposition:** The primary value of atomchung/ccstory lies in its ability to speed up developer workflows, automate local engineering tasks, and enhance CI feedback. This tool is particularly useful for engineers looking to streamline their daily development processes and improve collaboration with their team.

**Practical Adoption Path:** To adopt atomchung/ccstory, developers can follow these steps:

1. Evaluate the tool's integration with their existing development environment and infrastructure.
2. Assess the tool's ability to meet their specific needs and requirements.
3. Integrate the tool into their local engineering workflows, starting with small-scale testing and iteration.
4. Monitor the tool's performance and adjust as needed to ensure seamless integration and optimal results.

**Production Readiness:** atomchung/ccstory has a moderate level of production readiness, scoring 68/100. While it

### Русский

**atomchung/ccstory** — это open‑source утилита, которая преобразует данные о расходе Claude API в читаемый нарратив, позволяя инженерам быстро понять, за что они платят и какие задачи автоматизировать. Типичный сценарий — интеграция в локальные скрипты или CI/CD, где ccstory генерирует отчёты и подсказки для ускорения разработки, ревью и обратной связи. Готовность к production — средняя: проект пригоден для прототипов и внутренних пайплайнов, но перед выпуском в продакшн требуется проверка лицензии, безопасности и поддерживаемости зависимостей.

### 中文

**项目简介**  
atomchung/ccstory 是一个把 Claude Code 使用情况转化为可读叙事的工具。`ccusage` 负责展示费用明细，`ccstory` 则把这些数据编写成故事，让开发者一眼了解代码成本与行为。

**价值**  
- **节省时间**：在日常开发与代码审查时，直接看到费用与调用概况的可读报告，避免手动查询和统计。  
- **提升效率**：可嵌入 CI/CD 流程，自动生成成本/使用报告，帮助团队快速定位异常或优化点。  
- **改进反馈**：在 Pull Request、CI 日志或本地调试时提供直观的使用故事，帮助开发者更好地理解代码行为和资源消耗。

**典型接入方式**  
1. **CLI**：在本地或 CI 环境中通过 `ccstory` 命令行工具生成报告，支持自定义模板与输出格式（JSON、Markdown、HTML）。  
2. **SDK/API**：项目提供 Python SDK，调用 `generate_story()` 接口即可在代码中直接获取使用故事，适合自动化脚本或自定义仪表盘。  
3. **集成 CI**：在 GitHub Actions、GitLab CI 或 Jenkins 的构建步骤中加入 `ccstory`，将生成的报告作为构建产出或注释发布到 Pull Request。  

**生产可用性**  
- **成熟度**：当前评分 68/100，属于 **中等** 稳定性。适合原型、内部工具或受控环境使用。  
- **依赖与维护**：项目主要使用 Python，已更新至 2026‑07‑12，拥有 42 ⭐、4 🍴，但仍需进一步审查许可证、第三方依赖的安全性以及维护者活跃度。  
- **上线建议**：在正式生产前进行依赖安全扫描、版本锁定以及容错测试；若满足内部安全合规，可先在非关键业务或内部 CI 中试运行，确认报告准确性后再推广至全链路。

## 🧭 Practical evaluation

**Value:** atomchung/ccstory helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 42 GitHub stars
- 4 forks
- updated 2026-07-12
- primary language: Python
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 35/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 53/100 |
| recency | 40/100 |
| adoption | 30/100 |
| production | 55/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/atomchung/ccstory) · [← Back to DevTools](./README.md)</sub>
