# seancorfield/honeysql

[![Stars](https://img.shields.io/github/stars/seancorfield/honeysql?style=flat-square&color=yellow)](https://github.com/seancorfield/honeysql/stargazers) [![Forks](https://img.shields.io/github/forks/seancorfield/honeysql?style=flat-square&color=blue)](https://github.com/seancorfield/honeysql/network) [![Language](https://img.shields.io/badge/lang-Clojure-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> Turn Clojure data structures into SQL

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.9k |
| 🍴 **Forks** | 173 |
| 💻 **Language** | Clojure |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Honeysql (seancorfield/honeysql) is a Clojure library that lets you build SQL statements using native Clojure data structures, turning maps, vectors and keywords into safe, composable queries. With over 1.9 k stars and active maintenance, it’s a popular choice for teams that want to keep query logic in code rather than raw strings.  

**Value**  
- **Declarative query construction** – By expressing SQL as Clojure literals you get compile‑time syntax checking, easier refactoring, and seamless integration with existing Clojure data pipelines.  
- **Safety & composability** – Parameters are automatically bound, reducing injection risk, and queries can be incrementally built and combined, which is ideal for dynamic analytics or reporting workloads.  
- **Ecosystem fit** – Works naturally with libraries such as `clojure.java.jdbc`, `next.jdbc`, and data‑processing frameworks, allowing you to generate queries directly from transformation steps.  

**Practical Adoption Path**  

| Step | Action | Why it matters |
|------|--------|----------------|
| 1️⃣  | **Prototype** – Add the library to a sandbox project, write a few simple `select`, `insert`, and `update` statements using the DSL. | Confirms that the DSL matches your team’s coding style and that it integrates with your JDBC driver. |
| 2️⃣  | **Validate against existing queries** – Translate a representative set of production SQL strings into Honeysql forms and compare results. | Ensures functional parity and surfaces any edge‑case syntax (e.g., vendor‑specific extensions) that may need custom handling. |
| 3️⃣  | **Integrate with your data layer** – Wrap the generated query maps in your current `next.jdbc` or `clojure.java.jdbc` calls. | Minimal code churn; you keep the same connection handling while swapping string SQL for Honeysql maps. |
| 4️⃣  | **Add tests** – Use property‑based or snapshot tests to guarantee that the generated SQL remains stable after refactors. | Provides the safety net needed before moving to production. |
| 5️⃣  | **Gradual rollout** – Deploy the new query builder in a low‑risk service or internal analytics pipeline, monitor performance and correctness. | Limits impact if unexpected behavior appears. |

**Production Readiness**  
- **Maturity**: Medium. The library is mature (1901 stars, 173 forks) and receives regular updates (last commit 2026‑06‑27), but its integration signals are sparse, so you’ll need to verify compatibility with your specific database dialect and tooling.  
- **Risk Mitigation**: Conduct a small‑scale pilot, add comprehensive unit/integration tests, and review the generated SQL for any vendor‑specific quirks. Dependency health is good, but keep an eye on the library’s release cadence and any breaking changes.  
- **Suitability**: Ideal for prototypes, internal analytics pipelines, and services where query logic is heavily code‑driven. With proper validation and testing, it can be promoted to production for stable, internal workloads.  

In short, Honeysql offers a powerful, idiomatic way to generate SQL from Clojure data, but you should validate the integration path and add test coverage before treating it as a production‑critical component.

### Русский

**seancorfield/honeysql** – это библиотека на Clojure, позволяющая писать запросы к базе данных в виде обычных Clojure‑структур, которые автоматически преобразуются в корректный SQL. Она удобна для построения аналитических пайплайнов, обработки наборов данных и улучшения отчётных процессов, однако из‑за скудной документации по интеграции её стоит протестировать в изолированном окружении перед масштабным внедрением. По уровню готовности проект находится в среднем диапазоне: подходит для прототипов и внутренних сервисов, но требует проверки зависимостей и поддержки перед использованием в продакшене.

### 中文

**项目简介**  
`seancorfield/honeysql` 是一个 Clojure 库，能够把 Clojure 的数据结构（向量、映射等）直接转换为标准 SQL 语句，从而让开发者在代码中以函数式、可组合的方式构造查询。

**价值**  
- **提升开发效率**：使用原生 Clojure 数据结构编写查询，避免手写字符串拼接，降低语法错误风险。  
- **易于维护和重构**：查询逻辑以数据形式存在，版本控制、审计和单元测试都更直接。  
- **灵活的 DSL**：支持 SELECT、INSERT、UPDATE、DELETE 以及复杂的 JOIN、WHERE、GROUP BY 等子句，满足大多数分析和报表需求。

**典型接入方式**  
1. **在项目中加入依赖**（Leiningen / deps.edn）  
   ```clojure
   ;; Leiningen
   [honeysql "2.5.0"]
   ;; deps.edn
   {:deps {honeysql/honeysql {:mvn/version "2.5.0"}}}
   ```  
2. **构造查询数据结构**  
   ```clojure
   (require '[honeysql.core :as sql])
   (def q (-> (sql/select :id :name)
              (sql/from :users)
              (sql/where [:> :age 18])
              (sql/order-by :created_at)))
   ```  
3. **生成 SQL 字符串并执行**（配合 JDBC、next.jdbc、hugsql 等）  
   ```clojure
   (let [{:keys [query params]} (sql/format q)]
     (jdbc/execute! ds [query params]))
   ```  
4. **在测试或原型阶段直接打印 SQL**，快速验证生成结果。  

**生产可用性**  
- **成熟度**：GitHub ★1900+，活跃维护（截至 2026‑06‑27），社区已有不少实战案例。  
- **适用场景**：非常适合内部原型、数据分析管道以及需要频繁构造动态查询的微服务。  
- **风险与注意点**  
  - **集成成本**：库本身只负责生成 SQL，实际执行仍需自行选择 JDBC/next.jdbc 等适配层，且缺少完整的迁移或 ORM 功能。  
  - **审计与安全**：虽然使用数据结构可避免拼接注入，但仍需在 `format` 后检查生成的 SQL，尤其在接受外部参数时。  
- **推荐做法**：在进入生产前进行一次依赖审计（库的版本兼容性、许可证），并在 CI 中加入对关键查询的单元测试，以确保生成的 SQL 与预期一致。  

综上，`honeysql` 在 Clojure 生态中提供了轻量且可组合的 SQL 生成能力，适合作为原型到内部生产系统的桥梁，只要做好集成测试和安全审查，即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** seancorfield/honeysql helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1901 GitHub stars
- 173 forks
- updated 2026-06-27
- primary language: Clojure

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 70/100 |
| topics | 0/100 |
| outlook | 63/100 |
| quality | 65/100 |
| recency | 80/100 |
| adoption | 66/100 |
| production | 64/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/seancorfield/honeysql) · [← Back to Misc](./README.md)</sub>
