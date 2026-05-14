# ch32-rs/ch32-hal

[![Stars](https://img.shields.io/github/stars/ch32-rs/ch32-hal?style=flat-square&color=yellow)](https://github.com/ch32-rs/ch32-hal/stargazers) [![Forks](https://img.shields.io/github/forks/ch32-rs/ch32-hal?style=flat-square&color=blue)](https://github.com/ch32-rs/ch32-hal/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> A Rust HAL implementation for the CH32V0, CH32V1, CH32V2, CH32V3, CH32X0, CH32L1 family, with Embassy framework support and compatible with embedded-hal.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 203 |
| 🍴 **Forks** | 65 |
| 💻 **Language** | Rust |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`async` `drivers` `embedded` `hal` `rust`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
`ch32-rs/ch32-hal` is a Rust hardware‑abstraction‑layer (HAL) for the WCH CH32 series of MCUs (CH32V0‑V3, CH32X0, CH32L1). It implements the `embedded‑hal` traits, adds optional support for the async‑first Embassy framework, and is kept up‑to‑date (last commit 2026‑05‑13).

**Value proposition**  
- **Native Rust support** for a family of low‑cost, 32‑bit RISC‑V MCUs that are otherwise underserved in the Rust ecosystem.  
- **Compatibility with `embedded‑hal`** means existing driver crates (e.g., `embedded‑graphics`, `rtic`, sensor libraries) can be reused with little or no modification.  
- **Embassy integration** enables async programming, low‑power tickless operation, and easy multitasking for projects that already use the Embassy runtime.  
- **Open‑source and community‑driven** (≈200 stars, 65 forks) provides a transparent development process and the possibility to contribute fixes or extensions.

**Practical adoption path**  
1. **Read the README & examples** – verify that the target MCU (e.g., CH32V103) is listed and that the required toolchain (RISC‑V GNU, `cargo embed`/`probe‑rs`) is supported.  
2. **Create a minimal proof‑of‑concept**: start a new Cargo project, add `ch32-hal` as a dependency, and compile a “blink” example for the exact board you own. This validates the build chain, linker script, and any required BSP crates.  
3. **Integrate with existing code**: replace the current HAL (or raw register access) with `ch32-hal` by swapping the peripheral types to those exported by the crate. Because it follows `embedded‑hal`, most driver code should compile unchanged.  
4. **Add Embassy (optional)**: if your firmware already uses async/await, enable the `embassy` feature and migrate tasks to Embassy executors.  
5. **Run the test suite** (if any) and perform a hardware‑in‑the‑loop sanity check (timing, power, peripheral I/O).  

**Production readiness**  
- **Maturity**: The crate is actively maintained (last update 2026‑05‑13) and has a modest but active community.  
- **Stability**: It follows the stable `embedded‑hal` API, which is a de‑facto standard for Rust‑embedded drivers, reducing future breakage.  
- **Risk factors**:  
  * The integration documentation is limited to the README and example projects, so onboarding may require some trial‑and‑error.  
  * The ecosystem around CH32 devices (debug probes, board support packages) is smaller than for STM32 or nRF families, potentially increasing setup time.  
  * No formal LTS or semantic‑version guarantees are advertised; you should pin the crate version and monitor upstream changes.  

Overall, `ch32-rs/ch32-hal` is **suitable for prototypes, internal tools, or products that can tolerate a modest integration effort**. With a small PoC and a version lock, it can be promoted to production, provided you perform the usual dependency‑audit and long‑term maintenance checks.

### Русский

**ch32-rs/ch32-hal** — это открытая Rust‑библиотека HAL для микроконтроллеров семейства CH32 (V0‑V3, X0, L1), реализующая интерфейсы `embedded-hal` и поддерживающая асинхронный фреймворк Embassy. Она подходит для быстрого прототипирования или внутренних проектов, где требуется прямой доступ к периферии CH32 и возможность писать асинхронный код, однако перед выводом в продакшн следует проверить совместимость с конкретным пайплайном (чтение README, сборка небольшого POC) и оценить поддержку и обновляемость зависимостей. В текущем состоянии проект имеет умеренную готовность к продакшн‑использованию: достаточно зрелый (≈200 звёзд, активные коммиты), но требует отдельного валидационного этапа.

### 中文

**项目简介**  
ch32-rs/ch32-hal 是面向 CH32V0、CH32V1、CH32V2、CH32V3、CH32X0、CH32L1 系列 MCU 的 Rust 硬件抽象层实现，兼容 `embedded‑hal` 并提供对 Embassy 异步框架的原生支持。  

**价值**  
- **统一 API**：一次编写的驱动代码即可在同一家族的不同芯片上复用，降低移植成本。  
- **Rust 生态**：利用 Rust 的安全特性（所有权、零成本抽象）提升固件可靠性。  
- **异步支持**：通过 Embassy，可在资源受限的 MCU 上使用 async/await，简化并发任务的组织。  
- **社区活跃**：已有 200+ 星、65+ Fork，近期仍在维护，说明有一定的社区支撑。  

**典型接入方式**  
1. **在 Cargo.toml 中添加依赖**  
   ```toml
   [dependencies]
   ch32-hal = { git = "https://github.com/ch32-rs/ch32-hal", tag = "v0.3.0" }
   embassy = "0.2"
   embedded-hal = "1.0"
   ```  
2. **在代码中选择对应的芯片特性**（例如 `ch32v103`、`ch32l103`），并启用 Embassy 的 `executor`：  
   ```rust
   #[embassy_executor::task]
   async fn blink(mut led: ch32_hal::gpio::OutputPin) {
       loop {
           led.toggle().await;
           embassy::time::Delay::new().delay_ms(500).await;
       }
   }
   ```  
3. **初始化外设**：使用 `ch32_hal::pac`（外设访问层）配合 `ch32_hal::gpio`、`ch32_hal::serial` 等模块，按 `embedded-hal` trait 调用即可。  
4. **编译并下载**：使用 `cargo embed` 或 `probe-rs` 将固件烧录到目标板。  

**生产可用性**  
- **成熟度**：库已实现 `embedded-hal` 完整 trait，且通过 Embassy 的 CI 测试，适合原型和内部项目。  
- **维护状态**：最近一次提交在 2026‑05‑13，活跃度尚可，但仍需关注后续更新和安全补丁。  
- **风险**：文档主要在 README，部分高级特性（如 DMA、低功耗）示例较少；在大规模生产前建议：  
  1. **做小规模 PoC**，验证编译链、链接脚本和启动代码是否符合项目需求。  
  2. **审查依赖**（尤其是 Embassy 版本）是否与公司的长期支持策略匹配。  
  3. **建立内部测试套件**，覆盖关键外设的功能验证。  

综上，ch32-rs/ch32-hal 在需要 Rust + async 支持的 CH32 系列 MCU 项目中具备明显优势，适合作为原型或内部工具链的基础；在投入正式生产前，建议通过小范围验证并制定维护计划。

## 🧭 Practical evaluation

**Value:** ch32-rs/ch32-hal may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 203 GitHub stars
- 65 forks
- updated 2026-05-13
- primary language: Rust
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 49/100 |
| topics | 63/100 |
| outlook | 75/100 |
| quality | 71/100 |
| recency | 100/100 |
| adoption | 48/100 |
| production | 71/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/ch32-rs/ch32-hal) · [← Back to Misc](./README.md)</sub>
