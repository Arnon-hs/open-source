# FasterXML/jackson-module-scala

[![Stars](https://img.shields.io/github/stars/FasterXML/jackson-module-scala?style=flat-square&color=yellow)](https://github.com/FasterXML/jackson-module-scala/stargazers) [![Forks](https://img.shields.io/github/forks/FasterXML/jackson-module-scala?style=flat-square&color=blue)](https://github.com/FasterXML/jackson-module-scala/network) [![Language](https://img.shields.io/badge/lang-Scala-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> Add-on module for Jackson (https://github.com/FasterXML/jackson) to support Scala-specific datatypes

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 508 |
| 🍴 **Forks** | 139 |
| 💻 **Language** | Scala |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cbor` `hacktoberfest` `jackson` `json` `scala` `serialization` `smile` `xml`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Project Summary:**
FasterXML/jackson-module-scala is an open-source project that extends the popular Jackson library to support Scala-specific data types, enabling the development of AI capabilities without starting from scratch. This module facilitates the integration of AI features into existing projects, making it an ideal choice for prototyping and internal workflows. However, careful evaluation and validation of the setup cost are necessary before committing to production use.

**Value:**
The value proposition of FasterXML/jackson-module-scala lies in its ability to simplify the integration of AI capabilities into existing projects, allowing developers to focus on building and evaluating AI features without the need to establish a comprehensive model stack from scratch. This makes it an attractive choice for prototyping AI features, building RAG (Reusable Agent Graph) or agent workflows, and evaluating model tooling.

**Practical Adoption Path:**
To adopt FasterXML/jackson-module-scala, developers should start with a small proof of concept to evaluate the integration path and feasibility of the module. A thorough review of the README documentation is also recommended to ensure a smooth setup process. Once the proof of concept is successful, developers can proceed with integrating the module into their project, monitoring its performance, and validating the setup cost before committing to production use.

**Production Readiness:**

### Русский

FasterXML/jackson-module‑scala — это расширяющий модуль для популярного JSON‑парсера Jackson, который добавляет поддержку типовых Scala‑коллекций и классов, упрощая сериализацию/десериализацию данных в проектах на Scala. Его обычно используют в прототипах AI‑фич, RAG‑системах или агентных воркфлоу, где необходимо быстро интегрировать JSON‑взаимодействие без написания собственного маппинга. Готовность к production — средняя: модуль стабилен и активно поддерживается (508 звёзд, недавние коммиты), но перед выпуском в продакшн следует проверить совместимость зависимостей и провести небольшое proof‑of‑concept, чтобы уточнить детали интеграции.

### 中文

**项目简介**  
FasterXML/jackson-module-scala 是 Jackson（https://github.com/FasterXML/jackson）的 Scala 扩展模块，提供对 Scala 专有数据类型（如 `Option`, `Either`, `Tuple`, `CaseClass` 等）的序列化与反序列化支持，使得在 Scala 项目中使用 Jackson 进行 JSON 处理变得无缝且类型安全。

---

### 价值点
1. **桥接 Jackson 与 Scala**：利用成熟的 Jackson 核心库，同时保留 Scala 的函数式特性，避免自行实现繁琐的序列化逻辑。  
2. **加速 AI/ML 原型**：在构建 RAG、Agent 或其他 AI 工作流时，常需把模型输入/输出转为 JSON；该模块让 Scala 开发者快速完成数据搬运，省去手写转换代码的时间。  
3. **生态兼容**：与 Jackson 生态（如 `jackson-databind`, `jackson-module-parameter-names`）保持一致，可直接与 Spring Boot、Akka HTTP、Play Framework 等框架配合使用。

---

### 典型接入方式
1. **添加依赖**（sbt 示例）  
   ```scala
   libraryDependencies ++= Seq(
     "com.fasterxml.jackson.core" % "jackson-databind" % "2.17.0",
     "com.fasterxml.jackson.module" %% "jackson-module-scala" % "2.17.0"
   )
   ```
2. **注册模块**  
   ```scala
   import com.fasterxml.jackson.databind.ObjectMapper
   import com.fasterxml.jackson.module.scala.DefaultScalaModule

   val mapper = new ObjectMapper()
   mapper.registerModule(DefaultScalaModule)   // 启用 Scala 支持
   ```
3. **使用示例**  
   ```scala
   case class Person(name: String, age: Int, nickname: Option[String])

   val json = mapper.writeValueAsString(Person("Alice", 30, Some("Al")))
   val obj  = mapper.readValue[Person](json, classOf[Person])
   ```
   以上代码即可正确处理 `Option`、`case class` 等 Scala 类型。

4. **在框架中集成**  
   - **Spring Boot**：在 `Jackson2ObjectMapperBuilder` 中添加 `DefaultScalaModule`。  
   - **Akka HTTP**：在 `SprayJsonSupport` 或自定义 `JacksonSupport` 中注册模块。  
   - **Play Framework**：通过 `play-json` 的 `JacksonJson` 适配器使用同一 `ObjectMapper`。

---

### 生产可用性评估
| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | ★★★★☆ (4/5) | 2026-07-05 最近一次更新，508 星，139 Fork，社区活跃。 |
| **稳定性** | ★★★★☆ | 依赖 Jackson 主库的长期维护，向后兼容性良好。 |
| **安全性** | ★★★★☆ | 通过 Maven Central 分发，受制于 Jackson 的安全审计；仍需关注 CVE。 |
| **运维成本** | ★★★☆☆ | 需要在 CI 中验证 Scala 与 Jackson 版本匹配，避免二进制冲突。 |
| **适用场景** | ★★★★☆ | 原型、内部服务、数据管道；在对延迟和资源占用要求不极端的生产环境亦可使用。 |
| **风险** | ★★☆☆☆ | 集成文档相对分散，首次接入需阅读 README 与示例代码，确认与现有依赖的兼容性。 |

**结论**：该模块在功能完整性和社区支持上已足够成熟，适合作为 Scala 项目中 JSON 处理的标准方案。建议先在小范围 PoC 中验证 `ObjectMapper` 配置与现有依赖的兼容性，确认无冲突后即可推广至生产环境，并在 CI 中加入对应的序列化单元测试以防止升级风险。

## 🧭 Practical evaluation

**Value:** FasterXML/jackson-module-scala helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 508 GitHub stars
- 139 forks
- updated 2026-07-05
- primary language: Scala
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 58/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 56/100 |
| production | 55/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/FasterXML/jackson-module-scala) · [← Back to Misc](./README.md)</sub>
