# automvc/bee

[![Stars](https://img.shields.io/github/stars/automvc/bee?style=flat-square&color=yellow)](https://github.com/automvc/bee/stargazers) [![Forks](https://img.shields.io/github/forks/automvc/bee?style=flat-square&color=blue)](https://github.com/automvc/bee/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Bee is an AI, easy and high efficiency ORM framework,support JDBC,Cassandra,Mongodb,Sharding,Android,HarmonyOS.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 633 |
| 🍴 **Forks** | 59 |
| 💻 **Language** | Java |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android-orm` `dao` `mongodb-orm` `orm` `sharding-jdbc`

## 🎯 Categories

Database · Mobile

## 📝 Summary

### English

**Project Summary:**
Bee is an open-source, high-efficiency ORM (Object-Relational Mapping) framework that integrates AI capabilities, supporting various databases, including JDBC, Cassandra, MongoDB, and sharding. It is designed to simplify the addition of AI features to existing projects. Bee is suitable for prototyping AI features and building internal workflows.

**Value Proposition:**
The primary value proposition of Bee is its ability to add AI capabilities without requiring a new, blank model stack. This allows developers to quickly prototype and evaluate AI features, build internal workflows, and assess model tooling. Bee's versatility, supporting multiple databases and platforms (including Android and HarmonyOS), further enhances its value.

**Practical Adoption Path:**
To adopt Bee, developers should:
1. Review the project's README and documentation to understand its capabilities and limitations.
2. Start with a small proof of concept to evaluate Bee's feasibility and performance.
3. Assess the project's dependency and maintenance requirements to ensure they align with production needs.
4. Verify the project's license, security posture, and active maintainers to ensure a stable and secure foundation.

**Production Readiness:**
Bee is rated as "Medium" in terms of production readiness. While it is suitable for prototypes and internal workflows, its adoption

### Русский

**Bee** — это открытый Java‑ORM с встроенными AI‑возможностями, поддерживающий JDBC, Cassandra, MongoDB, шардирование и мобильные платформы (Android, HarmonyOS). Он позволяет быстро добавить AI‑функционал (прототипы RAG‑систем, агентные воркфлоу, оценка моделей) без необходимости строить стек с нуля; рекомендуется начать с небольшого proof‑of‑concept и проверки README. Готовность к продакшн — средняя: подходит для прототипов и внутренних сервисов, но требует проверки зависимостей, лицензии и активного сопровождения перед масштабным внедрением.

### 中文

**项目价值**  
automvc/bee 为 Java 开发者提供了一个“一站式”AI‑ORM 框架，能够在同一层级同时管理关系型数据库（JDBC）、NoSQL（Cassandra、MongoDB）以及分片、移动端（Android、HarmonyOS）等多种数据源，并内置 AI 能力。这样，团队在实现 RAG（检索增强生成）或智能代理工作流时，无需从零搭建模型堆栈，只需在已有的数据访问层上直接调用 AI 接口，显著缩短原型开发周期并提升迭代效率。

**典型接入方式**  
1. **依赖引入**：在 Maven/Gradle 项目中加入 `automvc:bee` 的坐标。  
2. **配置数据源**：在 `application.yml`（或 `properties`）中声明 JDBC、Cassandra、MongoDB 等连接信息，或在 Android/HarmonyOS 项目中使用对应的 SDK 初始化。  
3. **模型/实体声明**：使用 Bee 提供的注解（如 `@Entity`, `@ShardKey`）定义业务实体，框架自动生成对应的 DAO。  
4. **AI 调用**：通过 `BeeAI`（或类似的入口类）加载预训练模型或外部模型服务，直接在 DAO 方法中加入 `@AIPredict`、`@RAG` 等注解，实现“查询‑生成”一体化。  
5. **小范围验证**：先在本地或测试环境跑一个 PoC（如实现一个简单的智能搜索或推荐），确认模型调用、分片路由和移动端兼容性均正常后，再逐步推广到全链路。

**生产可用性**  
- **成熟度**：GitHub 现有 633 ★、59 Fork，最近一次提交在 2026‑06‑28，代码活跃度尚可，适合作为内部原型或业务实验平台。  
- **准备度**：属于 **中等**（Medium）级别。对生产环境使用前，需要完成以下检查：  
  1. **许可证合规**（确认使用的 Apache/MIT 等开源许可证是否满足公司政策）。  
  2. **安全审计**：审查依赖的第三方库（JDBC 驱动、MongoDB 客户端等）是否存在已知漏洞。  
  3. **运维准备**：评估分片、连接池、异常回滚等特性在高并发下的表现，并制定监控/日志方案。  
  4. **模型治理**：若使用自托管模型，需确保模型版本管理、推理资源（GPU/CPU）和数据隐私合规。  

总体而言，automvc/bee 适合作为 **AI‑增强原型** 或 **内部工作流** 的快速搭建工具；在完成安全、合规和运维验证后，亦可逐步推广至生产环境，尤其是对多数据源统一访问并需要 AI 辅助决策的业务场景。

## 🧭 Practical evaluation

**Value:** automvc/bee helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 633 GitHub stars
- 59 forks
- updated 2026-06-28
- primary language: Java
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 60/100 |
| topics | 63/100 |
| outlook | 56/100 |
| quality | 59/100 |
| recency | 40/100 |
| adoption | 55/100 |
| production | 55/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/automvc/bee) · [← Back to Database](./README.md)</sub>
