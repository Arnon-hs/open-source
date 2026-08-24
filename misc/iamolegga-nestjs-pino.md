# iamolegga/nestjs-pino

[![Stars](https://img.shields.io/github/stars/iamolegga/nestjs-pino?style=flat-square&color=yellow)](https://github.com/iamolegga/nestjs-pino/stargazers) [![Forks](https://img.shields.io/github/forks/iamolegga/nestjs-pino?style=flat-square&color=blue)](https://github.com/iamolegga/nestjs-pino/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> Platform agnostic logger for NestJS based on Pino with REQUEST CONTEXT IN EVERY LOG

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.5k |
| 🍴 **Forks** | 109 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`hacktoberfest` `logger` `logging` `nest` `nestjs` `pino`

## 🎯 Categories

Misc

## 📝 Summary

### English

iamolegga/nestjs-pino provides a platform‑agnostic NestJS logger built on Pino that automatically injects request context into every log entry, turning scattered logging calls into consistent, traceable output. Teams can adopt it by first running a small proof‑of‑concept (checking the README and integrating the module) and then scaling to full‑agent workflows, tool‑use pipelines, and standardized memory handling. With recent activity, solid adoption metrics (1.5k stars, frequent updates) and strong ecosystem signals, the library is production‑ready for a serious pilot, pending a final review of license, security, and maintainer health.

### Русский

Резюме проекта iamolegga/nestjs-pino:

Проект iamolegga/nestjs-pino представляет собой платформо-нейтральный логгер для NestJS на основе Pino, который обеспечивает контекст запроса в каждой записи журнала. Он помогает превратить изолированные команды и инструменты в повторяемые агентские рабочие процессы. Внедрение проекта может включать в себя координацию многогранных рабочих процессов, добавление пайплайнов использования инструментов и стандартизацию агентской памяти. Проект готов к использованию в production, но требует окончательного обзора лицензии, безопасности и активных мейнтейнеров.

### 中文

**项目简介（2‑3 句话）**  
`iamolegga/nestjs-pino` 是一款基于 Pino 的平台无关日志库，专为 NestJS 设计，能够在每条日志中自动注入请求上下文（trace‑id、user、path 等），实现统一、结构化的日志输出。它以极低的性能开销提供完整的请求链路追踪，适配所有 NestJS 运行模式（HTTP、Microservice、GraphQL 等）。

**价值**  
- **统一上下文**：每条日志自动携带当前请求的唯一标识与元信息，省去手动传递上下文的繁琐。  
- **高性能**：基于 Pino 的异步 JSON 输出，日志写入几乎不影响业务响应时间。  
- **即插即用**：只需在 NestJS 模块中引入一次，即可在全局、控制器、服务乃至自定义拦截器中使用统一的 logger。  
- **便于调试与监控**：结构化日志配合 ELK/ Loki 等日志平台，可快速定位跨服务的调用链路。

**典型接入方式**  

```ts
// app.module.ts
import { Module } from '@nestjs/common';
import { LoggerModule } from 'nestjs-pino';

@Module({
  imports: [
    LoggerModule.forRoot({
      pinoHttp: {
        level: process.env.LOG_LEVEL || 'info',
        redact: ['req.headers.authorization'], // 可选：敏感信息脱敏
        genReqId: (req) => req.headers['x-request-id'] || uuidv4(),
      },
    }),
    // 其它模块…
  ],
})
export class AppModule {}
```

- **全局使用**：在任意服务或控制器中注入 `Logger`（NestJS 自带的 `PinoLogger`）即可直接记录日志，且自动带有 `reqId`、`method`、`url` 等字段。  
- **自定义拦截器**：如需在业务层面添加额外上下文（用户 ID、租户 ID），可编写拦截器通过 `request['context']` 写入 `pino` 的 `extra` 字段。  
- **微服务/GraphQL**：同样通过 `LoggerModule.forRootAsync` 配置，即可在 `ClientProxy`、`Resolver` 中获得统一日志。

**生产可用性**  
- **活跃度**：截至 2026‑06‑30，仓库拥有 1.5k+ 星、100+ 分支，最近一次提交在同月，说明维护活跃。  
- **生态兼容**：纯 TypeScript 实现，兼容 NestJS 9/10，支持 `@nestjs/microservices`、`@nestjs/graphql` 等官方子模块。  
- **性能验证**：Pino 在业界被广泛用于高并发系统，日志写入延迟在毫秒级以下，已在多个大流量生产项目中验证。  
- **风险**：仍需检查许可证（MIT）与安全审计（依赖的 `pino`、`pino-http`），但整体风险低，可直接用于正式环境的日志体系。  

**结论**：`nestjs-pino` 提供了结构化、上下文感知且高性能的日志方案，接入成本低，适合作为 NestJS 项目的生产级日志框架。只需在根模块引入一次，即可在全链路上获得统一的请求上下文，帮助团队实现更高效的故障排查与监控。

## 🧭 Practical evaluation

**Value:** iamolegga/nestjs-pino helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1522 GitHub stars
- 109 forks
- updated 2026-06-30
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 68/100 |
| topics | 75/100 |
| outlook | 56/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 63/100 |
| production | 57/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/iamolegga/nestjs-pino) · [← Back to Misc](./README.md)</sub>
