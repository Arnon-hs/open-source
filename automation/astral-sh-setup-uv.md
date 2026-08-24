# astral-sh/setup-uv

[![Stars](https://img.shields.io/github/stars/astral-sh/setup-uv?style=flat-square&color=yellow)](https://github.com/astral-sh/setup-uv/stargazers) [![Forks](https://img.shields.io/github/forks/astral-sh/setup-uv?style=flat-square&color=blue)](https://github.com/astral-sh/setup-uv/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Set up your GitHub Actions workflow with a specific version of https://docs.astral.sh/uv/

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 805 |
| 🍴 **Forks** | 105 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`hacktoberfest` `python` `uv`

## 🎯 Categories

Automation

## 📝 Summary

### English

Here's a brief summary of the astral-sh/setup-uv project:

Astral-sh/setup-uv is an open-source project that automates the setup of GitHub Actions workflows with a specific version of the UV tool from Astral.sh. This tool helps developers remove repetitive manual operations from their workflow, allowing them to connect tools into repeatable flows and schedule operational tasks. With a high production readiness score and strong ecosystem signals, this project is suitable for serious pilots and adoption.

The practical adoption path involves:

1. Reviewing the project's metadata, including license, security posture, and active maintainers, to ensure it aligns with your project's needs.
2. Inspecting the integration signals and metadata to ensure it meets your requirements.
3. Configuring the GitHub Actions workflow to use the astral-sh/setup-uv tool.
4. Testing and refining the workflow to ensure it works as expected.

The production readiness of this project is high due to:

1. Recent activity, indicating ongoing maintenance and development.
2. Strong adoption, with 805 GitHub stars and 105 forks.
3. Ecosystem signals, such as the use of TypeScript and 3 topics, indicating a well-maintained and widely-used project.
4. High-quality signals, such as regular updates and a large community

### Русский

Резюме:

Астральный шаблон setup-uv для GitHub Actions позволяет автоматизировать повторяющиеся задачи и интегрировать инструменты в повторяющиеся потоки. Это уменьшает время, затрачиваемое на ручную работу и позволяет эффективно управлять операционными задачами. Проект готов к внедрению в production, имея сильные сигналы активности, адопции и экосистемы, а также высокую оценку качества (67/100).

### 中文

**项目简介**  
astral‑sh/setup‑uv 是一个 GitHub Actions 官方插件，能够在工作流中自动安装并锁定指定版本的 **uv**（Python 包管理与构建工具），省去手动下载、配置和版本管理的步骤。

**价值**  
- **消除重复性手动操作**：只需在 workflow 中声明版本，即可在每次 CI 运行时保证 uv 环境一致。  
- **提升可重复性**：将 uv 的安装、缓存和路径配置纳入代码，确保本地、CI 以及生产环境使用同一套依赖解析规则。  
- **加速开发与交付**：通过缓存机制和快速安装，显著缩短 CI 执行时间，帮助团队更快交付 Python 包。

**典型接入方式**  

```yaml
name: CI

on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      # 1️⃣ 使用插件安装指定版本的 uv
      - uses: astral-sh/setup-uv@v1
        with:
          uv-version: "0.4.5"   # 需要的 uv 版本，可省略使用 latest

      # 2️⃣ 让 uv 可在后续步骤中直接使用
      - name: Install dependencies
        run: uv sync   # 例如使用 uv 安装项目依赖

      # 3️⃣ 运行测试或构建
      - name: Run tests
        run: uv run pytest
```

关键点：  
- `uses: astral-sh/setup-uv@<tag>` 指定插件版本（推荐使用固定标签避免意外升级）。  
- `with: uv-version` 可选，明确锁定所需的 uv 版本。  
- 插件会自动进行缓存（`~/.cache/uv`），后续运行更快。

**生产可用性**  
- **活跃度**：最近一次更新于 2026‑07‑05，拥有 805 ★、105 Fork，社区活跃。  
- **语言与生态**：使用 TypeScript 编写，兼容所有官方支持的 runner（ubuntu、macOS、windows）。  
- **成熟度**：已在多个公开项目中采用，具备完整的 GitHub Actions 集成测试。  
- **风险**：目前未发现重大许可证或安全问题，但在正式上线前建议审查项目的 LICENSE、依赖安全报告以及维护者活跃度。

综合来看，astral‑sh/setup‑uv 已具备 **高生产准备度**，适合作为正式 CI/CD 流程的标准化组件。只要在引入前完成一次安全审计，即可在生产环境中放心使用。

## 🧭 Practical evaluation

**Value:** astral-sh/setup-uv helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 805 GitHub stars
- 105 forks
- updated 2026-07-05
- primary language: TypeScript
- 3 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 62/100 |
| topics | 38/100 |
| outlook | 54/100 |
| quality | 57/100 |
| recency | 40/100 |
| adoption | 59/100 |
| production | 56/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/astral-sh/setup-uv) · [← Back to Automation](./README.md)</sub>
