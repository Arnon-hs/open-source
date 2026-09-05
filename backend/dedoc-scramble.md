# dedoc/scramble

[![Stars](https://img.shields.io/github/stars/dedoc/scramble?style=flat-square&color=yellow)](https://github.com/dedoc/scramble/stargazers) [![Forks](https://img.shields.io/github/forks/dedoc/scramble?style=flat-square&color=blue)](https://github.com/dedoc/scramble/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Modern Laravel OpenAPI (Swagger) documentation generator. No PHPDoc annotations required.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.1k |
| 🍴 **Forks** | 200 |
| 💻 **Language** | PHP |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api` `generator` `laravel` `openapi` `swagger`

## 🎯 Categories

Backend

## 📝 Summary

### English

**Summary**  
dedoc/scramble is a modern Laravel OpenAPI (Swagger) documentation generator that creates UI‑ready specs without requiring any PHPDoc annotations. By turning API definitions directly into interactive, reusable front‑end components, it lets teams ship product‑facing interfaces faster and with far less custom UI work.

**Value**  
The tool eliminates the manual effort of writing and maintaining separate UI code for each endpoint, letting developers focus on business logic while the generated UI stays in sync with the API. Because the output is a standard OpenAPI spec, the same definitions can be reused across SDKs, client libraries, and automated testing pipelines, accelerating delivery and reducing inconsistencies between back‑end and front‑end.

**Practical adoption path**  
1. **Add the package** to a Laravel project via Composer.  
2. **Configure** the Scramble service provider to point at your existing route definitions or controller classes.  
3. **Run the CLI** (or use the built‑in API endpoint) to generate the OpenAPI JSON/YAML and the bundled Swagger UI.  
4. **Integrate** the generated UI into your front‑end build (e.g., embed the static files or proxy the UI endpoint).  
5. **Iterate** by updating routes; Scramble re‑generates the spec automatically, keeping documentation and UI current.

**Production readiness**  
The project shows strong OSS signals: 2,138 GitHub stars, 200 forks, recent commits (as of 2026‑07‑12), and active community engagement. Its Laravel‑native design, clear API/CLI exposure, and compliance with the OpenAPI standard make it a viable candidate for a pilot in production environments. While the license, security posture, and maintainer activity still need a final check, the overall health and ecosystem adoption suggest a high degree of readiness for real‑world use.

### Русский

dedoc/scramble — это современный генератор документации OpenAPI (Swagger) для Laravel, который избавляет от необходимости писать PHPDoc‑аннотации, позволяя быстро создавать пользовательские интерфейсы и переиспользовать готовые UI‑компоненты. Проект легко интегрировать через API/SDK/CLI, он уже активно поддерживается (более 2000 звёзд, регулярные обновления) и считается готовым к использованию в продакшене после окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
dedoc/scramble 是一款面向 Laravel 的现代 OpenAPI（Swagger）文档生成器，完全摆脱了 PHPDoc 注解的束缚，只需几行配置即可自动生成完整的 API 文档。

**价值**  
- **快速交付 UI**：通过自动生成的 OpenAPI 规范，前端团队可以直接使用 Swagger UI 或代码生成工具搭建用户界面，显著减少手工编写 UI 的工作量。  
- **组件复用**：统一的接口描述让不同业务线能够共享 UI 组件和 SDK，提升开发效率并降低维护成本。  
- **提升交付质量**：文档与代码同步，避免因文档滞后导致的前后端对接错误。

**典型接入方式**  
1. **Composer 安装**：`composer require dedoc/scramble`。  
2. **在 Laravel 服务提供者中注册**：在 `config/app.php` 的 `providers` 数组里加入 `Dedoc\Scramble\ScrambleServiceProvider::class`。  
3. **配置路由**：在 `routes/web.php` 中加入 `Scramble::routes();`，即可在 `/api-docs`（或自定义路径）访问生成的 Swagger UI。  
4. **可选 CLI/SDK**：通过自带的 `scramble` CLI 导出 JSON/YAML 规范，或直接在代码中调用 `Scramble::generate()` 获取 OpenAPI 对象，便于与 CI/CD、SDK 生成工具集成。

**生产可用性**  
- **活跃度**：截至 2026‑07‑12，项目拥有 2138 ⭐、200+ Fork，最近一次提交仅几天前，表明社区和维护者仍在积极维护。  
- **生态兼容**：基于 Laravel 8/9/10，兼容主流 PHP 版本，且提供标准的 OpenAPI 3.0 输出，易与现有 API 网关、自动化测试及前端代码生成工具对接。  
- **风险评估**：目前未发现重大许可证或安全漏洞风险，但在正式生产前仍建议审查其 LICENSE（MIT）及最新的安全审计报告，确认维护者响应速度符合内部合规要求。  

综上，dedoc/scramble 在文档自动化、前端交付加速以及跨团队协作方面具备显著优势，且社区活跃、更新及时，适合作为生产环境的 API 文档解决方案进行试点或正式上线。

## 🧭 Practical evaluation

**Value:** dedoc/scramble helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2138 GitHub stars
- 200 forks
- updated 2026-07-12
- primary language: PHP
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 71/100 |
| topics | 63/100 |
| outlook | 73/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 67/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/dedoc/scramble) · [← Back to Backend](./README.md)</sub>
