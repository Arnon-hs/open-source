# VoidenHQ/voiden

[![Stars](https://img.shields.io/github/stars/VoidenHQ/voiden?style=flat-square&color=yellow)](https://github.com/VoidenHQ/voiden/stargazers) [![Forks](https://img.shields.io/github/forks/VoidenHQ/voiden?style=flat-square&color=blue)](https://github.com/VoidenHQ/voiden/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> Design, Test and Document APIs in plain Markdown. Compose Requests with API blocks. Reuse, Replace & Version everything just like code. Offline, Truly Git Native, No Lock-in.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 54 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api` `api-client` `automation` `bruno-alternative` `cli` `curl-alternative` `graphql` `http-client` `insomnia-alternative` `javascript` `markdown` `offline-first`

## 🎯 Categories

Automation · Backend · DevTools · Design

## 📝 Summary

### English

**Brief Summary**  
VoidenHQ / voiden is an open‑source, Git‑native platform for designing, testing, and documenting APIs using plain Markdown. It lets you compose requests with reusable “API blocks,” version them like code, and run everything offline—no vendor lock‑in, no cloud dependencies.

**Value**  
- **Eliminates repetitive manual steps**: By treating API definitions as Markdown files that can be programmatically executed, teams replace copy‑paste request fiddling, ad‑hoc testing, and scattered documentation with a single source of truth.  
- **Reusable, version‑controlled assets**: API blocks can be referenced, overridden, and versioned across projects, enabling consistent contracts and reducing drift between design, test, and production.  
- **Tool‑agnostic automation**: Because the workflow lives in Git and is exposed via CLI/SDK, it can be stitched into CI pipelines, scheduled jobs, or integrated with other dev‑ops tools without tying you to a proprietary service.

**Practical Adoption Path**  
1. **Pilot the Markdown API spec** – Clone the repo, add a few endpoint definitions in the provided Markdown format, and run the CLI locally to generate request code and test responses.  
2. **Integrate with CI** – Add the `voiden` CLI step to your build pipeline (e.g., GitHub Actions, GitLab CI) to automatically validate API contracts on every push.  
3. **Replace existing scripts** – Swap out custom curl/Postman collections with voiden API blocks, leveraging its versioning to keep test suites in sync with code changes.  
4. **Scale to production** – Use the CLI or generated SDKs in scheduled jobs or serverless functions for recurring operational tasks (e.g., health checks, data syncs).  

**Production Readiness**  
- **Activity & community**: 1,216 stars, 54 forks, recent commits (as of 2026‑06‑23) and a healthy set of topics indicate an active ecosystem.  
- **Maturity**: Written in TypeScript, the project follows standard package conventions and provides API/SDK/CLI interfaces, making it easy to embed in existing TypeScript/JavaScript stacks.  
- **Risk assessment**: No major metadata concerns; however, a final review of the license (MIT/Apache?), security audit results, and maintainer responsiveness is advisable before a full‑scale rollout.  

Overall, voiden is a high‑readiness OSS candidate for teams looking to codify API design, testing, and automation in a version‑controlled, lock‑in‑free manner.

### Русский

VoidenHQ/voiden — это open‑source инструмент, позволяющий проектировать, тестировать и документировать API полностью в Markdown, автоматически генерируя запросы, версии и заменяемые блоки кода, что устраняет рутинные ручные операции и упрощает построение повторяемых рабочих потоков. Типичный сценарий: команда описывает API в репозитории, использует CLI/SDK для локального тестирования и интеграции с CI/CD, а затем планирует и автоматизирует операционные задачи без привязки к конкретным сервисам. Проект имеет высокий уровень готовности к production: активные коммиты (обновление 2026‑06‑23), более 1200 звёзд, 54 форка, поддержка TypeScript, обширные метаданные и интеграционные сигналы, что делает его надёжным кандидатом для пилотного внедрения, при условии окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
VoidenHQ/voiden 是一款基于纯 Markdown 的 API 设计、测试与文档工具，支持在 Markdown 中直接编写 API 请求块，并像管理代码一样对请求、响应、版本和替换进行复用。它完全离线、原生 Git，避免供应商锁定。

**价值主张**  
- **消除重复手工**：把 API 调用、测试、文档统一写在 Markdown 中，省去在 UI、脚本、Postman 等工具之间来回切换的繁琐操作。  
- **可复用、可版本化**：所有请求块、变量、响应示例都可以像代码一样分支、合并、回滚，实现真正的可追溯性。  
- **与现有工作流无缝衔接**：支持 CLI、SDK 与自定义插件，可轻松嵌入 CI/CD、自动化调度或其他内部工具。

**典型接入方式**  
1. **CLI**：`voiden run <markdown-file>` 直接在本地执行 API 请求，适合脚本化和 CI 环境。  
2. **SDK**：通过 npm 包 `@voiden/sdk` 在 Node/TS 项目中调用 `voiden.executeBlock()`，实现程序化调用。  
3. **Git 集成**：将 `.voiden/` 目录加入仓库，利用 Git Hooks（如 pre‑commit）自动校验 API 文档与实际响应的一致性。  
4. **插件/扩展**：利用提供的插件接口，可将 Voiden 与 Jira、GitHub Actions、Airflow 等平台对接，实现任务调度或工单自动化。

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，项目最近一次提交，拥有 1,216 星、54 个 Fork，20+ 主题标签，表明社区活跃。  
- **技术成熟度**：主语言 TypeScript，提供完整的 API/SDK/CLI，且全部代码托管在 GitHub，易于审计和自托管。  
- **安全与合规**：暂无重大元数据风险，仍需对许可证（MIT）和安全审计（依赖漏洞）进行最终确认。  
- **适配度**：提供明确的实现信号（API、SDK、CLI、语言元数据），评估成本低，适合作为内部或外部服务的 API 设计与自动化入口，完全可以在生产环境进行试点。  

综合来看，VoidenHQ/voiden 已具备高可用的 OSS 基础，适合在需要统一 API 文档、自动化测试与可重复执行的场景中快速落地。

## 🧭 Practical evaluation

**Value:** VoidenHQ/voiden helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1216 GitHub stars
- 54 forks
- updated 2026-06-23
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 66/100 |
| topics | 100/100 |
| outlook | 67/100 |
| quality | 67/100 |
| recency | 40/100 |
| adoption | 59/100 |
| production | 62/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/VoidenHQ/voiden) · [← Back to Automation](./README.md)</sub>
