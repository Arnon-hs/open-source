# typelevel/cats-tagless

[![Stars](https://img.shields.io/github/stars/typelevel/cats-tagless?style=flat-square&color=yellow)](https://github.com/typelevel/cats-tagless/stargazers) [![Forks](https://img.shields.io/github/forks/typelevel/cats-tagless?style=flat-square&color=blue)](https://github.com/typelevel/cats-tagless/network) [![Language](https://img.shields.io/badge/lang-Scala-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Library of utilities for tagless final encoded algebras

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 319 |
| 🍴 **Forks** | 41 |
| 💻 **Language** | Scala |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-07-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`functional-programming` `scala` `tagless`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Project Summary:**

The typelevel/cats-tagless project is an open-source library of utilities for tagless final encoded algebras, primarily written in Scala. While it has a relatively low score of 54/100, its 319 GitHub stars and 41 forks indicate a moderate level of interest and adoption. This project may be useful for specific workflows that align with its README and activity, but requires careful evaluation and integration.

**Value Proposition:**

The typelevel/cats-tagless project offers a set of utilities for working with tagless final encoded algebras, which can be beneficial for developers who need to implement this design pattern in their projects. Its primary value lies in its ability to simplify the process of encoding and working with algebras, making it a useful tool for specific workflows.

**Practical Adoption Path:**

Before adopting the typelevel/cats-tagless project, it's essential to carefully evaluate its README and activity to ensure it aligns with your specific workflow. Manual inspection of the project's integration signals is necessary to understand the integration path and potential setup costs. Once you've validated the setup cost, you can consider committing to the project.

**Production Readiness:**

The typelevel/cats-tagless project is considered to have medium production readiness, indicating

### Русский

typelevel/cats-tagless — это набор утилит для работы с алгебрами в стиле tagless final на Scala, который упрощает определение и композицию DSL‑ов, позволяя писать типобезопасный, легко тестируемый код без необходимости создавать отдельные интерпретаторы. Его обычно подключают в прототипах или внутренних сервисах, где уже используется Cats и требуется гибкая абстракция над эффектами; перед переходом в продакшн стоит проверить совместимость с текущей сборкой и оценить нагрузку от дополнительных зависимостей. По уровню готовности проект считается средним: имеет активную поддержку (обновления до 2026‑07‑12, 319 ★, 41 форк), но детали интеграции не описаны подробно, поэтому требуется ручная проверка перед масштабным внедрением.

### 中文

**简短介绍**  
`typelevel/cats-tagless` 是一个基于 **Tagless Final** 编码风格的 Scala 库，提供一系列实用工具（如 `FunctorK`、`InjectK`、`Derived` 等）帮助你快速构建、组合和解释代数（Algebra）接口。它与 Cats 生态深度集成，旨在让函数式抽象既保持类型安全，又保持可组合性和可测试性。

---

## 价值（Value Proposition）

| 维度 | 说明 |
|------|------|
| **抽象与解耦** | 通过 Tagless Final，将业务 algebras 与具体实现解耦，能够在同一代码基上轻松切换实现（比如 mock、生产实现、远程调用）。 |
| **可组合性** | 提供 `FunctorK`、`InjectK`、`SemigroupK` 等 type‑class，使不同 algebras 能在同一个 Free‑like 结构中自由组合。 |
| **与 Cats 兼容** | 完全基于 Cats 类型类，能够直接使用现有的 `Applicative`, `Monad`, `Parallel` 等实例，无需额外适配层。 |
| **编译期安全** | 所有转换在编译期完成，避免运行时的反射或错误的依赖注入。 |
| **测试友好** | 可以为每个 algebra 生成 mock 实现或解释器，配合 Cats Effect 的 `IO`、`Resource` 等进行纯函数式测试。 |

---

## 典型接入方式（Typical Integration）

1. **在 `build.sbt` 中加入依赖**  

   ```scala
   libraryDependencies += "org.typelevel" %% "cats-tagless-core" % "0.16.0"
   // 如需 macro 自动派生
   libraryDependencies += "org.typelevel" %% "cats-tagless-macros" % "0.16.0"
   ```

2. **定义 Tagless Final Algebra**  

   ```scala
   import cats.effect.Sync
   import cats.tagless.FunctorK

   @autoFunctorK // macro 自动生成 FunctorK 实例
   trait Logging[F[_]] {
     def info(msg: String): F[Unit]
     def error(msg: String, t: Throwable): F[Unit]
   }
   ```

3. **实现具体解释器**（例如基于 `cats.effect.IO`）  

   ```scala
   import cats.effect.IO

   class ConsoleLogging extends Logging[IO] {
     def info(msg: String): IO[Unit]  = IO.println(s"[INFO] $msg")
     def error(msg: String, t: Throwable): IO[Unit] = IO.println(s"[ERROR] $msg: ${t.getMessage}")
   }
   ```

4. **在业务代码中使用抽象**  

   ```scala
   class Service[F[_]: Sync](log: Logging[F]) {
     def run: F[Unit] = log.info("service started")
   }

   // 组合多个 algebras
   type App[F[_]] = Logging[F] with OtherAlgebra[F]
   ```

5. **利用 `InjectK` / `FunctorK` 进行依赖注入或解释器转换**  

   ```scala
   // 将 Logging[IO] 注入到更大的解释器堆栈
   val app: App[IO] = new Service[IO](new ConsoleLogging) with OtherAlgebraImpl[IO]
   ```

6. **在测试环境中提供 Mock 实现**  

   ```scala
   class MockLogging[F[_]: Applicative] extends Logging[F] {
     def info(msg: String): F[Unit] = Applicative[F].unit
     def error(msg: String, t: Throwable): F[Unit] = Applicative[F].unit
   }
   ```

---

## 生产可用性（Production Readiness）

| 维度 | 评估 |
|------|------|
| **社区活跃度** | 319 ★、41 Fork，最近一次提交在 **2026‑07‑12**，说明仍在维护。 |
| **依赖成熟度** | 依赖 Cats、Cats Effect 等成熟库，且已在多个开源项目中使用。 |
| **稳定性** | 代码库已发布多个 0.x 版本，语义版本遵循 SemVer，向后兼容性较好。 |
| **风险** | - 文档主要集中在 README，缺少完整的使用手册；<br>- 需要自行决定宏自动派生或手写实例，集成成本取决于团队对宏的熟悉度。 |
| **适用场景** | - 原型或内部服务快速搭建；<br>- 需要高度可组合、可测试的业务抽象；<br>- 与 Cats Effect、http4s、fs2 等生态共用时尤为便利。 |
| **生产建议** | 1. 在 CI 中加入 `scalafmt` / `scalacOptions` 检查，确保宏生成代码无意外。<br>2. 通过 `InjectK`/`FunctorK` 进行模块化测试，验证解释器在真实运行时的行为。<br>3. 定期跟踪 `cats-tagless` 的发布日志，评估潜在的破坏性变更。 |

**结论**：`cats-tagless` 已达到 **中等** 的生产可用性，适合在内部或对可靠性要求不极端的生产系统中使用。只要在引入前做好依赖审计、宏兼容性检查以及基本的集成测试，即可安全投入使用。

## 🧭 Practical evaluation

**Value:** typelevel/cats-tagless may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 319 GitHub stars
- 41 forks
- updated 2026-07-12
- primary language: Scala
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 53/100 |
| topics | 38/100 |
| outlook | 70/100 |
| quality | 68/100 |
| recency | 100/100 |
| adoption | 50/100 |
| production | 70/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/typelevel/cats-tagless) · [← Back to Misc](./README.md)</sub>
