# tempestphp/tempest-framework

[![Stars](https://img.shields.io/github/stars/tempestphp/tempest-framework?style=flat-square&color=yellow)](https://github.com/tempestphp/tempest-framework/stargazers) [![Forks](https://img.shields.io/github/forks/tempestphp/tempest-framework?style=flat-square&color=blue)](https://github.com/tempestphp/tempest-framework/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> The PHP framework that gets out of your way

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.2k |
| 🍴 **Forks** | 171 |
| 💻 **Language** | PHP |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`framework` `mvc` `php`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Tempest Framework is a lightweight, convention‑driven PHP framework that aims to stay out of the way of developers, providing just enough structure to build web applications while letting you write plain PHP code. With a solid community presence (2 238 ★, 171 forks) and recent activity, it can be a good fit for prototypes or internal tools when its design matches your workflow.  

**Value**  
- **Minimal intrusion** – offers routing, DI, and testing helpers without imposing heavy abstractions, so you can keep most of your codebase in vanilla PHP.  
- **Modern PHP features** – leverages attributes, typed properties, and PSR‑compatible components, making it easy to integrate with existing libraries.  
- **Active maintenance** – the repository was updated as of 2026‑06‑27, indicating ongoing support.  

**Practical Adoption Path**  
1. **Evaluate the README and example projects** to confirm that its routing/DI model aligns with your current architecture.  
2. **Spin up a sandbox** (e.g., a fresh Composer project) and run the built‑in skeleton to verify that the framework boots, routes, and runs tests as expected.  
3. **Map dependencies**: check the Composer lock file for third‑party packages, ensure they are compatible with your PHP version, and audit any security advisories.  
4. **Integrate incrementally** – start by using Tempest for a non‑critical module (e.g., an admin panel) before migrating larger parts of the codebase.  

**Production Readiness**  
- **Maturity**: Medium. The framework is stable enough for prototypes and internal services, but it lacks extensive enterprise‑grade tooling (e.g., built‑in monitoring, advanced caching).  
- **Risks**: Integration points are not fully documented in the metadata, so you’ll need to verify configuration, logging, and error‑handling mechanisms manually.  
- **Recommendation**: Adopt for low‑risk projects after a short proof‑of‑concept; for mission‑critical production systems, perform a thorough dependency audit and consider adding supplemental components (e.g., a dedicated logger, health‑check middleware).

### Русский

**Tempest Framework** – лёгкий PHP‑фреймворк, который «не влезает» в ваш код и позволяет быстро собрать прототип или внутренний сервис, используя знакомый набор компонентов без навязывания строгой архитектуры. Подойдёт, если README и активность репозитория совпадают с вашими задачами (например, построение небольших API, микросервисов или админ‑панелей), но перед внедрением стоит проверить процесс установки и совместимость зависимостей, так как путь интеграции из метаданных неочевиден. Готовность к production – средняя: проект имеет значительное сообщество (≈2 к звёзд) и активные обновления, однако требует ручного аудита и тестирования перед запуском в продакшн.

### 中文

**项目简介**  
Tempest Framework（tempestphp/tempest-framework）是一款“让你专注业务、框架不干扰”的轻量级 PHP 框架，旨在提供零侵入式的开发体验，核心功能简洁、约定明确，适合快速搭建原型或内部工具。

**价值点**  
- **低侵入、约定优先**：只提供必要的路由、DI、事件等基础设施，开发者可以按需引入，几乎不需要学习庞大的框架概念。  
- **现代化 PHP 生态**：遵循 PSR 标准，兼容 Composer、PHP 8+ 的属性语法和 async/await（如 Swoole），方便与现有库无缝集成。  
- **活跃社区**：截至 2026‑06‑27 已拥有 2.2k+ Stars、170+ Fork，近期仍在维护，说明社区对其轻量化理念认可度较高。

**典型接入方式**  
1. **Composer 安装**  
   ```bash
   composer require tempestphp/tempest-framework
   ```
2. **创建入口文件**（如 `public/index.php`）  
   ```php
   use Tempest\Tempest;
   require __DIR__.'/../vendor/autoload.php';

   // 自动加载所有 @Controller、@Command 等标记的类
   Tempest::boot()
          ->handleRequest();   // 对 HTTP 请求进行路由分发
   ```
3. **编写业务代码**  
   - 使用 `#[Controller]`、`#[Get('/hello')]` 等属性声明控制器和路由。  
   - 通过 `#[Inject]` 注入服务，利用框架自带的 DI 容器管理依赖。  
   - 如需异步或 CLI，直接使用 `#[Command]` 或 `#[Async]` 属性即可。

4. **可选扩展**  
   - 引入 `tempestphp/tempest-database`、`tempestphp/tempest-auth` 等官方插件，按需增强持久化、鉴权等功能。  
   - 与 Symfony、Laravel 等组件共存，只要遵循 PSR‑4 自动加载即可。

**生产可用性**  
- **成熟度**：项目已更新至 2026‑06‑27，星数和 Fork 数表明社区活跃，核心功能相对稳定。  
- **适用场景**：非常适合内部工具、原型、微服务或对性能/体积有严格要求的项目；对大型、复杂业务（如多租户、复杂事务）仍需自行评估是否需要更完整的生态。  
- **风险与注意事项**  
  - 官方文档和集成案例相对有限，首次接入时需要自行梳理路由、DI、错误处理等细节。  
  - 依赖的第三方插件（如数据库、缓存）需检查其维护状态和兼容性。  
  - 在生产环境部署前，建议完成单元/集成测试、性能基准以及 CI/CD 流程，以确保框架升级不会带来意外破坏。  

**结论**：Tempest Framework 提供了一套“开箱即用、低侵入”的 PHP 开发基石，适合作为快速迭代的内部项目或微服务的技术选型。只要在引入前做好依赖审查和基础设施测试，它可以在生产环境中稳定运行。

## 🧭 Practical evaluation

**Value:** tempestphp/tempest-framework may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2238 GitHub stars
- 171 forks
- updated 2026-06-27
- primary language: PHP
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 71/100 |
| topics | 38/100 |
| outlook | 56/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 67/100 |
| production | 53/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/tempestphp/tempest-framework) · [← Back to Misc](./README.md)</sub>
