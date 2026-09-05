# zircote/swagger-php

[![Stars](https://img.shields.io/github/stars/zircote/swagger-php?style=flat-square&color=yellow)](https://github.com/zircote/swagger-php/stargazers) [![Forks](https://img.shields.io/github/forks/zircote/swagger-php?style=flat-square&color=blue)](https://github.com/zircote/swagger-php/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> A php swagger annotation and parsing library

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.3k |
| 🍴 **Forks** | 938 |
| 💻 **Language** | PHP |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary:** zircote/swagger-php is an open-source PHP library for Swagger annotation and parsing, offering a useful tool for developers when integrated into a specific workflow. However, its adoption requires manual inspection and validation of setup costs due to sparse integration signals. With 5299 GitHub stars and a relatively recent update, it has a moderate level of production readiness.

**Value Proposition:** The library's value lies in its ability to facilitate Swagger-based workflows, making it a potential fit for projects that rely on Swagger annotations for API documentation and integration. Its open-source nature and moderate popularity suggest that it may be a reliable choice for certain use cases.

**Practical Adoption Path:**

1. **Manual Inspection**: Before adopting zircote/swagger-php, developers should carefully review the library's documentation and code to understand its integration path and potential pitfalls.
2. **Validate Setup Costs**: Validate the setup costs and potential maintenance requirements for the library to ensure it aligns with the project's needs and resources.
3. **Integration Testing**: Conduct thorough integration testing to ensure the library works as expected in the specific workflow.

**Production Readiness:** With a moderate level of production readiness (Medium), zircote/swagger-php is suitable for prototypes or internal workflows. However, it may not be the best choice for production

### Русский

**zircote/swagger-php** — это библиотека на PHP, позволяющая описывать API через Swagger‑аннотации и генерировать спецификации OpenAPI. Она подходит для быстрого прототипирования и внутренних проектов, где требуется автоматическое документирование без отдельного инструмента, но перед выводом в продакшн следует проверить совместимость с текущим стеком и оценить нагрузку на сборку, так как интеграционный путь не полностью описан в метаданных. При достаточной проверке зависимостей и процесса генерации библиотека считается готовой к использованию в продуктиве со средним уровнем риска.

### 中文

**项目简介（2‑3 句）**  
zircote/swagger-php 是一款基于 PHP 注解的 Swagger（OpenAPI）文档生成库，能够在代码中直接使用 `@OA\*` 注解描述 API 接口，并在运行时自动解析生成符合 OpenAPI 规范的 JSON/YAML 文档。它在社区中拥有 5.3k+ 星、近 1k 次 Fork，维护活跃，适合在 PHP 项目中快速构建可机器读取的 API 文档。

**价值**  
- **代码即文档**：通过注解把接口说明写在源码里，保持实现与文档同步，降低文档失效风险。  
- **标准化输出**：生成的文档完全符合 OpenAPI 3.x 规范，可直接用于 Swagger UI、Redoc、Postman 等工具，支持自动化测试和 SDK 生成。  
- **生态兼容**：与主流框架（Laravel、Symfony、Slim 等）兼容，只需在项目的 Composer 中加入依赖即可使用。

**典型接入方式**  
1. **Composer 安装**  
   ```bash
   composer require zircote/swagger-php
   ```
2. **在代码中添加注解**（示例）  
   ```php
   /**
    * @OA\Get(
    *     path="/api/users/{id}",
    *     summary="获取单个用户",
    *     @OA\Parameter(
    *         name="id",
    *         in="path",
    *         required=true,
    *         @OA\Schema(type="integer")
    *     ),
    *     @OA\Response(
    *         response=200,
    *         description="成功返回用户信息",
    *         @OA\JsonContent(ref="#/components/schemas/User")
    *     )
    * )
    */
   public function getUser(int $id) { … }
   ```
3. **生成文档**（CLI）  
   ```bash
   ./vendor/bin/openapi --output ./public/swagger.json ./src
   ```
   将生成的 `swagger.json` 或 `swagger.yaml` 部署到静态路径，配合 Swagger UI 即可在线预览。

4. **在框架中集成**（以 Laravel 为例）  
   - 在 `AppServiceProvider::boot()` 中调用 `\OpenApi\Generator::scan([app_path()])`，并将结果缓存。  
   - 路由返回生成的 JSON：  
     ```php
     Route::get('/api-docs', fn() => response()->json(\OpenApi\Generator::scan([app_path()])));
     ```

**生产可用性**  
- **成熟度**：中等偏上。拥有大量星标和活跃的维护者，最近一次提交在 2026‑06‑29，代码质量和兼容性都较为可靠。  
- **适用场景**：非常适合内部系统、原型项目以及需要快速生成 OpenAPI 文档的业务；在对外公开的微服务或需要 SDK 自动生成的场景也可使用。  
- **风险与注意事项**  
  - **集成成本**：库本身不提供框架级别的自动装配，需要自行在项目启动时调用扫描生成，或编写少量包装代码。  
  - **依赖管理**：确保项目的 PHP 版本（>=7.4）与库的依赖兼容，定期检查 Composer 更新以避免安全漏洞。  
  - **文档完整性**：注解必须完整覆盖所有接口，否则生成的 OpenAPI 文档会出现空缺；建议在 CI 中加入生成文档的步骤并对比变更。  

综上，zircote/swagger-php 在需要统一、可机器读取的 API 文档时是一把“轻量级”利器，只要做好注解维护和 CI 检查，就可以在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** zircote/swagger-php may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 5299 GitHub stars
- 938 forks
- updated 2026-06-29
- primary language: PHP

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 74/100 |
| stars | 79/100 |
| topics | 0/100 |
| outlook | 66/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 78/100 |
| production | 66/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/zircote/swagger-php) · [← Back to Misc](./README.md)</sub>
