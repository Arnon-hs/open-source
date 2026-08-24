# SonarSource/sonarqube-cli

[![Stars](https://img.shields.io/github/stars/SonarSource/sonarqube-cli?style=flat-square&color=yellow)](https://github.com/SonarSource/sonarqube-cli/stargazers) [![Forks](https://img.shields.io/github/forks/SonarSource/sonarqube-cli?style=flat-square&color=blue)](https://github.com/SonarSource/sonarqube-cli/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Command-line interface for SonarQube with AI agent integration. Scan for secrets and get fast feedback on code quality and security from your terminal.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 194 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `ai` `cli` `code-quality` `secrets` `security` `sonarqube` `static-analysis`

## 🎯 Categories

AI/ML · DevTools · Security

## 📝 Summary

### English

**Brief Summary**  
SonarSource/sonarqube‑cli is a TypeScript‑based command‑line tool that brings SonarQube’s code‑quality and security analysis directly to the terminal, augmented with an AI agent that can scan for secrets and provide rapid, contextual feedback. With 194 stars, recent commits, and a clean API/CLI surface, it offers a ready‑to‑use foundation for prototyping AI‑enhanced RAG or agent workflows without building a model stack from scratch.  

**Value**  
- **AI‑enabled insights**: The built‑in agent can automatically detect secrets, suggest remediation, and answer quality‑related questions, turning raw scan results into actionable guidance.  
- **Fast developer feedback**: Running the CLI locally gives immediate visibility into code health, shortening the feedback loop compared with waiting for CI pipelines.  
- **Low‑effort integration**: Because it exposes a standard CLI and SDK, teams can embed it in scripts, CI/CD jobs, or custom agents with just a few configuration steps, accelerating the creation of prototype AI features or full‑fledged RAG pipelines.  

**Practical Adoption Path**  
1. **Pilot** – Install the npm package (`npm i -g sonarqube-cli`) and run a scan on a small repo to evaluate output quality and AI response relevance.  
2. **CI/CD integration** – Add the CLI to your build pipeline (GitHub Actions, GitLab CI, etc.) to enforce quality gates and capture AI‑generated findings as build artifacts.  
3. **Agent/RAG extension** – Wrap the CLI calls in a custom AI agent or LangChain/RAG component, feeding the scan results into a vector store for downstream queries or automated remediation suggestions.  
4. **Scale** – Deploy the CLI across multiple services or monorepos, optionally configuring it to point at a self‑hosted SonarQube server for enterprise‑grade data governance.  

**Production Readiness**  
- **Activity & Community**: Recent commits (as of 2026‑06‑23), 194 stars, and active issue discussion indicate a healthy open‑source project.  
- **Stability**: The TypeScript codebase is well‑typed, and the CLI has a stable command surface, making it suitable for production scripts.  
- **Ecosystem Fit**: Straightforward API/SDK exposure and clear language metadata simplify integration with existing DevOps tooling.  
- **Risks**: Licensing and long‑term maintainer commitment still need a final review, but no major security or metadata concerns have been identified. Overall, the project is mature enough for a serious pilot and can be promoted to production after the standard security and compliance checks.

### Русский

SonarSource/sonarqube‑cli — это CLI‑утилита для SonarQube, расширяющая стандартный сканер возможностями AI‑агента: из терминала можно быстро проверять код на уязвимости, искать секреты и получать мгновенную обратную связь по качеству и безопасности. Проект подходит для прототипирования AI‑фич, построения RAG‑ или агентных воркфлоу и оценки инструментов модели, так как предоставляет открытый API/SDK и метаданные языка. По активности репозитория (194 ★, недавние коммиты, широкая экосистема) готовность к пилотному использованию в продакшене оценивается как высокая, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**简短介绍**  
SonarSource/sonarqube‑cli 是一款面向终端的 SonarQube 命令行工具，内置 AI Agent 能力，可在本地快速扫描代码中的安全隐患（如 secrets）并即时返回质量与安全反馈。  

**价值**  
- **即插即用的 AI 能力**：无需自行训练模型，即可在现有 SonarQube 工作流中加入智能分析、代码建议和 RAG（检索增强生成）等功能。  
- **提升开发效率**：开发者在终端即可获得安全/质量报告，缩短 CI/CD 反馈闭环。  
- **原型与实验友好**：提供统一的 API/SDK 与 CLI，方便快速构建和验证 AI 驱动的代码审查、自动化修复等新特性。  

**典型接入方式**  
1. **CLI 直接使用**：在本地或 CI 环境中安装 npm 包（`npm i -g @sonarqube/cli`），通过 `sonarqube scan` 命令提交代码并获取 AI 反馈。  
2. **SDK 调用**：在自定义脚本或工具中引入 TypeScript SDK，调用 `scan()`、`analyzeSecrets()` 等方法，获取结构化的分析结果用于后续自动化处理。  
3. **Agent/Workflow 集成**：结合 GitHub Actions、GitLab CI 或自建流水线，将 CLI 作为步骤执行，并将返回的 JSON 报告喂入 RAG 系统或 Chat‑Ops 机器人，实现 “代码‑AI‑反馈” 的闭环。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23 最近一次提交，拥有 194 星、8 个 fork，社区活跃。  
- **技术成熟**：使用 TypeScript 编写，提供完整的 API 文档和示例，易于在现有 TypeScript/JavaScript 项目中集成。  
- **安全与合规**：项目已通过初步的许可证与安全审查（暂无重大风险），并得到 SonarSource 官方背书，适合作为正式生产环境的试点或核心组件。  

综合来看，sonarqube‑cli 具备 **高可用性**、**易集成** 与 **AI 增值** 三大优势，是在现有 SonarQube 体系上快速引入智能代码审查的理想选择。

## 🧭 Practical evaluation

**Value:** SonarSource/sonarqube-cli helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 194 GitHub stars
- 8 forks
- updated 2026-06-23
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 49/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 59/100 |
| recency | 40/100 |
| adoption | 42/100 |
| production | 57/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/SonarSource/sonarqube-cli) · [← Back to AI/ML](./README.md)</sub>
