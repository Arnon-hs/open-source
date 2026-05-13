# drogonframework/drogon

[![Stars](https://img.shields.io/github/stars/drogonframework/drogon?style=flat-square&color=yellow)](https://github.com/drogonframework/drogon/stargazers) [![Forks](https://img.shields.io/github/forks/drogonframework/drogon?style=flat-square&color=blue)](https://github.com/drogonframework/drogon/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Drogon: A C++14/17/20 based HTTP web application framework running on Linux/macOS/Unix/Windows

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 13.9k |
| 🍴 **Forks** | 1.3k |
| 💻 **Language** | C++ |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`asynchronous-programming` `drogon` `http` `http-framework` `http-server` `linux` `non-blocking-io`

## 🎯 Categories

Backend

## 📝 Summary

### English

**Summary**  
Drogon is a high‑performance C++14/17/20 web framework for building HTTP APIs that runs on Linux, macOS, Unix, and Windows. With over 13 k GitHub stars and active maintenance, it lets teams reuse proven service infrastructure instead of reinventing common backend components, accelerating API delivery and enforcing consistent service patterns.  

**Value**  
- **Speed to market** – By providing ready‑made routing, request/response handling, JSON support, and async I/O, Drogon cuts the time needed to spin up new micro‑services.  
- **Standardization** – A single, well‑documented framework enforces uniform coding conventions and architectural patterns across multiple services, reducing technical debt and onboarding friction.  
- **Performance & scalability** – Native C++ execution and built‑in coroutine support deliver low latency and high throughput, making it suitable for latency‑sensitive back‑ends.  

**Practical Adoption Path**  
1. **Proof of concept** – Clone the repo, follow the README to build a minimal “Hello World” service, and run it on a dev box to verify toolchain compatibility.  
2. **Pilot service** – Migrate a low‑risk internal API to Drogon, using its code generation and plugin system to replace existing boilerplate.  
3. **Integration checks** – Validate CI/CD pipelines, container images, and security scanning (e.g., Snyk, Dependabot) against the project’s dependencies.  
4. **Gradual rollout** – Extend the pilot to additional services, establishing internal libraries (e.g., authentication middleware) that can be shared across teams.  

**Production Readiness**  
Drogon scores high for production use: recent commits (as of 2026‑05‑13), a large and active community (13 878 stars, 1 337 forks), and multiple platform supports indicate stability and ongoing maintenance. While no major metadata risks have been identified, a final review of the MIT‑style license, vulnerability reports, and maintainer responsiveness is recommended before committing to large‑scale deployments. With these checks completed, Drogon is a solid OSS candidate for serious pilot projects and eventual full‑scale production adoption.

### Русский

**Drogon** — это высокопроизводительный C++‑фреймворк для создания HTTP‑сервисов, позволяющий командам быстро переиспользовать готовую инфраструктуру бекенда вместо написания её с нуля. Типичное внедрение начинается с небольшого proof‑of‑concept, следуя инструкциям в README, после чего сервисы можно масштабировать, стандартизируя паттерны API и ускоряя выпуск новых функций. По оценке проекта (13878 звёзд, активные коммиты, широкая adoption) готовность к продакшн‑использованию высокая, однако требуется окончательная проверка лицензии, безопасности и активности мейнтейнеров.

### 中文

**项目简介**  
Drogon 是一个基于 C++14/17/20 的高性能 HTTP Web 应用框架，支持 Linux、macOS、Unix 与 Windows 多平台运行。它提供了完整的路由、异步 I/O、JSON、WebSocket、数据库等常用后端功能，让开发者可以用现代 C++ 快速构建 API 服务。

**价值**  
- **复用基础设施**：框架封装了网络、序列化、线程池、日志等通用模块，团队无需重复实现这些底层组件。  
- **提升交付速度**：通过约定的路由与控制器写法，可在几行代码内完成接口的定义与实现，显著缩短 API 开发周期。  
- **统一服务模式**：提供统一的异常处理、请求验证、跨域、限流等最佳实践，帮助团队在多个微服务之间保持一致的设计风格。

**典型接入方式**  
1. **阅读 README 与示例**：先克隆仓库，运行 `git submodule update --init` 并参考 `examples` 目录的最小示例。  
2. **创建 CMake 项目**：在 CMakeLists.txt 中加入 `add_subdirectory(drogon)`，并链接 `drogon` 库。  
3. **编写控制器**：继承 `drogon::HttpController`，使用 `GET`, `POST` 等宏注册路由。  
4. **启动服务**：在 `main.cpp` 中调用 `app().addListener("0.0.0.0", 8080).run();`，即可在本地验证。  
5. **小范围 PoC**：先在单机或容器中跑通一个简单的 CRUD 接口，确认编译、部署、监控链路后，再逐步迁移已有服务。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑13，项目拥有 13 878 星、1 337 forks，最近一次提交在当日，说明社区和维护者仍在积极迭代。  
- **跨平台与成熟特性**：支持异步 I/O、HTTP/2、HTTPS、WebSocket、ORM（支持 PostgreSQL、MySQL 等），已在多个大型企业内部使用。  
- **风险点**：仍需对许可证（BSD‑3‑Clause）进行合规审查，评估依赖的第三方库（如 OpenSSL、Boost）的安全更新情况，并确认核心维护者的长期可用性。  
- **结论**：在完成上述合规与安全审查后，Drogon 完全可以作为后端服务的生产候选，适合需要高并发、低延迟且希望统一 C++ 技术栈的团队。

## 🧭 Practical evaluation

**Value:** drogonframework/drogon helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 13878 GitHub stars
- 1337 forks
- updated 2026-05-13
- primary language: C++
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 78/100 |
| stars | 88/100 |
| topics | 88/100 |
| outlook | 87/100 |
| quality | 92/100 |
| recency | 100/100 |
| adoption | 85/100 |
| production | 81/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/drogonframework/drogon) · [← Back to Backend](./README.md)</sub>
