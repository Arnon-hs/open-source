# oxidecomputer/usdt

[![Stars](https://img.shields.io/github/stars/oxidecomputer/usdt?style=flat-square&color=yellow)](https://github.com/oxidecomputer/usdt/stargazers) [![Forks](https://img.shields.io/github/forks/oxidecomputer/usdt?style=flat-square&color=blue)](https://github.com/oxidecomputer/usdt/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-38%2F100-brightgreen?style=flat-square)](#)

> Dust your Rust with USDT probes

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 135 |
| 🍴 **Forks** | 15 |
| 💻 **Language** | Rust |
| 📈 **Score** | 38/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
oxidecomputer/usdt is a Rust library that provides USDT (User‑Space Statically‑Defined Tracing) probes, letting developers instrument their applications with low‑overhead, dynamically‑enabled trace points. With 135 GitHub stars and recent activity (last updated 2026‑05‑11), it’s a mature, community‑tested option for adding observability to Rust codebases, especially in prototype or internal‑tool scenarios.

**Value**  
- **Fine‑grained observability**: USDT probes let you emit rich, contextual data without recompiling or restarting the target process, which is ideal for performance‑critical Rust services.  
- **Zero‑cost when disabled**: The probes compile to no‑op code unless enabled by a tracing backend, keeping runtime overhead negligible.  
- **Rust‑native API**: The crate offers idiomatic macros and types, making it straightforward to embed probes directly in existing Rust modules.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Evaluate the README & examples** – clone the repo, run `cargo test` and the provided demo binaries. | Confirms the library builds with your toolchain (Rust 1.70+). |
| 2️⃣  | **Add the crate** – add `usdt = "0.x"` to `Cargo.toml` and import the macros (`use usdt::probe;`). | Minimal dependency impact; the crate is small and pure‑Rust. |
| 3️⃣  | **Instrument key code paths** – sprinkle `probe!("name", arg1, arg2);` where you need visibility. | Start with a few high‑traffic functions to limit initial surface. |
| 4️⃣  | **Select a USDT consumer** – DTrace, BPFtrace, or a Rust‑based collector (e.g., `usdt-bpf`). | The probes are backend‑agnostic; choose what fits your observability stack. |
| 5️⃣  | **Validate locally** – run the binary, enable the probe set with the consumer, and verify that events appear as expected. | Guarantees the instrumentation works before CI integration. |
| 6️⃣  | **CI/CD integration** – add a lint step that checks the crate builds and optionally runs a smoke‑test with a headless BPFtrace script. | Prevents regressions and ensures probes stay functional across releases. |
| 7️⃣  | **Roll out to staging** – enable probes in a controlled environment, monitor performance impact, and tune probe frequency. | Confirms zero‑cost behavior and validates operational tooling. |

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑05‑11) and has a healthy star count, indicating community interest, but documentation around integration patterns is sparse.  
- **Risk**: The integration path isn’t fully described in the metadata; you’ll need to manually verify that your tracing backend (DTrace/BPFtrace/etc.) can consume the generated USDT sections.  
- **Recommended use**: Ideal for prototypes, internal services, or as a stepping stone toward full observability. For production, perform a dedicated validation phase—build, instrument, and benchmark the instrumented binary, and confirm that your observability pipeline reliably captures and stores the probe data. Once those checks pass, the crate can be promoted to production with confidence.

### Русский

**oxidecomputer/usdt** — это библиотека на Rust, предоставляющая USDT‑пробки (User‑Space Dynamic Tracing) для детального наблюдения за выполнением кода без изменения исходников. Она подходит для прототипов и внутренних инструментов, где требуется гибкая трассировка — например, при отладке производительности микросервисов или построении кастомных профайлеров. Проект имеет умеренную готовность к production: активное развитие (обновление — 2026‑05‑11, 135 ★), но интеграция требует ручного анализа и проверки зависимостей, поэтому рекомендуется использовать её после предварительного тестирования в контролируемой среде.

### 中文

**项目简介**  
oxidecomputer/usdt 是一个用 Rust 编写的 USDT（User‑Space DTrace）探针库，旨在帮助开发者在 Rust 程序中快速埋点、实时观测内部状态，适合调试、性能分析以及运行时诊断。

**价值**  
- **低侵入式监控**：通过 USDT 探针在不修改业务逻辑的前提下获取细粒度运行时信息。  
- **Rust 原生支持**：提供宏和 API，直接在 Rust 代码中声明、触发探针，避免跨语言桥接的复杂性。  
- **快速定位问题**：配合系统的 DTrace、bpftrace 等工具，可在生产环境实时追踪异常路径，提升故障排查效率。

**典型接入方式**  
1. **在 Cargo.toml 中添加依赖**  
   ```toml
   [dependencies]
   usdt = { git = "https://github.com/oxidecomputer/usdt", rev = "最新提交哈希" }
   ```  
2. **在代码中声明探针**  
   ```rust
   use usdt::register_probes;
   
   register_probes! {
       probe my_module, request_start(arg1: u64, arg2: &str);
       probe my_module, request_end(status: i32);
   }
   ```  
3. **在关键位置触发**  
   ```rust
   usdt::fire!(my_module, request_start, request_id, &path);
   // 业务代码…
   usdt::fire!(my_module, request_end, 200);
   ```  
4. **使用 DTrace / bpftrace 进行观察**  
   ```bash
   sudo bpftrace -e 'usdt:my_module:request_start { printf("request %d %s\n", arg0, str(arg1)); }'
   ```

**生产可用性**  
- **成熟度**：GitHub 135 ⭐、15 Fork，最近一次提交在 2026‑05‑11，活跃度尚可。  
- **适用场景**：非常适合原型、内部工具或对可观测性要求高的服务；在正式生产环境使用前，建议完成以下检查：  
  1. **兼容性验证**：确认目标运行环境（Linux、macOS）支持 USDT 并已安装相应的 tracing 工具。  
  2. **依赖审计**：评估库的 transitive dependencies，确保没有安全或许可证风险。  
  3. **性能基准**：在预上线环境进行基准测试，量化探针开启/关闭时的开销。  
- **风险**：元数据中未提供完整的接入指南，实际集成路径需要手动阅读源码和示例；若业务对探针的可靠性要求极高，建议在内部进行充分的验证后再推广。  

总体而言，oxidecomputer/usdt 在 Rust 项目中提供了轻量且强大的可观测手段，适合作为内部调试或原型阶段的监控方案；在生产环境使用时，需要进行依赖、兼容性和性能的额外评估。

## 🧭 Practical evaluation

**Value:** oxidecomputer/usdt may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 135 GitHub stars
- 15 forks
- updated 2026-05-11
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 30/100 |
| stars | 45/100 |
| topics | 0/100 |
| outlook | 36/100 |
| quality | 39/100 |
| recency | 20/100 |
| adoption | 41/100 |
| production | 40/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/oxidecomputer/usdt) · [← Back to Misc](./README.md)</sub>
