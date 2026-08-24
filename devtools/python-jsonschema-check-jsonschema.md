# python-jsonschema/check-jsonschema

[![Stars](https://img.shields.io/github/stars/python-jsonschema/check-jsonschema?style=flat-square&color=yellow)](https://github.com/python-jsonschema/check-jsonschema/stargazers) [![Forks](https://img.shields.io/github/forks/python-jsonschema/check-jsonschema?style=flat-square&color=blue)](https://github.com/python-jsonschema/check-jsonschema/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> A CLI and set of pre-commit hooks for jsonschema validation with built-in support for GitHub Workflows, Renovate, Azure Pipelines, and more!

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 321 |
| 🍴 **Forks** | 64 |
| 💻 **Language** | Python |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `json-schema` `pre-commit` `python`

## 🎯 Categories

DevTools

## 📝 Summary

### English

python‑jsonschema/check‑jsonschema provides a CLI and pre‑commit hooks that automate JSON‑Schema validation across CI/CD pipelines (GitHub Workflows, Renovate, Azure Pipelines, etc.), eliminating repetitive manual checks and enabling repeatable, scheduled validation tasks. Its straightforward integration—exposing clear API/SDK/CLI signals and strong Python‑based implementation—makes adoption easy for teams looking to plug schema validation into existing automation workflows. With recent activity, solid adoption metrics (321★, 64 forks), and high production‑readiness signals, it is a reliable open‑source candidate for a pilot or broader rollout.

### Русский

**python-jsonschema/check-jsonschema** — это CLI‑утилита и набор pre‑commit‑хуков для автоматической проверки JSON‑документов по схемам jsonschema, с готовой интеграцией в GitHub Workflows, Renovate, Azure Pipelines и другие CI/CD‑системы. Она позволяет избавиться от ручных проверок, включать валидацию в повторяемые конвейеры и планировать регулярные задачи, что ускоряет процесс разработки и повышает надёжность артефактов. Проект обладает высокой готовностью к production: активная поддержка (обновление 2026‑06‑29), 321 звезда, 64 форка, широкая экосистема и открытый Python‑API, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**项目简介**  
`python-jsonschema/check-jsonschema` 是一个基于 CLI 的工具集合，提供 JSON Schema 校验以及 pre‑commit hook，实现了对 GitHub Workflows、Renovate、Azure Pipelines 等 CI/CD 平台的原生支持。

**价值**  
- **自动化重复工作**：在提交、CI 或日常运维中自动执行 JSON Schema 校验，彻底摆脱手动检查的错误与成本。  
- **可组合的流水线节点**：通过 CLI、pre‑commit hook 或 CI 集成点，轻松把校验环节嵌入任意 DevOps 流程，实现“一次配置、全流程复用”。  
- **统一的错误报告**：统一的错误输出格式便于在 GitHub Checks、Azure Pipelines 日志或 Renovate 报告中直接呈现，提升团队可视化与调试效率。

**典型接入方式**  
1. **CLI**：`check-jsonschema --schemafile schema.json data.json` 直接在本地或 CI 脚本中调用。  
2. **Pre‑commit Hook**：在 `.pre-commit-config.yaml` 中声明 `repo: https://github.com/python-jsonschema/check-jsonschema`，即可在每次 `git commit` 前自动校验。  
3. **CI/CD 集成**：在 GitHub Actions、Azure Pipelines、GitLab CI 等工作流中使用官方提供的 Action/Task，或在 Renovate 配置中加入 `check-jsonschema` 作为自定义脚本步骤。  

**生产可用性**  
- **活跃度**：最近一次提交（2026‑06‑29），拥有 321 ⭐、64 🍴，社区活跃。  
- **语言与依赖**：纯 Python 实现，兼容 Python 3.8+，依赖成熟的 `jsonschema` 库。  
- **成熟度**：已在多个开源项目和企业 CI 中实际使用，具备完整的错误码、日志与文档，适合作为正式环境的校验组件。  
- **风险**：需进一步确认许可证兼容性（MIT），以及审计其安全依赖链，但整体风险低，已具备进入生产的条件。

## 🧭 Practical evaluation

**Value:** python-jsonschema/check-jsonschema helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 321 GitHub stars
- 64 forks
- updated 2026-06-29
- primary language: Python
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 53/100 |
| topics | 50/100 |
| outlook | 57/100 |
| quality | 56/100 |
| recency | 40/100 |
| adoption | 51/100 |
| production | 55/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/python-jsonschema/check-jsonschema) · [← Back to DevTools](./README.md)</sub>
