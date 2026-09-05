# jwt-scala/jwt-scala

[![Stars](https://img.shields.io/github/stars/jwt-scala/jwt-scala?style=flat-square&color=yellow)](https://github.com/jwt-scala/jwt-scala/stargazers) [![Forks](https://img.shields.io/github/forks/jwt-scala/jwt-scala?style=flat-square&color=blue)](https://github.com/jwt-scala/jwt-scala/network) [![Language](https://img.shields.io/badge/lang-Scala-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> JWT support for Scala. Bonus extensions for Play, Play JSON, Json4s, Circe, uPickle, Spray and Argonaut

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 676 |
| 🍴 **Forks** | 143 |
| 💻 **Language** | Scala |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`jwt` `jwt-scala` `scala`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`jwt-scala/jwt-scala` is a lightweight, pure‑Scala library that implements JSON Web Token (JWT) creation, signing, verification, and claims handling. It ships with optional adapters for popular Scala ecosystems such as Play, Play‑JSON, Json4s, Circe, uPickle, Spray, and Argonaut, making it easy to plug JWT support into existing codebases. With over 670 stars and recent activity, it is a mature community‑driven option for projects that need token‑based authentication without pulling in heavyweight Java dependencies.

**Value**  
- **Unified API**: One core JWT implementation with a consistent API across multiple JSON libraries, reducing the learning curve and avoiding duplicated code.  
- **Ecosystem Flexibility**: Choose the JSON binding that matches your stack (Play, Circe, etc.) and simply import the corresponding extension module.  
- **Lightweight & Pure Scala**: No transitive Java JWT libraries, which keeps the dependency graph clean and improves compile‑time performance.  

**Practical Adoption Path**  
1. **Evaluate Compatibility** – Verify that the JSON library you already use (e.g., Circe) has a matching extension in the repo.  
2. **Add Dependency** – Include the core `jwt-scala` artifact and the specific extension (e.g., `jwt-circe`) in your `build.sbt`.  
3. **Prototype** – Write a small proof‑of‑concept that creates a token, signs it with your chosen algorithm (HS256, RS256, etc.), and validates it using the library’s `Jwt` objects.  
4. **Security Review** – Check the supported algorithms, key‑handling utilities, and ensure you are using recommended defaults (e.g., RSA/ECDSA for production).  
5. **Integrate** – Replace any ad‑hoc JWT handling in your codebase with the library’s API, wiring it into your authentication middleware (Play filters, Akka HTTP directives, etc.).  

**Production Readiness**  
- **Maturity**: The project has a solid star count (676) and recent commits (as of 2026‑05‑11), indicating an active community.  
- **Stability**: Core JWT functionality is well‑tested; the optional adapters are thin wrappers, but you should validate them against your exact JSON library version.  
- **Risk Level**: Medium. Suitable for prototypes, internal services, or production workloads after a brief audit of licensing (MIT‑style), security posture (algorithm support), and maintainer activity. Perform a dependency‑vulnerability scan and consider pinning versions to avoid accidental breaking changes.  

In short, `jwt-scala/jwt-scala` offers a convenient, Scala‑native JWT solution that can be adopted quickly for most Scala projects, provided you perform the usual due‑diligence checks before promoting it to mission‑critical production environments.

### Русский

**jwt-scala/jwt-scala** — это open‑source библиотека, предоставляющая полную поддержку JWT в проектах на Scala и набор удобных адаптеров для популярных JSON‑библиотек (Play, Play‑JSON, Json4s, Circe, uPickle, Spray, Argonaut). Она отлично подходит для быстрого прототипирования или внутренних сервисов, где требуется генерация и валидация токенов, но перед выводом в продакшн следует проверить совместимость зависимостей, актуальность лицензии и убедиться в наличии активных мейнтейнеров. В текущем виде проект имеет средний уровень готовности — много звёзд и недавнее обновление, однако интеграцию рекомендуется пройти через ручную оценку.

### 中文

**项目简介**  
`jwt-scala/jwt-scala` 是一套在 Scala 生态下使用 JSON Web Token（JWT）的库，核心模块提供标准的 JWT 编码、解码与验证功能，并额外提供针对 Play、Play‑JSON、Json4s、Circe、uPickle、Spray、Argonaut 等流行框架/序列化库的扩展，使得在不同的 Scala 项目中几乎可以“即插即用”。  

---

## 价值点  

| 价值 | 说明 |
|------|------|
| **统一的 JWT API** | 只需引入核心库即可在纯 Scala、Akka HTTP、Play 等多种环境中生成、解析、校验 JWT，避免在不同项目中重复实现。 |
| **丰富的序列化适配** | 通过专门的扩展模块，直接支持 Play JSON、Circe、Json4s、uPickle、Spray‑JSON、Argonaut 等常用 JSON 序列化框架，省去手动转换的繁琐。 |
| **社区认可** | 目前拥有 676+ ⭐、143+ 🍴，活跃度仍在（最近一次提交 2026‑05‑11），说明在 Scala 社区中已有一定的使用基础。 |
| **易于原型与内部工具** | 依赖仅限于 Scala 标准库和常见 JSON 库，集成成本低，适合快速搭建认证原型或内部服务。 |

---

## 典型接入方式  

1. **在 `build.sbt` 中添加依赖**（以 Play‑JSON 为例）  
   ```scala
   libraryDependencies ++= Seq(
     "com.github.jwt-scala" %% "jwt-core"      % "9.0.0",
     "com.github.jwt-scala" %% "jwt-play-json" % "9.0.0"
   )
   ```
2. **生成 Token**  
   ```scala
   import pdi.jwt.{JwtAlgorithm, JwtClaim, JwtJson}
   import play.api.libs.json.Json

   val claim = JwtClaim(
     expiration = Some(System.currentTimeMillis() / 1000 + 3600),
     issuedAt   = Some(System.currentTimeMillis() / 1000)
   ).+("userId", "12345")

   val token = JwtJson.encode(claim, "your-secret-key", JwtAlgorithm.HS256)
   ```
3. **验证 & 解析**  
   ```scala
   val decoded = JwtJson.decodeJson(token, "your-secret-key", Seq(JwtAlgorithm.HS256))
   decoded match {
     case Success(json) => // json: JsValue，直接使用 Play‑JSON 读取字段
     case Failure(ex)   => // token 无效或已过期
   }
   ```
4. **在框架中集成**（以 Play Filter 为例）  
   ```scala
   class JwtAuthFilter @Inject()(implicit ec: ExecutionContext) extends Filter {
     def apply(next: RequestHeader => Future[Result])
              (rh: RequestHeader): Future[Result] = {
       rh.headers.get("Authorization").flatMap(_.stripPrefix("Bearer ").some) match {
         case Some(token) if JwtJson.isValid(token, "your-secret-key") => next(rh)
         case _ => Future.successful(Results.Unauthorized("Invalid token"))
       }
     }
   }
   ```

> **提示**：如果项目使用的是 Circe、Json4s、uPickle 等其他 JSON 序列化库，只需替换 `jwt-play-json` 为对应的扩展模块（如 `jwt-circe`），API 基本保持一致。

---

## 生产可用性评估  

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | 中等 | 已有数年历史、数百星、近期提交，适合原型和内部系统；但相对于更大型的 JWT 库（如 `auth0/java-jwt`），社区插件、issue 处理速度略慢。 |
| **依赖与维护** | 需要自行审查 | 依赖仅限于 Scala 标准库和对应 JSON 库，整体体积小；建议在引入前检查所使用的扩展模块的最新版本和安全报告。 |
| **安全性** | 需要自行验证 | 库本身实现了标准的 HS256/RS256 等算法，但未提供官方的安全审计报告；在生产环境中应配合安全扫描工具（如 Snyk、OWASP Dependency‑Check）并自行进行渗透测试。 |
| **易用性** | 高 | API 简洁、与常用框架深度集成，文档（README）覆盖了核心使用场景。 |
| **可扩展性** | 良好 | 支持自定义 `JwtAlgorithm`、自定义 `JwtHeader`，并且可以自由切换底层 JSON 序列化实现。 |
| **推荐场景** | - 快速原型<br>- 内部微服务之间的轻量身份验证<br>- 与 Play、Akka HTTP、http4s 等 Scala Web 框架的统一认证 | 对于对安全合规要求极高的外部面向用户的生产系统，建议在评估完安全审计、监控和密钥管理方案后再决定是否正式采用。 |

**结论**：`jwt-scala/jwt-scala` 在功能完整性和 Scala 生态兼容性方面表现出色，适合作为内部项目或原型的 JWT 解决方案。若计划在面向客户的生产环境中使用，建议在引入前完成以下步骤：  

1. **安全审计**（检查已知 CVE、依赖漏洞）。  
2. **密钥管理**（使用 HSM、Vault 或云 KMS 替代硬编码密钥）。  
3. **高可用部署**（在负载均衡层或网关统一校验，避免每个服务重复实现）。  

完成上述准备后，即可在生产环境中安全、稳定地使用该库。

## 🧭 Practical evaluation

**Value:** jwt-scala/jwt-scala may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 676 GitHub stars
- 143 forks
- updated 2026-05-11
- primary language: Scala
- 3 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 60/100 |
| topics | 38/100 |
| outlook | 65/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 58/100 |
| production | 67/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/jwt-scala/jwt-scala) · [← Back to Misc](./README.md)</sub>
