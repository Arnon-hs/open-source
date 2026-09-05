# facebookincubator/Glean

[![Stars](https://img.shields.io/github/stars/facebookincubator/Glean?style=flat-square&color=yellow)](https://github.com/facebookincubator/Glean/stargazers) [![Forks](https://img.shields.io/github/forks/facebookincubator/Glean?style=flat-square&color=blue)](https://github.com/facebookincubator/Glean/network) [![Language](https://img.shields.io/badge/lang-Hack-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> System for collecting, deriving and working with facts about source code.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.4k |
| 🍴 **Forks** | 88 |
| 💻 **Language** | Hack |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
Glean is Facebook’s open‑source system for collecting, deriving, and querying factual data about source code. It stores code‑level “facts” (e.g., definitions, call sites, type information) in a searchable index, enabling sophisticated static‑analysis and code‑navigation workflows.  

**Value**  
- **Rich code intelligence**: By materialising structural facts about a codebase, Glean makes it possible to write high‑level queries that answer questions such as “which services call this API?” or “what are all the overloads of a given function?” without writing custom parsers.  
- **Extensible derivations**: New fact types can be derived from existing ones, allowing teams to incrementally enrich the knowledge graph as their analysis needs evolve.  
- **Language‑agnostic core**: Although the reference implementation is in Hack, the fact model and query language are language‑neutral, so it can be adapted to other ecosystems.

**Practical Adoption Path**  
1. **Pilot the data pipeline** – Clone the repo, run the provided Docker compose setup, and ingest a small, self‑contained repository to verify that the fact extraction works for your language stack.  
2. **Define needed fact schemas** – Extend the existing schema (or reuse the default) to capture the specific code attributes your team cares about (e.g., build targets, security annotations).  
3. **Integrate with CI/CD** – Hook the extractor into your build pipeline so that facts are regenerated on each commit; store the generated `.glean` files in an artifact store or a dedicated Glean server.  
4. **Query and iterate** – Use the Glean query language (similar to GraphQL) from scripts, notebooks, or IDE plugins to surface insights; refine schemas and derivations based on feedback.  
5. **Scale & harden** – Deploy a production Glean server (or use the hosted version if available), set up authentication, monitoring, and backup of the fact store.

**Production Readiness**  
- **Maturity**: Medium. The project has a solid community footprint (≈1.3 k stars, recent updates) and is used internally at Facebook, but documentation and integration guides are sparse.  
- **Suitability**: Ideal for prototypes, internal tooling, or teams that need deep static analysis without building a custom parser. For production use, you should perform a thorough dependency audit (Hack runtime, required services) and establish a maintenance plan for schema evolution.  
- **Risks**: The integration path is not clearly documented; expect a non‑trivial setup effort and possible custom glue code. Validate the operational cost (storage for fact indices, query latency) before committing to a long‑term deployment.

### Русский

Glean — это открытая система от Facebook Incubator для сбора, обработки и анализа фактов о исходном коде, позволяющая автоматически извлекать метаданные (зависимости, вызовы, типы и т. д.) и использовать их в инструментах статического анализа, ревью и проектной навигации. Типичный сценарий — интеграция в CI/CD или внутренний аналитический пайплайн, где после предварительной проверки совместимости и настройки Glean служит источником актуального кода‑фактов для прототипов и внутренних сервисов. Готовность к production — средняя: проект стабилен и активно поддерживается (1355 звёзд, недавнее обновление), но путь интеграции требует ручного анализа и проверки зависимостей перед развертыванием в продакшн.

### 中文

**项目简介**  
facebookincubator/Glean 是一个用于收集、推导和查询源码事实的系统，帮助开发者以结构化方式存储代码元数据，从而实现高效的代码搜索、依赖分析和自动化审计。

**价值**  
- **统一事实库**：把编译信息、依赖关系、注解、测试覆盖等多维度数据统一写入可查询的事实库，消除散落在不同工具链中的信息孤岛。  
- **强大查询能力**：基于自研的查询语言（类似 SQL）可以快速检索跨语言、跨仓库的代码事实，支持复杂的依赖图、变更影响分析等场景。  
- **提升生产力**：在代码审查、迁移、自动生成文档或安全审计时，直接使用已有事实即可避免重复解析和手工统计。

**典型接入方式**  
1. **构建阶段集成**：在 CI/CD 流水线中加入 Glean 的编译插件（Hack/Cpp/Java 等），让编译器在生成对象文件时同步生成事实（FactDB）。  
2. **事实导入**：使用 `glean import` 将已有的 build metadata（Bazel、Buck、CMake 等）或第三方工具输出（Clang AST、LSP）导入 Glean。  
3. **查询服务部署**：启动 Glean server（基于 SQLite/rocksdb）并通过 HTTP/gRPC 暴露查询接口，供内部工具或 IDE 插件调用。  
4. **权限与治理**：结合组织的 SSO/LDAP 为不同团队配置查询权限，确保敏感代码事实受控访问。

**生产可用性**  
- **成熟度**：项目已有 1355+ stars、88 forks，最近一次提交在 2026‑06‑26，活跃度尚可。  
- **适用范围**：适合内部原型、代码分析平台或作为大型 monorepo 的事实层；在生产环境使用前建议完成以下检查：  
  - **依赖审计**：确认所使用的 Hack 运行时、数据库后端以及 CI 插件与现有技术栈兼容。  
  - **运维准备**：评估事实库的规模（TB 级别时需考虑分片或外部存储），并制定备份/恢复策略。  
  - **安全评审**：审查查询接口的访问控制，防止代码事实泄露。  
- **风险**：元数据中缺乏明确的接入指南，集成路径需要手动探索和实验。若团队能够投入一定的前期调研和脚本开发，Glean 在内部工作流中可达到 **中等** 的生产就绪度；在对可靠性要求极高的对外服务中仍需更充分的测试与运维支撑。

## 🧭 Practical evaluation

**Value:** facebookincubator/Glean may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1355 GitHub stars
- 88 forks
- updated 2026-06-26
- primary language: Hack

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 49/100 |
| stars | 67/100 |
| topics | 0/100 |
| outlook | 62/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 62/100 |
| production | 63/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/facebookincubator/Glean) · [← Back to Misc](./README.md)</sub>
