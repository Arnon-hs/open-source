# Kotlin/kotlinx.collections.immutable

[![Stars](https://img.shields.io/github/stars/Kotlin/kotlinx.collections.immutable?style=flat-square&color=yellow)](https://github.com/Kotlin/kotlinx.collections.immutable/stargazers) [![Forks](https://img.shields.io/github/forks/Kotlin/kotlinx.collections.immutable?style=flat-square&color=blue)](https://github.com/Kotlin/kotlinx.collections.immutable/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Immutable persistent collections for Kotlin

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.4k |
| 🍴 **Forks** | 68 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`collections` `immutable` `immutable-collections` `kotlin`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
Kotlin/kotlinx.collections.immutable provides a set of persistent, immutable collection types (lists, sets, maps, etc.) that can be used in Kotlin projects to guarantee functional‑style safety without copying data on every mutation. With over 1.4 k stars and recent updates, it is a mature library that can replace mutable collections when you need thread‑safe, versioned data structures.

**Value**  
The library lets you work with collections that never change after creation, enabling safe sharing across threads and simplifying reasoning about state in reactive or concurrency‑heavy codebases. Because the collections are persistent, each “modification” returns a new structure that shares most of its internal representation with the previous one, giving you immutability with minimal memory and performance overhead.

**Practical adoption path**  
1. **Read the README** and run the small “Hello‑Immutable‑Collection” example to verify the API matches your coding style.  
2. Add the dependency (`implementation("org.jetbrains.kotlinx:kotlinx-collections-immutable:<version>")`) to a sandbox module or a prototype service.  
3. Replace a few critical mutable collections (e.g., a shared `MutableList` used in coroutines) with their immutable counterparts and run existing unit tests to confirm behavior.  
4. Gradually expand the usage to larger parts of the codebase once the proof‑of‑concept proves stable.

**Production readiness**  
The project is at a medium readiness level: it is actively maintained (last commit 2026‑05‑12), has a healthy community signal, and is suitable for prototypes or internal services. Before moving to production, perform a dependency audit (check for transitive conflicts), verify that the library’s versioning policy aligns with your release cadence, and run performance benchmarks for your specific workloads. With those checks in place, the library can be safely promoted to production environments.

### Русский

**Kotlin/kotlinx.collections.immutable** — это библиотека с неизменяемыми (persistent) коллекциями, написанными на Kotlin, позволяющая безопасно работать с данными в многопоточных и реактивных приложениях без копирования структуры. Типичный сценарий внедрения — добавить зависимость, проверить README и реализовать небольшой proof‑of‑concept (например, заменив `MutableList` на `PersistentList`) для оценки совместимости с текущим кодом. Готовность к production — средняя: библиотека стабильно поддерживается (1403 ★, обновление 2026‑05‑12), но перед выпуском в прод необходимо проверить процесс сборки, совместимость с используемыми версиями Kotlin и потенциальные накладные расходы на миграцию.

### 中文

**项目简介**  
Kotlin/kotlinx.collections.immutable 为 Kotlin 提供了一套不可变（immutable）且持久化（persistent）的集合实现，包括 `PersistentList`、`PersistentSet`、`PersistentMap` 等。通过结构共享的方式，它在对集合进行增删改操作时只会复制必要的节点，既保持了函数式编程的安全性，又拥有接近可变集合的性能。

**价值**  
- **安全性**：不可变集合天然防止并发修改导致的竞态条件，适合多线程或协程环境。  
- **可预测的副作用**：所有修改都会返回新实例，原始集合保持不变，便于调试和单元测试。  
- **性能**：采用持久化数据结构，增删改的时间复杂度通常为 O(log n) 或 O(1)，而且共享内部节点降低了内存开销。  
- **与 Kotlin 标准库兼容**：提供的 API 与 `kotlin.collections` 接口保持一致，迁移成本低。

**典型接入方式**  
1. **Gradle / Maven 引入**  
   ```kotlin
   // Gradle Kotlin DSL
   implementation("org.jetbrains.kotlinx:kotlinx-collections-immutable:0.3.7")
   ```
2. **创建持久化集合**  
   ```kotlin
   val list = persistentListOf(1, 2, 3)
   val newList = list.add(4)          // 返回新列表，原 list 不变
   val set = persistentSetOf("a", "b")
   val newSet = set.remove("a")
   ```
3. **在业务代码中替换可变集合**  
   将 `MutableList`、`MutableMap` 等改为对应的持久化实现，或在需要快照的场景（如 UI 状态、事件流）直接使用 `persistent*Of` 创建只读视图。  
4. **与协程/Flow 结合**  
   持久化集合可以安全地在多个协程之间共享，配合 `StateFlow`、`MutableStateFlow` 使用时，只需在每次更新时 `stateFlow.value = newCollection`。

**生产可用性**  
- **成熟度**：项目已有 1400+ 星、持续更新（截至 2026‑05‑12），社区活跃，文档齐全。  
- **适用范围**：非常适合内部工具、原型以及对并发安全有要求的微服务/Android 应用。  
- **风险与注意事项**  
  - 依赖体积相对较小，但仍需在 CI 中确认兼容的 Kotlin 版本（当前 1.9+）。  
  - 持久化集合的性能特性在极大规模（数十万以上）时需要评估，必要时做基准测试。  
  - 与已有的可变集合混用时要注意 API 差异，避免意外的类型转换。  

综合来看，kotlinx.collections.immutable 已具备在生产环境中使用的基本条件，只要在引入前完成一次小规模的 PoC（验证 API、性能和构建兼容性），即可安全投入项目。

## 🧭 Practical evaluation

**Value:** Kotlin/kotlinx.collections.immutable may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1403 GitHub stars
- 68 forks
- updated 2026-05-12
- primary language: Kotlin
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 67/100 |
| topics | 50/100 |
| outlook | 67/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 61/100 |
| production | 66/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/Kotlin/kotlinx.collections.immutable) · [← Back to Misc](./README.md)</sub>
