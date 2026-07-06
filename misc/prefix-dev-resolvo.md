# prefix-dev/resolvo

[![Stars](https://img.shields.io/github/stars/prefix-dev/resolvo?style=flat-square&color=yellow)](https://github.com/prefix-dev/resolvo/stargazers) [![Forks](https://img.shields.io/github/forks/prefix-dev/resolvo?style=flat-square&color=blue)](https://github.com/prefix-dev/resolvo/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> Fast package resolver written in Rust (CDCL based SAT solving)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 220 |
| 🍴 **Forks** | 29 |
| 💻 **Language** | Rust |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-07-06 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
`prefix-dev/resolvo` is a fast, CDCL‑based SAT‑solver written in Rust that resolves package dependency graphs. With ~220 stars and recent activity (last commit 2026‑07‑06), it can be a solid building block for custom package‑management or build‑tool workflows, provided the integration effort is evaluated first.

**Value**  
- **Speed & determinism** – By leveraging a conflict‑driven clause learning (CDCL) SAT engine, Resolvo can explore large dependency graphs orders of magnitude faster than naïve backtracking resolvers.  
- **Rust ecosystem** – The library is pure Rust, offering zero‑cost abstractions, strong type safety, and easy inclusion in any Rust‑based tooling or as a FFI component for other languages.  
- **Open‑source flexibility** – The codebase is small enough to audit, extend, or tailor to niche policies (e.g., version pinning, optional features) that commercial resolvers may not expose.

**Practical Adoption Path**  
1. **Prototype** – Add the crate to a sandbox project, run the provided examples, and feed it a representative manifest to verify correctness and performance.  
2. **Integration feasibility study** – Examine the public API (resolver entry points, error types, and configuration structs) and map them to your existing dependency‑resolution pipeline. Because the README is sparse, you’ll likely need to read the source or generated docs to understand required data structures (e.g., `Package`, `Constraint`).  
3. **Wrap / adapt** – If your system is not Rust‑native, create a thin C‑ABI or gRPC wrapper around the resolver binary; the crate compiles to a static library with no external dependencies, simplifying cross‑language integration.  
4. **Testing & validation** – Run the resolver against your full dependency set, compare results with the current resolver, and add regression tests for edge cases (conflicts, optional dependencies, platform markers).  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update today) and has a modest community (220 stars, 29 forks), but the documentation and integration guides are limited.  
- **Risk**: The integration path is not obvious; you’ll need to allocate time for code‑review and possibly contribute missing glue code.  
- **Recommendation**: Suitable for internal tools, prototypes, or as a performance‑critical component in a larger Rust‑centric stack, provided you perform a thorough dependency audit and add comprehensive test coverage before promoting it to production.

### Русский

Резюме проекта prefix-dev/resolvo:

Решение prefix-dev/resolvo представляет собой быстрое решение для пакетного ресолвера на языке Rust, основанное на алгоритме CDCL для решения задач SAT. Это может быть полезно для определенных рабочих процессов, если README и активность проекта соответствуют конкретному сценарию использования. Проект готов к внедрению в прототипах или внутренних рабочих процессах, но требует дополнительных проверок на производственную готовность.

### 中文

**项目简介**  
`prefix-dev/resolvo` 是一个用 Rust 编写的高速依赖包解析器，核心采用 CDCL（Conflict‑Driven Clause Learning）技术实现 SAT 求解，能够在复杂依赖图中快速找到可行的安装方案。

**价值**  
- **性能优势**：基于 SAT 求解的算法在大规模依赖树上比传统的回溯式解析快数倍，适合需要频繁解析或对响应时间敏感的场景。  
- **Rust 生态**：使用安全且零成本抽象的 Rust 实现，易于在已有 Rust 项目或跨语言 FFI 场景中嵌入，兼具安全性和可维护性。  
- **可定制**：提供底层求解器接口，开发者可以在此基础上实现自定义的约束（例如平台、版本策略）而无需重新实现求解逻辑。

**典型接入方式**  
1. **作为库直接引入**：在 `Cargo.toml` 中加入 `resolvo = { git = "https://github.com/prefix-dev/resolvo" }`，然后在代码中使用 `resolvo::Solver` 创建求解器实例，提供依赖列表和约束即可获得解析结果。  
2. **CLI 包装**：项目自带的 `resolvo-cli` 可作为独立的命令行工具，在 CI/CD 流程或脚本中调用 `resolvo resolve <manifest>`，返回 JSON/YAML 格式的解析方案，便于与其他构建系统集成。  
3. **FFI / 微服务**：如果主系统不是 Rust，可以通过 `cbindgen` 生成 C 接口或将解析器封装成轻量的 HTTP 微服务（例如使用 `actix-web`），其他语言通过 REST 调用获取解析结果。

**生产可用性**  
- **成熟度**：当前拥有约 220 个 GitHub ★、29 个 fork，最近一次提交为 2026‑07‑06，活跃度尚可。  
- **适用范围**：适合作为原型验证、内部工具或对解析速度有严格要求的服务。直接用于面向外部用户的生产环境仍需进行：  
  - **依赖审计**：检查其依赖链是否符合贵公司的安全合规政策。  
  - **错误处理**：验证在异常依赖（循环、冲突）情况下的错误报告是否满足业务需求。  
  - **监控与回滚**：为解析过程添加超时、日志和回滚机制，以防 SAT 求解出现异常耗时。  
- **总体评估**：在做好上述检查后，可在内部或受控的生产环境中使用；若需要更高的 SLA（如 99.99% 可用），建议在关键路径上加入冗余或 fallback 到成熟的成熟解析器（如 `cargo`、`conda`）。  

> **总结**：`resolvo` 在性能和可定制性上提供了显著优势，适合作为依赖解析的加速层或内部工具。接入方式灵活，生产使用时需进行依赖审计和容错设计，方可达到中等到高的可靠性要求。

## 🧭 Practical evaluation

**Value:** prefix-dev/resolvo may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 220 GitHub stars
- 29 forks
- updated 2026-07-06
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 50/100 |
| topics | 0/100 |
| outlook | 65/100 |
| quality | 61/100 |
| recency | 100/100 |
| adoption | 46/100 |
| production | 67/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/prefix-dev/resolvo) · [← Back to Misc](./README.md)</sub>
