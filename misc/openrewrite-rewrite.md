# openrewrite/rewrite

[![Stars](https://img.shields.io/github/stars/openrewrite/rewrite?style=flat-square&color=yellow)](https://github.com/openrewrite/rewrite/stargazers) [![Forks](https://img.shields.io/github/forks/openrewrite/rewrite?style=flat-square&color=blue)](https://github.com/openrewrite/rewrite/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> Automated mass refactoring of source code.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.5k |
| 🍴 **Forks** | 521 |
| 💻 **Language** | Java |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`abstract-syntax-tree` `ast` `code-search` `java` `refactoring` `refactoring-tools`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
OpenRewrite Rewrite is an open‑source Java library that automates large‑scale, systematic refactoring of source code. With a strong community (3,400+ stars, 500+ forks) and recent activity, it can be used to apply consistent code‑style, API‑migration, or security‑fix transformations across many repositories.

**Value**  
Rewrite lets teams codify refactoring rules as reusable recipes, enabling one‑click, repeatable changes that would otherwise require manual, error‑prone edits. This accelerates migration to new libraries, enforces coding standards, and reduces technical debt at scale.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone a small, representative module and run the supplied sample recipes to verify that the tool can parse and transform your codebase.  
2. **Customize recipes** – Write or extend existing recipes to match your specific migration or linting goals, using the extensive documentation and examples in the README.  
3. **Integrate into CI** – Add a Gradle/Maven plugin step that runs Rewrite in a non‑blocking mode (e.g., `--dryRun`) to generate pull requests or diff reports.  
4. **Iterate and expand** – Gradually roll the validated recipes out to additional modules or services, monitoring build health and developer feedback.

**Production Readiness**  
The project shows high production readiness: it is actively maintained (last update 2026‑05‑12), has a sizable user base, and is already adopted by several large enterprises for automated migrations. While the integration path isn’t fully documented in the metadata, the available plugins, clear API, and community support make it a solid candidate for a serious pilot, provided the initial setup cost is validated through the small PoC.

### Русский

OpenRewrite — это библиотека для автоматизированного массового рефакторинга Java‑кода, позволяющая задавать правила трансформации и применять их к большому количеству репозиториев без ручного вмешательства. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept на одном‑двух проектах, проверка README и примеров правил, а затем масштабирование на CI/CD для постоянного поддержания качества кода. По оценке готовности проекта к продакшн: активная поддержка, более 3400 звёзд, регулярные коммиты и уже используемые в крупных компаниях, что делает его надёжным кандидатом для пилотного использования.

### 中文

**项目简介**  
OpenRewrite（`openrewrite/rewrite`）是一套基于 Java 的自动化大规模代码重构框架，能够在不改变业务行为的前提下统一执行风格迁移、API 替换、安全加固等批量改动。

**价值**  
- **统一性**：一次定义的重构 recipe 可在整个代码库甚至多个仓库中重复执行，保证改动一致且可追溯。  
- **安全性**：所有改动通过编译期 AST 分析完成，避免正则匹配带来的误改风险。  
- **可扩展**：支持自定义 Java、Kotlin、XML、YAML 等多语言 recipe，且社区已有丰富的开箱即用的迁移规则。  

**典型接入方式**  
1. **阅读 README 与示例**，确认已有的 recipe 是否满足需求。  
2. **在本地或 CI 环境**通过 Maven/Gradle 插件引入 `org.openrewrite:rewrite-maven-plugin`（或对应的 Gradle 插件）。  
3. 编写或引用所需的 **recipe.yaml**，在 `pom.xml`/`build.gradle` 中配置插件执行目标（如 `rewriteRun`）。  
4. 先在小范围（单个模块或分支）运行 `rewriteDryRun` 进行预览，确认改动后再在全库或 CI 中正式执行。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑12，拥有 3.4k+ Stars、500+ Fork，社区活跃。  
- **成熟度**：已在多个大型企业（如 Netflix、Google）内部使用，具备完整的测试套件和稳定的发布周期。  
- **风险**：集成路径需要根据项目的构建工具（Maven/Gradle）和语言范围自行配置，建议先做小规模 POC 验证配置成本。  

总体而言，OpenRewrite 在代码质量治理、技术债务清除和安全加固方面具备高可用性，适合作为企业级代码迁移与自动化重构的核心工具。

## 🧭 Practical evaluation

**Value:** openrewrite/rewrite may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3469 GitHub stars
- 521 forks
- updated 2026-05-12
- primary language: Java
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 75/100 |
| topics | 75/100 |
| outlook | 75/100 |
| quality | 79/100 |
| recency | 80/100 |
| adoption | 73/100 |
| production | 69/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/openrewrite/rewrite) · [← Back to Misc](./README.md)</sub>
