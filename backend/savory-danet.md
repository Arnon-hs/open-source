# Savory/Danet

[![Stars](https://img.shields.io/github/stars/Savory/Danet?style=flat-square&color=yellow)](https://github.com/Savory/Danet/stargazers) [![Forks](https://img.shields.io/github/forks/Savory/Danet?style=flat-square&color=blue)](https://github.com/Savory/Danet/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> The most mature backend framework for Deno. Create awesome HTTP and WebSocket server as well as KVQueue workers !

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 520 |
| 🍴 **Forks** | 23 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`deno` `dependency-injection` `framework` `hacktoberfest` `ioc` `typescript` `websocket` `websocket-server`

## 🎯 Categories

Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Savory/Danet is a mature, TypeScript‑first backend framework for Deno that lets you spin up HTTP and WebSocket servers and run KVQueue workers with minimal boilerplate. It focuses on reusing common service infrastructure so teams can ship API services faster and standardize backend patterns. With active maintenance, 520 GitHub stars and recent releases, it is ready for a serious pilot in production environments.

**Value**  
- **Infrastructure reuse:** Provides ready‑made abstractions for routing, middleware, WebSocket handling, and KV‑based queue processing, eliminating the need to rebuild these pieces for each service.  
- **Speed to market:** By offering a consistent set of patterns and utilities, developers can focus on business logic, reducing time‑to‑delivery for new APIs.  
- **Standardization:** Enforces a common project structure and conventions across services, making code reviews, onboarding, and cross‑team collaboration smoother.

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC):** Clone the repo, run the example server, and verify that the README instructions work on your CI pipeline.  
2. **Small Service Migration:** Choose a low‑risk internal microservice (e.g., a health‑check or admin endpoint) and rewrite it using Savory/Danet to validate integration with your existing logging, tracing, and KV store.  
3. **Incremental Expansion:** Gradually replace legacy services, leveraging the framework’s built‑in WebSocket and KVQueue modules where appropriate.  
4. **Tooling Alignment:** Add Savory/Danet to your internal template repository, update linting/formatting configs, and publish a versioned internal wrapper if needed.

**Production Readiness**  
- **Activity & Community:** Recent commits (as of 2026‑06‑25), 520 stars, and a modest fork count indicate healthy interest and ongoing maintenance.  
- **Ecosystem Fit:** Written in TypeScript for Deno, it aligns with modern serverless and edge‑runtime stacks; the KVQueue integration matches popular Deno KV providers.  
- **Risk Assessment:** No critical metadata issues detected, though a final review of the license (MIT‑compatible) and a security audit of dependencies is advisable.  
Overall, Savory/Danet meets the criteria for a production‑grade OSS component and is suitable for a pilot that can scale to broader adoption after the PoC phase.

### Русский

Savory/Danet — это зрелый open‑source бэкенд‑фреймворк для Deno, позволяющий быстро собрать HTTP/ WebSocket‑сервисы и KV‑очереди, экономя время на повторной реализации типовых инфраструктурных компонентов. Командам рекомендуется начать с небольшого proof‑of‑concept, проверив README и интеграцию, а затем масштабировать решение для ускоренного вывода API‑сервисов в продакшн. Проект имеет высокий уровень готовности: активные обновления, 520 звёзд на GitHub, стабильный TypeScript‑код и положительные сигналы экосистемы, что делает его надёжным кандидатом для серьёзных пилотов.

### 中文

**项目简介（2‑3 句）**  
Savory/Danet 是面向 Deno 的成熟后端框架，提供完整的 HTTP、WebSocket 服务以及 KVQueue 工作线程。它帮助团队复用已有的服务基础设施，快速搭建高质量的 API 与实时通信系统。

**价值**  
- **复用基础设施**：统一的路由、请求/响应、错误处理、日志、鉴权等模块，避免重复实现。  
- **加速交付**：开箱即用的 WebSocket 与 KVQueue 支持，使实时功能和异步任务能够在几行代码内上线。  
- **标准化**：提供约定好的服务模式（如控制器、服务层、插件），提升团队代码一致性和可维护性。

**典型接入方式**  
1. **阅读 README**，确认兼容的 Deno 版本并安装依赖：`deno run -A https://deno.land/x/savory_danet/install.ts`。  
2. **创建最小示例**：在 `src/main.ts` 中使用 `import { createServer } from "savory/danet"`，定义路由和 WebSocket 处理器，随后运行 `deno task dev`。  
3. **逐步迁移**：在已有项目中先把单一业务模块（如用户登录 API）迁移到 Savory/Danet，验证路由、鉴权和日志是否符合预期，再扩展到 WebSocket 与 KVQueue。  
4. **CI/CD 集成**：利用 Deno 的缓存与锁文件 (`deno.lock`) 将框架版本锁定，确保生产环境与开发环境一致。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑25，GitHub 统计 520 ★、23 Fork，表明社区活跃且持续维护。  
- **成熟度**：框架已实现完整的 HTTP、WebSocket、KVQueue 功能，并提供详细文档与示例，适合作为正式业务的底层框架。  
- **风险**：暂无重大元数据风险，但仍需对许可证（MIT/Apache 等）和安全审计进行最终确认，确保符合企业合规要求。  
- **推荐**：可先在小型 PoC 项目中验证，若结果满意，可直接在生产环境中采用，作为 OSS 候选的后端基础设施。

## 🧭 Practical evaluation

**Value:** Savory/Danet helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 520 GitHub stars
- 23 forks
- updated 2026-06-25
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 58/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 73/100 |
| recency | 80/100 |
| adoption | 51/100 |
| production | 69/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/Savory/Danet) · [← Back to Backend](./README.md)</sub>
