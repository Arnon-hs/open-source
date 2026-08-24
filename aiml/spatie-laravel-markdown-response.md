# spatie/laravel-markdown-response

[![Stars](https://img.shields.io/github/stars/spatie/laravel-markdown-response?style=flat-square&color=yellow)](https://github.com/spatie/laravel-markdown-response/stargazers) [![Forks](https://img.shields.io/github/forks/spatie/laravel-markdown-response?style=flat-square&color=blue)](https://github.com/spatie/laravel-markdown-response/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-46%2F100-brightgreen?style=flat-square)](#)

> Serve markdown versions of your HTML pages to AI agents and bots

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 76 |
| 🍴 **Forks** | 7 |
| 💻 **Language** | PHP |
| 📈 **Score** | 46/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `laravel` `markdown` `php`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief summary**  
spatie/laravel-markdown-response is a Laravel package that automatically generates markdown representations of your HTML pages, making them easier for AI agents, bots, and other automated consumers to parse. By adding a simple response macro, you can serve both the original HTML and a clean markdown version without duplicating content or maintaining separate templates.

**Value**  
- **Automation‑first**: Eliminates the tedious step of manually converting HTML to markdown for downstream AI pipelines, reducing human error and speeding up data‑extraction workflows.  
- **Consistency**: Guarantees that the markdown always mirrors the live HTML, so bots always receive up‑to‑date content.  
- **Low overhead**: A single line of code in a controller or route is enough to expose the markdown endpoint, letting you reuse existing Laravel views.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run `composer require spatie/laravel-markdown-response`, and add the provided macro to a test route. Verify that the markdown output matches expectations for a few representative pages.  
2. **Readme & tests review** – Confirm that the package’s test suite passes in your environment and that the README covers configuration (e.g., caching, custom markdown renderers).  
3. **Pilot integration** – Wrap a handful of high‑traffic pages (e.g., product listings, help docs) with the markdown response and point a small AI‑oriented service at the new endpoint.  
4. **Scale** – Once the pilot proves stable, roll the macro out across the site, optionally adding middleware for rate‑limiting or authentication if the markdown is not meant for public consumption.

**Production readiness**  
- **Maturity**: 76 ★ on GitHub, recent update (2026‑06‑26), and a modest fork count indicate an active, maintained project.  
- **Suitability**: Ideal for prototypes, internal tools, or any workflow where markdown consumption is needed; it is not yet a turnkey solution for mission‑critical public APIs without additional safeguards.  
- **Considerations before production**:  
  * Verify dependency compatibility with your Laravel version.  
  * Add monitoring/caching to avoid rendering markdown on every request in high‑traffic scenarios.  
  * Conduct a security review if the markdown endpoint could expose sensitive content.  

Overall, spatie/laravel-markdown-response offers a quick win for automating markdown delivery, with a straightforward proof‑of‑concept path and medium‑level readiness for production after the usual due‑diligence steps.

### Русский

**spatie/laravel-markdown-response** — это пакет для Laravel, который автоматически генерирует markdown‑версии ваших HTML‑страниц, позволяя легко обслуживать AI‑агентов и ботов без ручного копипаста. Типичный сценарий — добавить middleware или отдельный маршрут, включить пакет в небольшом proof‑of‑concept, проверить работу через README и затем интегрировать в существующий pipeline автоматизации (например, в CI/CD или планировщик задач). Готовность к production — средняя: пакет подходит для прототипов и внутренних процессов, но требует проверки зависимостей, тестов и возможных доработок перед масштабным внедрением.

### 中文

**项目简介（2‑3 句话）**  
`spatie/laravel-markdown-response` 是一个 Laravel 扩展，能够在同一路由上同时返回 HTML 与对应的 Markdown 版本，方便 AI 代理、爬虫和聊天机器人直接读取页面内容。它通过拦截响应并自动转换为 Markdown，帮助开发者省去手动编写或维护额外文档的工作。

**价值**  
- **降低重复劳动**：无需为每个页面手动编写 Markdown，框架自动生成，节省人力。  
- **提升 AI 可用性**：AI 代理和搜索爬虫更容易解析 Markdown，提升内容的可检索性和上下文理解。  
- **加速自动化流程**：可直接在 CI/CD、聊天机器人或数据管道中使用 Markdown 输出，实现“内容即服务”。

**典型接入方式**  
1. **安装**：`composer require spatie/laravel-markdown-response`。  
2. **注册服务提供者**（Laravel 5.5+ 可自动发现）：在 `config/app.php` 中添加 `Spatie\LaravelMarkdownResponse\MarkdownResponseServiceProvider::class`（如需手动）。  
3. **中间件或响应宏**：在路由或控制器中使用 `->markdown()` 方法，或在全局中间件里检测 `Accept: text/markdown` 并返回 `MarkdownResponse::make($html)`。  
4. **小范围验证**：先在一个测试路由或内部工具上开启，确认生成的 Markdown 符合预期，再推广到整个站点。  

**生产可用性**  
- **成熟度**：GitHub 76 星、7 Fork，最近一次提交在 2026‑06‑26，代码活跃。  
- **适用场景**：原型、内部工具或对 Markdown 输出有明确需求的业务系统；对外公开的高并发站点仍需评估性能影响。  
- **准备工作**：在生产环境部署前，建议：  
  1. **性能基准**：在负载测试中测量 HTML→Markdown 转换的耗时。  
  2. **依赖审计**：确认所有 PHP 依赖兼容当前 Laravel 版本并无安全漏洞。  
  3. **回滚策略**：提供开关（如环境变量）以在出现问题时快速恢复普通 HTML 响应。  
- **结论**：在经过小规模 POC 验证后，可在内部或低流量的生产环境中安全使用；若计划大规模公开，需进一步进行性能调优和运维监控。

## 🧭 Practical evaluation

**Value:** spatie/laravel-markdown-response helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 76 GitHub stars
- 7 forks
- updated 2026-06-26
- primary language: PHP
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 23/100 |
| stars | 40/100 |
| topics | 50/100 |
| outlook | 49/100 |
| quality | 48/100 |
| recency | 40/100 |
| adoption | 35/100 |
| production | 48/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/spatie/laravel-markdown-response) · [← Back to AI/ML](./README.md)</sub>
