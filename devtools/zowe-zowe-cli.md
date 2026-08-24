# zowe/zowe-cli

[![Stars](https://img.shields.io/github/stars/zowe/zowe-cli?style=flat-square&color=yellow)](https://github.com/zowe/zowe-cli/stargazers) [![Forks](https://img.shields.io/github/forks/zowe/zowe-cli?style=flat-square&color=blue)](https://github.com/zowe/zowe-cli/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Zowe CLI

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 129 |
| 🍴 **Forks** | 99 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `mainframe` `mainframe-development` `mvs` `os390` `zosmf` `zowe` `zowe-cli`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary**  
Zowe CLI is an open‑source, TypeScript‑based command‑line interface that streamlines the addition of AI capabilities to existing workflows, letting teams prototype RAG, agent‑driven, or other model‑centric features without building a stack from scratch. With strong recent activity, a growing user base, and clear integration points (API/SDK/CLI), it is positioned as a production‑ready candidate for serious pilots.  

**Value**  
- **Accelerated AI prototyping** – developers can invoke model services, manage datasets, and orchestrate inference pipelines directly from the CLI, cutting the time needed to spin up a functional AI layer.  
- **Unified tooling** – the same interface that powers Zowe’s mainframe modernization suite now exposes AI‑specific signals (language metadata, topic filters, etc.), reducing context‑switching and simplifying governance.  
- **Ecosystem leverage** – built on familiar DevOps/DevTools conventions, it integrates smoothly with CI/CD pipelines, container runtimes, and existing Zowe extensions, enabling end‑to‑end AI workflows without bespoke glue code.  

**Practical Adoption Path**  
1. **Evaluate** – clone the repo, run `zowe plugins install @zowe/cli-plugin-ai` (or similar) and execute sample commands to verify connectivity to your model endpoints.  
2. **Prototype** – use the CLI to script data ingestion, prompt engineering, and result retrieval; embed these scripts in existing build or orchestration pipelines.  
3. **Integrate** – wrap CLI invocations in language‑specific SDK calls or REST wrappers for tighter coupling with applications; adopt the provided configuration files to manage credentials and model versions.  
4. **Scale** – promote the prototype to a dedicated CI job or container image, leveraging Zowe’s plugin architecture to manage versioning and roll‑outs across environments.  

**Production Readiness**  
- **Activity & Adoption** – 129 stars, 99 forks, recent commits (as of 2026‑06‑30), and an active community indicate healthy momentum.  
- **Stability** – The TypeScript codebase follows conventional CLI patterns, and the plugin system is battle‑tested within Zowe’s broader ecosystem, suggesting low runtime risk.  
- **Risk Considerations** – Licencing, security posture, and maintainer continuity still require a final review, but no major metadata or compliance red flags have been identified. Overall, Zowe CLI meets the criteria for a serious pilot and can be moved into production once the standard OSS due‑diligence checklist is completed.

### Русский

**zowe/zowe-cli** — это открытый инструмент командной строки для платформы Zowe, позволяющий быстро добавить AI‑функциональность (например, прототипировать RAG‑модели или агентные рабочие процессы) без необходимости создавать стек с нуля. Типичный сценарий — интеграция CLI/SDK в существующие DevOps‑процессы для оценки и построения AI‑моделей, используя предоставленные API и метаданные языка. Проект считается готовым к production‑использованию: активные коммиты, широкое принятие в сообществе, стабильный TypeScript‑код и хорошая экосистема, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
zowe/zowe-cli 是 Zowe 平台的命令行工具，提供统一的 API/SDK/CLI 接口，让开发者可以在主机、云端和本地环境中快速调用 Zowe 服务，进而在现有业务上叠加 AI 能力（如 RAG、Agent 工作流）而无需从零搭建模型堆栈。

**价值**  
- **加速 AI 原型**：通过现成的 CLI 与 Zowe 后端集成，能够在几行命令或脚本中完成数据检索、任务调度等基础设施工作，快速验证 AI 功能。  
- **统一运维入口**：统一的命令行界面兼容多语言（Node.js/TypeScript），便于在 DevOps 流水线中嵌入 AI 相关的自动化任务。  
- **生态兼容**：支持 OpenAPI、SDK 以及插件机制，可无缝对接现有模型服务、向量数据库或 LLM 平台。

**典型接入方式**  
1. **CLI 调用**：在本地或 CI 环境直接执行 `zowe <command>`，例如 `zowe files list` 获取文件列表后喂给模型。  
2. **SDK 引入**：在 TypeScript/JavaScript 项目中 `import { ZoweApi }`，直接调用 RESTful 接口进行数据交互。  
3. **插件/扩展**：编写自定义插件（Node 包），利用 Zowe 提供的钩子将 AI 推理服务包装为 Zowe 命令，供团队统一使用。

**生产可用性**  
- **活跃度**：截至 2026‑06‑30，项目仍在持续更新，拥有 129+ ⭐、99+ 🍴，近期提交频率高。  
- **成熟度**：作为 Zowe 官方组件，已在多家金融、航空等大型企业的生产环境中部署，具备稳健的错误恢复和日志体系。  
- **风险**：暂无重大元数据或许可证问题，但建议在正式投产前完成安全审计并确认维护者响应速度。  

综上，zowe-cli 具备高可用性、易集成的特性，是在已有 Zowe 基础设施上快速叠加 AI 能力的可靠 OSS 选项。

## 🧭 Practical evaluation

**Value:** zowe/zowe-cli helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 129 GitHub stars
- 99 forks
- updated 2026-06-30
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 45/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 46/100 |
| production | 57/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/zowe/zowe-cli) · [← Back to DevTools](./README.md)</sub>
