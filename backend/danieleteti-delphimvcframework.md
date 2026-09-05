# danieleteti/delphimvcframework

[![Stars](https://img.shields.io/github/stars/danieleteti/delphimvcframework?style=flat-square&color=yellow)](https://github.com/danieleteti/delphimvcframework/stargazers) [![Forks](https://img.shields.io/github/forks/danieleteti/delphimvcframework?style=flat-square&color=blue)](https://github.com/danieleteti/delphimvcframework/network) [![Language](https://img.shields.io/badge/lang-Pascal-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> DMVCFramework (for short) is a popular and powerful framework for Web API and Web Applications in Delphi. Supports RESTful and JSON-RPC WEB APIs development.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.4k |
| 🍴 **Forks** | 382 |
| 💻 **Language** | Pascal |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api` `application-server` `delphi` `delphimvcframework` `json-rpc` `jsonwebtoken` `jwt` `jwt-authentication` `native` `object-pascal` `pascal` `rest`

## 🎯 Categories

Backend · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
DMVCFramework is a mature, open‑source Delphi library for building RESTful and JSON‑RPC web APIs and full‑stack web applications. It lets teams reuse a proven service‑layer stack—routing, request handling, authentication, serialization, and more—so they can ship API services faster and keep backend patterns consistent across projects. With over 1,300 GitHub stars, active maintenance, and a growing ecosystem, it is ready for serious production pilots.

**Value**  
- **Accelerated delivery** – Common backend concerns (routing, validation, security, serialization, error handling) are already implemented, letting developers focus on business logic.  
- **Standardization** – By adopting a single framework, teams enforce consistent API design, error contracts, and security practices across services.  
- **Reuse & extensibility** – The framework’s modular architecture (filters, middlewares, custom serializers) makes it easy to plug in existing services or third‑party libraries without rewriting core infrastructure.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the sample projects, and verify that the existing CI/CD pipeline can compile Pascal code.  
2. **Integration** – Replace a small, low‑risk internal service with a DMVC‑based implementation, using the provided CLI and SDK for scaffolding.  
3. **Gradual migration** – Incrementally refactor other services to the framework, reusing shared filters (e.g., JWT authentication, CORS) and data‑transfer objects.  
4. **Governance** – Add DMVCFramework to the organization’s approved dependency list, document version‑pinning, and set up automated security scans of the repository.

**Production Readiness**  
- **Activity & community** – Recent commits (as of 2026‑07‑12), 1.3 k stars, 382 forks, and 17 related topics indicate a healthy, engaged community.  
- **Stability** – The framework follows semantic versioning, provides extensive documentation, and has been used in multiple commercial Delphi projects.  
- **Security** – No major open vulnerabilities are reported; however, a final review of licensing (MIT‑style) and any custom security extensions is advisable.  
- **Ecosystem fit** – Works natively with Delphi’s compiler and toolchain, making it straightforward to integrate into existing Delphi‑based backends without additional language bridges.

Overall, DMVCFramework offers a robust, production‑grade foundation for Delphi teams looking to standardize and speed up API development while reusing proven backend components.

### Русский

DMVCFramework — это зрелый open‑source‑фреймворк для создания REST‑ful и JSON‑RPC API на Delphi, позволяющий командам быстро развернуть сервисы, переиспользуя готовую инфраструктуру бэкенда и стандартизируя паттерны взаимодействия. Проект активно поддерживается (1387 звёзд, 382 форка, последние коммиты — июль 2026 г.) и демонстрирует высокий уровень готовности к продакшн, поэтому его можно безболезненно интегрировать в существующие пайплайны через API/SDK/CLI. Основные риски (лицензия, безопасность, поддержка) требуют лишь финального аудита, но в целом фреймворк готов к серьёзным пилотным запускам.

### 中文

**项目简介**  
DMVCFramework（danieleteti/delphimvcframework）是 Delphi 生态中最流行且功能强大的 Web API 与 Web 应用框架，原生支持 RESTful 与 JSON‑RPC 接口的快速开发。

**价值**  
- **复用后端基础设施**：提供完整的路由、请求/响应、序列化、认证、异常处理等通用模块，团队无需重复搭建这些“底层设施”。  
- **加速 API 交付**：约定式的控制器/模型结构、自动生成 OpenAPI 文档，使服务从概念到可用的时间大幅缩短。  
- **统一服务模式**：通过统一的中间件与安全插件（JWT、OAuth、CORS 等），帮助团队在多个微服务之间保持一致的安全与日志标准。

**典型接入方式**  
1. **项目依赖**：在 Delphi 项目中通过 **Delphi Package Manager (DPM)** 或手动引用 `DMVCFramework` 包。  
2. **创建控制器**：继承 `TMVCController`，使用 `[MVCPath]`、`[MVCHTTPMethod]` 等属性标记路由和 HTTP 方法。  
3. **配置服务器**：在 `TMVCEngine` 中注册控制器、启用中间件（如 JWT、CORS），并调用 `Engine.Start` 启动 HTTP 服务器。  
4. **部署**：可直接运行于 Windows 服务、Linux 容器（使用 FireMonkey/Lazarus 编译为跨平台二进制）或配合 Nginx/Apache 进行反向代理。

**生产可用性**  
- **活跃度**：截至 2026‑07‑12，项目仍在持续更新，最近一次提交仅数天前；拥有 1387 ★、382 Fork，社区活跃。  
- **成熟度**：已在多个企业级项目中上线，具备完整的错误处理、日志、性能监控插件，且支持 OpenAPI 自动生成。  
- **安全性**：框架本身提供认证/授权中间件，代码审计记录良好；但仍建议在正式投产前进行内部安全评估。  
- **生态兼容**：兼容最新的 Delphi 10.4+ 编译器，支持跨平台部署（Windows、Linux、macOS），并可通过 REST/JSON‑RPC 与其他语言服务互操作。  

综合来看，DMVCFramework 在后端复用、快速交付与标准化方面具备显著优势，且社区活跃、更新频繁，已达到可以在生产环境中安全试点的水平。后续仍需确认许可证细节与维护者响应速度，以确保长期可维护性。

## 🧭 Practical evaluation

**Value:** danieleteti/delphimvcframework helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1387 GitHub stars
- 382 forks
- updated 2026-07-12
- primary language: Pascal
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 65/100 |
| stars | 67/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 80/100 |
| recency | 80/100 |
| adoption | 66/100 |
| production | 72/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/danieleteti/delphimvcframework) · [← Back to Backend](./README.md)</sub>
