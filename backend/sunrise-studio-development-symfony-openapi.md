# sunrise-studio-development/symfony-openapi

[![Stars](https://img.shields.io/github/stars/sunrise-studio-development/symfony-openapi?style=flat-square&color=yellow)](https://github.com/sunrise-studio-development/symfony-openapi/stargazers) [![Forks](https://img.shields.io/github/forks/sunrise-studio-development/symfony-openapi?style=flat-square&color=blue)](https://github.com/sunrise-studio-development/symfony-openapi/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> Mentioned in Habr article: Контракт из кода, клиент из контракта: избавляемся от тройного дублирования в API

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 48/100 |
| 🗓️ **Last push** | 2026-07-05 |
| 🔍 **Source** | habr |

## 🏷️ Topics

`habr` `rss`

## 🎯 Categories

Backend

## 📝 Summary

### English

**Project Summary:** 
"Contract from Code, Client from Contract" is an open-source project that aims to eliminate triple duplication in API development by reusing service infrastructure, allowing teams to ship API services faster and standardize service patterns. This project helps teams avoid rebuilding common backend pieces, promoting code reusability and efficiency. By adopting this project, teams can streamline their development workflow and improve product delivery.

**Value Proposition:**
The primary value of this project lies in its ability to help teams reuse service infrastructure, reducing the need to rebuild common backend pieces. This can lead to faster API service delivery, improved code reusability, and standardized service patterns.

**Practical Adoption Path:**

1. **Manual Inspection:** Before adopting the project, teams need to perform a manual inspection to ensure the project's quality and compatibility with their existing infrastructure.
2. **Dependency and Maintenance Checks:** Teams should verify the project's dependencies, maintenance requirements, and release cadence to ensure they can sustain the project in production.
3. **Prototype or Internal Workflow:** Given the project's medium production readiness score, it's recommended to start with a prototype or internal workflow to test and validate the project's effectiveness.

**Production Readiness:**
The project has a medium production readiness score, indicating that it's suitable

### Русский

Резюме проекта "Контракт из кода, клиент из контракта: избавляемся от тройного дублирования в API":

Этот проект позволяет командам повторно использовать инфраструктуру сервиса, вместо того, чтобы каждый раз создавать общие заделки backend. Он помогает командам быстрее развертывать API-сервисы и стандартизировать шаблоны сервисов. Поскольку проект находится в стадии средней готовности, его можно использовать в прототипах или внутренних потоках работы, но перед внедрением необходимо проверить зависимость и поддержку.

### 中文

**项目简介（2‑3 句）**  
“Контракт из кода, клиент из контракта: избавляемся от тройного дублирования в API” 是一套基于代码生成合同（Contract‑from‑code）再反向生成客户端（Client‑from‑contract）的工具链，旨在消除 API 开发、文档和客户端实现之间的三重重复工作。通过统一的合同模型，团队可以在同一源文件中维护接口规范，自动同步生成服务实现骨架、OpenAPI 文档以及对应的 SDK。

**价值**  
- **提升开发效率**：一次编写接口定义，即可自动产出服务端框架、文档和客户端库，显著缩短 API 上线周期。  
- **降低维护成本**：接口变更只需修改合同文件，所有相关代码和文档同步更新，避免因手工同步导致的错误和遗漏。  
- **统一标准**：强制使用统一的合同格式，帮助团队在微服务环境中实现接口风格和错误处理的一致性。

**典型接入方式**  
1. **准备合同文件**：使用项目提供的 DSL（如 TypeScript 接口或 protobuf）编写 API 合同。  
2. **运行生成脚本**：通过 npm/yarn（或对应的 CI 步骤）执行 `generate:contract`，自动生成：  
   - 服务端代码骨架（Express/Koa/FastAPI 等）  
   - OpenAPI/Swagger 文档  
   - 客户端 SDK（JS/TS、Python、Java 等）  
3. **手动审查**：在将生成产物合并到代码库前，进行代码审查和单元测试，确保生成逻辑符合项目规范。  
4. **CI/CD 集成**：将生成步骤写入 CI 流程，确保每次合同变更后自动更新产物并进行回归测试。

**生产可用性**  
- **成熟度**：目前标记为 **Medium**，适合原型、内部工具或对可靠性要求不极端的业务。  
- **使用前检查**：需确认许可证兼容、维护者活跃度、文档完整度以及发布频率；项目的集成信号较少，建议在正式上线前进行充分的单元/集成测试。  
- **风险**：质量信号有限，可能存在未及时修复的 bug；在生产环境使用时应配合内部监控和回滚机制，并对生成的代码进行代码审查。  

总体而言，该项目在加速 API 开发、统一接口规范方面提供了显著价值，但在正式生产环境部署前，建议进行严格的评估和测试，以确保其稳定性和长期可维护性。

## 🧭 Practical evaluation

**Value:** Контракт из кода, клиент из контракта: избавляемся от тройного дублирования в API helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated Sun, 05 Ju
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 56/100 |
| quality | 39/100 |
| recency | 100/100 |
| adoption | 0/100 |
| production | 59/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 70/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/sunrise-studio-development/symfony-openapi) · [← Back to Backend](./README.md)</sub>
