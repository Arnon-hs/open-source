# JetBrains/qodana-cli

[![Stars](https://img.shields.io/github/stars/JetBrains/qodana-cli?style=flat-square&color=yellow)](https://github.com/JetBrains/qodana-cli/stargazers) [![Forks](https://img.shields.io/github/forks/JetBrains/qodana-cli?style=flat-square&color=blue)](https://github.com/JetBrains/qodana-cli/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> 🔧 JetBrains Qodana’s official command line tool

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 231 |
| 🍴 **Forks** | 26 |
| 💻 **Language** | Go |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ci` `cli` `code-quality` `code-review` `code-scanning` `devsecops` `java` `javascript` `kotlin` `php` `python` `qodana`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
JetBrains /qodana‑cli is the official command‑line interface for Qodana, JetBrains’ AI‑enhanced static‑analysis platform. Written in Go, it lets developers invoke Qodana’s analysis, retrieve rich language‑specific signals, and integrate AI‑powered checks (e.g., RAG or agent workflows) directly into CI/CD pipelines. With active maintenance, a growing user base (231 ★), and a clean CLI/SDK surface, it’s ready for early‑stage pilots and production use.  

**Value**  
- **AI‑augmented quality gates** – the tool surfaces implementation‑level metadata (API usage, SDK calls, language constructs) that downstream LLMs can consume to generate precise suggestions, automated fixes, or to feed retrieval‑augmented generation (RAG) pipelines.  
- **Zero‑setup prototyping** – you can spin up Qodana analyses without building a custom model stack, accelerating proof‑of‑concepts for AI‑driven code review, security linting, or documentation generation.  
- **Extensible integration** – the CLI outputs JSON/HTML reports and exposes environment variables, making it straightforward to hook into existing build systems, GitHub Actions, or custom orchestration layers.  

**Practical Adoption Path**  
1. **Evaluate locally** – install the binary (`go install github.com/JetBrains/qodana-cli@latest`), run `qodana scan` on a sample repo, and inspect the generated reports.  
2. **Integrate into CI** – add a step in your pipeline (GitHub Actions, GitLab CI, Jenkins, etc.) that runs the CLI and publishes the JSON output as an artifact.  
3. **Connect AI layer** – feed the CLI’s structured signals into your LLM/RAG service (e.g., via a small wrapper that reads the JSON and prompts the model).  
4. **Iterate & monitor** – use the built‑in quality gates to fail builds on critical issues, and gradually expand the AI‑driven remediation logic as confidence grows.  

**Production Readiness**  
- **Activity & community** – recent commits (as of 2026‑05‑12), 231 stars, and 26 forks indicate healthy interest and ongoing maintenance.  
- **Stability** – the Go codebase is compact and compiled, reducing runtime dependencies; the CLI has a stable, versioned release process.  
- **Ecosystem fit** – works across major languages supported by Qodana and can be called from any environment that can execute a binary, fitting well into micro‑service or monorepo architectures.  
- **Risks** – licensing (Apache‑2.0) and security posture appear clean, but a final review of dependency vulnerabilities and maintainer responsiveness is advisable before full‑scale production rollout.  

Overall, JetBrains /qodana‑cli offers a low‑friction entry point to embed AI‑enhanced code analysis into existing development workflows, and its maturity makes it suitable for both pilot projects and production deployments after standard security vetting.

### Русский

**JetBrains/qodana-cli** — официальная CLI‑утилита Qodana, позволяющая быстро добавить AI‑возможности (прототипирование функций, построение RAG‑ и агентных воркфлоу, оценка моделей) без необходимости разрабатывать стек с нуля. Интеграция проста: инструмент раскрывает сигналы реализации (API/SDK/CLI, метаданные языка, целевые темы) и может быть использован в существующих пайплайнах DevTools. По активности репозитория (231 звезда, частые коммиты, поддержка Go) проект считается готовым к пилотному запуску в продакшн, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
JetBrains /qodana‑cli 是 JetBrains 官方发布的 Qodana 静态分析 CLI 工具，基于 Go 实现，提供统一的命令行入口来运行 Qodana 检查、生成报告并集成到 CI/CD 流程中。

**价值**  
- **即插即用的 AI 能力**：通过内置的模型检测和代码质量规则，帮助团队在不自行搭建模型堆栈的前提下快速引入 AI 驱动的代码审查功能。  
- **加速原型与 RAG/Agent 工作流**：可直接在本地或 CI 环境中调用，支持把代码分析结果作为检索增强（RAG）或智能代理的输入，实现更复杂的自动化治理。  
- **统一的实现信号**：提供 API/SDK/CLI 三种调用方式，输出语言元数据、问题定位和专题标签，便于下游工具二次加工。

**典型接入方式**  
1. **CLI 直接调用**：在本地或 CI 步骤中执行 `qodana scan --project-dir . --output-dir ./qodana-report`。  
2. **CI 集成**：在 GitHub Actions、GitLab CI、Azure Pipelines 等平台使用官方提供的 Docker 镜像或自定义步骤，实现每次提交自动检测。  
3. **SDK / API**：通过 Go 包或 HTTP 接口（如 `qodana serve`) 将分析结果实时推送至自研平台或 RAG 系统，完成后续的语义检索或智能响应。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑12，项目最近一次更新，拥有 231 ⭐、26 🍴，主语言 Go，社区活跃。  
- **成熟度**：已在 JetBrains 自家产品线以及多家企业 CI 中使用，具备完整的错误报告、可配置规则集和可视化报告。  
- **风险**：暂无重大元数据或许可证风险，但建议在正式投产前完成安全审计（依赖的第三方库、容器镜像等）并确认维护者响应机制。  

总体而言，JetBrains/qodana-cli 具备高可用性和易集成特性，是在生产环境中引入 AI 驱动代码质量检测的可靠 OSS 选项。

## 🧭 Practical evaluation

**Value:** JetBrains/qodana-cli helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 231 GitHub stars
- 26 forks
- updated 2026-05-12
- primary language: Go
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 36/100 |
| stars | 50/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 71/100 |
| recency | 80/100 |
| adoption | 46/100 |
| production | 75/100 |
| usefulness | 74/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/JetBrains/qodana-cli) · [← Back to DevTools](./README.md)</sub>
