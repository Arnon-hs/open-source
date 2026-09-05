# oss-serverless/osls

[![Stars](https://img.shields.io/github/stars/oss-serverless/osls?style=flat-square&color=yellow)](https://github.com/oss-serverless/osls/stargazers) [![Forks](https://img.shields.io/github/forks/oss-serverless/osls?style=flat-square&color=blue)](https://github.com/oss-serverless/osls/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Serverless Framework CLI v3 alternative

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 626 |
| 🍴 **Forks** | 81 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Cloud & Storage

## 📝 Summary

### English

**Project Summary:**

oss-serverless/osls is an open-source, serverless framework CLI alternative that enables teams to reuse service infrastructure and accelerate API service deployment. By standardizing service patterns, it facilitates faster delivery of backend services. This project is particularly useful for prototypes or internal workflows.

**Value:**

The primary value proposition of oss-serverless/osls lies in its ability to help teams reuse common backend pieces, reducing the need to rebuild infrastructure from scratch. This promotes efficiency and consistency in service development, allowing teams to focus on delivering high-quality services faster.

**Practical Adoption Path:**

To adopt oss-serverless/osls, teams should start with a small proof of concept to evaluate its feasibility. A thorough review of the README documentation is also essential to understand the project's architecture and potential integration points. Once the project is well-understood, teams can begin to integrate it into their existing workflows, starting with small-scale deployments and gradually scaling up to more complex services.

**Production Readiness:**

oss-serverless/osls is considered production-ready for small-scale deployments, such as internal workflows or proof-of-concepts. However, its production readiness is rated as Medium due to the need for dependency and maintenance checks before scaling up to larger, more critical services. While the project has a moderate

### Русский

**oss-serverless/osls** – это открытая альтернатива Serverless Framework CLI v3, позволяющая командам повторно использовать готовую инфраструктуру сервисов вместо постоянного написания одинаковых бекенд‑компонентов. Типичный сценарий — быстрый запуск новых API‑сервисов, стандартизация шаблонов и снижение дублирования кода за счёт общего набора инфраструктурных модулей; рекомендуется начать с небольшого proof‑of‑concept и проверить README. Готовность к продакшну — средняя: проект подходит для прототипов и внутренних процессов, но перед масштабным внедрением стоит оценить зависимости, лицензирование и активность поддержки.

### 中文

**项目简介（2‑3 句）**  
oss-serverless/osls 是一款基于 JavaScript 的 Serverless Framework CLI v3 替代方案，旨在帮助团队复用已有的服务基础设施，避免重复搭建通用的后端组件。通过统一的脚手架与插件体系，开发者可以更快地交付 API 服务，并在团队内部形成一致的服务模式。

**价值**  
- **基础设施复用**：把公共的云资源（如 API Gateway、Lambda、数据库等）抽象为可共享的模块，降低重复工作量。  
- **加速交付**：提供开箱即用的项目模板和 CI/CD 集成脚本，让新服务的搭建时间从数天缩短到数小时。  
- **标准化**：统一的目录结构、配置约定和插件生态帮助团队在多个微服务之间保持一致的开发、部署和运维实践。

**典型接入方式**  
1. **先行评估**：阅读仓库的 README 与快速上手指南，确认其插件和模板是否满足当前云供应商（AWS、Azure、GCP 等）以及语言栈的需求。  
2. **小范围 PoC**：在一个独立的 Git 仓库或内部实验环境中创建一个最小化的服务（如单个 HTTP 接口），使用 `osls init` 初始化项目，完成本地调试后执行 `osls deploy` 部署到测试环境。  
3. **CI/CD 集成**：将 `osls` 命令写入现有的 CI 流水线（GitHub Actions、GitLab CI、Jenkins 等），利用其 `--stage` 参数实现多环境部署。  
4. **逐步迁移**：在验证 PoC 成功后，逐步将已有的 Serverless Framework 项目迁移到 osls，复用其公共基础设施模块。

**生产可用性**  
- **成熟度**：GitHub 目前拥有 626 ★、81 Fork，最近一次提交为 2026‑06‑28，活跃度尚可。适合作为原型、内部工具或非关键业务的后端服务。  
- **风险点**：仍需对许可证（MIT/Apache 等）进行确认，评估其依赖库的安全漏洞（可使用 `npm audit`），并检查维护者的响应速度。  
- **上线建议**：在正式生产前完成以下工作  
  1. 完整的安全审计（依赖、IAM 权限、函数超时等）。  
  2. 监控与日志方案集成（如 CloudWatch、Datadog）。  
  3. 灰度发布或蓝绿部署验证回滚机制。  
  4. 编写内部 SOP，明确谁负责基础设施模块的维护与版本升级。  

综上，oss-serverless/osls 能显著提升团队的后端交付效率，适合先在小范围内部项目中验证，经过安全与运维审查后方可在生产环境稳妥使用。

## 🧭 Practical evaluation

**Value:** oss-serverless/osls helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 626 GitHub stars
- 81 forks
- updated 2026-06-28
- primary language: JavaScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 60/100 |
| topics | 0/100 |
| outlook | 67/100 |
| quality | 60/100 |
| recency | 80/100 |
| adoption | 56/100 |
| production | 65/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/oss-serverless/osls) · [← Back to Cloud--storage](./README.md)</sub>
