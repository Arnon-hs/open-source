# sindresorhus/p-queue

[![Stars](https://img.shields.io/github/stars/sindresorhus/p-queue?style=flat-square&color=yellow)](https://github.com/sindresorhus/p-queue/stargazers) [![Forks](https://img.shields.io/github/forks/sindresorhus/p-queue?style=flat-square&color=blue)](https://github.com/sindresorhus/p-queue/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Promise queue with concurrency control

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.2k |
| 🍴 **Forks** | 211 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`async-functions` `async-queue` `node-module` `npm-package` `promise` `promise-queue` `queue` `queue-data-stucture`

## 🎯 Categories

Data

## 📝 Summary

### English

Here's a brief summary of the sindresorhus/p-queue project:

sindresorhus/p-queue is an open-source promise queue with concurrency control, designed to convert raw data into searchable, analyzable, or automated pipelines. This project offers a high level of production readiness, making it suitable for serious pilot implementations. Its strong adoption, recent activity, and TypeScript language support make it a practical choice for organizing analytics pipelines, processing datasets, and improving reporting workflows.

In terms of practical adoption, the project's value lies in its ability to streamline data processing and analytics tasks. To adopt this project, start with a small proof of concept and carefully review the README documentation. Evaluate the project's feasibility and potential impact on your specific use case before investing in a larger implementation.

The production readiness of sindresorhus/p-queue is high due to its recent activity, strong adoption (4229 GitHub stars and 211 forks), and ecosystem signals. While some risks remain, such as the need for a final review of the license, security posture, and active maintainers, the project's overall quality signals suggest a solid foundation for a serious pilot implementation.

### Русский

Резюме:

Представляю open-source проект sindresorhus/p-queue - очередь промисов с контролем параллельности. Этот проект позволяет преобразовать необработанные данные в поисковые, анализируемые или автоматизированные потоки, что делает его идеальным решением для организации аналитических потоков, обработки данных и улучшения рабочих процессов отчетности. Проект имеет высокий уровень готовности к production, что делает его достойным к рассмотрению для serious пилота.

### 中文

**项目简介（2‑3 句）**  
`sindresorhus/p-queue` 是一个基于 Promise 的任务队列库，提供并发数限制、优先级和自动重试等功能，让你可以轻松地在 Node.js 或浏览器环境中控制异步任务的执行顺序和并发度。

**价值**  
- **高效资源利用**：通过限制并发数，防止对数据库、API 或磁盘等资源的瞬时冲击，提升系统稳定性。  
- **简化流水线**：把数据抓取、清洗、分析等步骤封装为 Promise，交给 p‑queue 管理，代码更易读、易维护。  
- **灵活调度**：支持任务优先级、任务超时、自动重试等特性，满足复杂的 ETL 与报告自动化场景。

**典型接入方式**  
1. **安装**：`npm i p-queue`（或 `yarn add p-queue`）。  
2. **创建队列**：```ts
import PQueue from 'p-queue';
const queue = new PQueue({ concurrency: 5 }); // 同时最多运行 5 个任务
```  
3. **加入任务**：```ts
await queue.add(() => fetchData(id));   // fetchData 返回 Promise
```  
4. **可选配置**：如 `priority`, `timeout`, `autoStart`, `throwOnTimeout` 等，根据业务需求在构造函数中传入。  
5. **在项目中**：在数据处理、日志收集、邮件发送等需要批量并发控制的模块统一使用同一个 `PQueue` 实例，或为不同子系统创建独立实例。

**生产可用性**  
- **活跃度**：截至 2026‑07‑03 最近一次提交，拥有 4,229 ★、211 forks，社区活跃，Issue 及 PR 反馈迅速。  
- **技术成熟度**：使用 TypeScript 编写，提供完整类型声明，兼容 ES2020+，并已通过多轮 CI 测试。  
- **可靠性**：内置错误重试、超时控制和优先级调度，已在多个开源项目和商业系统中验证。  
- **风险**：仍需审查许可证（MIT）以及潜在的安全依赖（通过 `npm audit`），但整体风险低，适合作为正式生产环境的依赖。  

综上，`p-queue` 具备高并发控制能力、易于集成的 API 与成熟的社区支持，是构建可靠数据处理流水线的理想 OSS 组件。

## 🧭 Practical evaluation

**Value:** sindresorhus/p-queue helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4229 GitHub stars
- 211 forks
- updated 2026-07-03
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 77/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 82/100 |
| recency | 80/100 |
| adoption | 72/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/sindresorhus/p-queue) · [← Back to Data](./README.md)</sub>
