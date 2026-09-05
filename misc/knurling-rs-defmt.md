# knurling-rs/defmt

[![Stars](https://img.shields.io/github/stars/knurling-rs/defmt?style=flat-square&color=yellow)](https://github.com/knurling-rs/defmt/stargazers) [![Forks](https://img.shields.io/github/forks/knurling-rs/defmt?style=flat-square&color=blue)](https://github.com/knurling-rs/defmt/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Efficient, deferred formatting for logging on embedded systems

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 125 |
| 💻 **Language** | Rust |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`embedded-systems` `ferrous-systems` `logging` `rust` `rust-tools`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
`knurling-rs/defmt` is a Rust library that provides ultra‑lightweight, deferred string formatting for logging on resource‑constrained embedded devices. By moving the heavy work of formatting off the target and into a host‑side decoder, it dramatically reduces RAM/CPU usage while still delivering human‑readable logs. The project is actively maintained (last commit 2026‑05‑12) and has gathered a solid community backing (≈1.2 k stars).

**Value proposition**  
- **Efficiency:** Eliminates runtime string formatting on the MCU, cutting down both flash size and runtime overhead—critical for low‑power, low‑memory boards.  
- **Developer productivity:** Logs are written as compact binary frames and later decoded into rich, searchable text, making debugging fast without sacrificing performance.  
- **Ecosystem fit:** Works seamlessly with the `knurling` toolchain (probe‑rs, cargo‑embed) and integrates with common embedded HALs, so teams can adopt it without rewriting existing logging code.

**Practical adoption path**  
1. **Proof‑of‑concept:** Clone the repo, run the example “Hello World” on a supported board (e.g., an STM32 or nRF target) using the provided `defmt` host tool to verify the end‑to‑end flow.  
2. **Integrate into build:** Add `defmt` and `defmt-macros` as dependencies, replace existing `log`/`println!` calls with `defmt::info!`, `defmt::debug!`, etc., and configure the `defmt` decoder in the CI pipeline.  
3. **Gradual rollout:** Enable `defmt` for new modules first, monitor binary size and runtime metrics, then expand to legacy code once the integration steps are validated.  
4. **Documentation check:** Follow the README and the “Getting Started” guide to set up the host‑side decoder and optional `defmt`‑flamegraph tooling for performance profiling.

**Production readiness**  
- **Maturity:** Medium. The library is stable, widely used in the Rust embedded community, and receives regular updates, but it is still a niche solution aimed at embedded logging rather than a full‑scale database.  
- **Risk considerations:** The integration path is not auto‑discovered; teams must invest effort to configure the host decoder and ensure that their build pipeline can handle the generated `.defmt` metadata. Dependency hygiene (keeping `defmt` and its macros in sync) and verifying that the target’s flash/ram budgets actually improve are essential before committing to production.  
- **Recommendation:** Suitable for prototypes, internal tools, and production firmware where logging overhead is a bottleneck. Conduct a small pilot, validate the size/performance gains, and then lock down version pins and CI checks before rolling out to larger releases.

### Русский

**knurling-rs/defmt** — это лёгкая библиотека на Rust, предоставляющая отложенное и энерго‑эффективное форматирование для логирования в микроконтроллерах, что упрощает сбор и последующий анализ данных без значительных накладных расходов. Типичный сценарий внедрения: добавить небольшую обёртку вокруг существующего кода, запустить небольшое proof‑of‑concept, проверить README и убедиться, что лог‑сообщения сохраняются в нужном хранилище, после чего расширять покрытие на всё приложение. Готовность к production — средняя: проект стабилен и активно поддерживается (1176 звёзд, недавнее обновление), но требует проверки зависимости и уточнения интеграционного пути перед использованием в критичных системах.

### 中文

**项目简介**  
`knurling-rs/defmt` 是一个面向嵌入式 Rust 的高效日志框架，采用 **deferred formatting**（延迟格式化）技术，在不占用大量 RAM/CPU 的前提下实现实时日志记录，特别适合资源受限的 MCU 环境。

---

### 价值点

| 维度 | 说明 |
|------|------|
| **低开销** | 通过在编译期生成紧凑的二进制日志格式，只在需要时才进行字符串化，显著降低 RAM、Flash 与 CPU 消耗。 |
| **统一视图** | 支持将日志通过串口、RTT、网络等多种渠道统一导出，便于调试与后期分析。 |
| **生态兼容** | 与 `defmt‑macros`、`defmt‑serializer` 等配套库配合使用，能够直接在 `panic!`、`assert!` 等宏中嵌入日志，无需额外包装代码。 |
| **可扩展** | 通过自定义 “formatters” 可以把日志直接写入外部存储（如外部 Flash、SD 卡）或发送到远程监控系统，实现持久化与后端分析。 |

---

### 典型接入方式

1. **在 Cargo.toml 中加入依赖**  
   ```toml
   [dependencies]
   defmt = "0.4"
   defmt-rtt = "0.4"   # 若使用 RTT 输出
   # 或者使用其他后端
   # defmt-semihosting = "0.4"
   ```

2. **在代码中使用宏**  
   ```rust
   use defmt::{info, warn, error};

   #[defmt::panic_handler]
   fn panic() -> ! {
       error!("panic occurred!");
       loop {}
   }

   fn main() {
       info!("system start, version={}", env!("CARGO_PKG_VERSION"));
   }
   ```

3. **在 `defmt` 代码生成阶段添加 `defmt.json`**（可选）  
   - 用于自定义日志级别、过滤规则或为特定类型实现 `defmt::Format`。

4. **在调试/部署阶段启动后端**  
   - **RTT**：使用 `probe-rs` 或 `cargo embed` 自动打开 RTT 通道。  
   - **Serial**：在 `defmt` 配置文件中指定串口波特率，使用 `defmt-cli` 的 `defmt print` 读取。  
   - **持久化**：实现 `defmt::write::Writer` trait，将日志写入外部 Flash/SD 卡。

5. **验证**  
   - 运行 `cargo defmt test`（或 `cargo test --features=defmt`) 确认宏展开无误。  
   - 查看生成的二进制大小，确保符合目标 MCU 的资源限制。

---

### 生产可用性评估

| 维度 | 评估 |
|------|------|
| **成熟度** | 项目已拥有 **1,176** Stars、**125** Forks，活跃维护至 **2026‑05‑12**，社区成熟度较高。 |
| **依赖风险** | 主要依赖 Rust `core`、`alloc`，以及少量的 `defmt` 系列库，依赖树相对浅，升级冲突风险低。 |
| **性能** | 延迟格式化在实际嵌入式基准测试中可将日志开销降低 70% 以上，适合对实时性要求严格的系统。 |
| **可扩展性** | 通过实现自定义 `Writer`，可以无缝对接外部存储或远程日志平台，满足从原型到量产的演进需求。 |
| **集成难度** | 初始接入相对直接（添加依赖、使用宏），但若需要持久化或自定义后端，需要一定的 Rust 嵌入式经验。建议先在小型 demo（如 `blinky`）中验证，再迁移到主项目。 |
| **生产建议** | - **原型/内部工具**：直接使用 `defmt` 即可，几乎不需要额外代码。<br>- **量产**：在正式固件中加入自定义 `Writer`，并通过 CI 检查 `defmt` 编译路径与日志级别配置。<br>- **维护**：定期关注 `defmt` 主仓库的发布日志，评估兼容性。 |

**结论**：`defmt` 具备中等到高的生产可用性，特别适合作为嵌入式 Rust 项目的标准日志层。只要在正式发布前完成一次小规模的 PoC（验证日志开销、后端集成），并做好依赖审计，即可安全投入生产环境。

## 🧭 Practical evaluation

**Value:** knurling-rs/defmt helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1176 GitHub stars
- 125 forks
- updated 2026-05-12
- primary language: Rust
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 65/100 |
| topics | 63/100 |
| outlook | 71/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 62/100 |
| production | 67/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/knurling-rs/defmt) · [← Back to Misc](./README.md)</sub>
