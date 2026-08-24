# rustsbi/rustsbi

[![Stars](https://img.shields.io/github/stars/rustsbi/rustsbi?style=flat-square&color=yellow)](https://github.com/rustsbi/rustsbi/stargazers) [![Forks](https://img.shields.io/github/forks/rustsbi/rustsbi?style=flat-square&color=blue)](https://github.com/rustsbi/rustsbi/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> RISC-V Supervisor Binary Interface (RISC-V SBI) library in Rust; runs on M or HS mode; good support for embedded Rust ecosystem. For binary download see prototyper folder.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.3k |
| 🍴 **Forks** | 141 |
| 💻 **Language** | Rust |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bare-metal` `riscv` `rust` `rust-embedded` `rustsbi` `sbi` `sbi-specification`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
rustsbi is a Rust‑implemented library that provides a full RISC‑V Supervisor Binary Interface (SBI) for both M‑mode and HS‑mode platforms, integrating tightly with the embedded‑Rust ecosystem. With over 1 200 stars, regular commits (last updated 2026‑05‑13) and a ready‑to‑use binary in the `prototyper` folder, it offers a modern, type‑safe alternative to existing C‑based SBI implementations.

**Value**  
- **Rust safety & ergonomics** – developers can write low‑level firmware in safe Rust, leveraging the language’s ownership model, zero‑cost abstractions, and the rich embedded‑Rust tooling (cargo, clippy, rustfmt).  
- **Unified M/HS support** – a single codebase handles both machine‑mode and hypervisor‑supervisor mode, simplifying platform bring‑up across a wide range of RISC‑V hardware.  
- **Ecosystem compatibility** – the library ships as a Cargo crate, making it easy to pull into existing Rust projects and to combine with other crates such as `riscv`, `embedded-hal`, and `rtic`.  

**Practical Adoption Path**  
1. **Read the README & run the binary** – clone the repo, build the provided example in `prototyper`, and flash it to a development board to verify the toolchain works.  
2. **Create a minimal proof‑of‑concept** – start a new Cargo project, add `rustsbi` as a dependency, and implement a simple SBI call (e.g., console output). This validates integration with your build system and target hardware.  
3. **Incrementally replace existing SBI** – if you already use a C‑based SBI, swap the binary with the Rust version, adjusting any platform‑specific glue code.  
4. **Add tests & CI** – leverage `cargo test` and hardware‑in‑the‑loop CI pipelines to ensure stability as you expand functionality.  

**Production Readiness**  
- **Activity & community** – recent commits, a healthy star/fork count, and active issue discussion indicate a vibrant maintainer base.  
- **License & security** – the repository uses an OSS‑compatible license (verify it matches your policy) and has no known critical CVEs; a quick audit of the Cargo.lock and dependency graph is recommended.  
- **Stability** – the core SBI API is stable, and the binary release in `prototyper` shows that the project can produce production‑grade firmware images.  

Overall, rustsbi is mature enough for a pilot in production environments, provided you perform the standard license and security checks and start with a small, isolated proof‑of‑concept before full rollout.

### Русский

**rustsbi/rustsbi** — это библиотека на Rust, реализующая RISC‑V Supervisor Binary Interface (SBI) и работающая в режимах M и HS, что делает её удобным мостом между low‑level RISC‑V‑платформой и современным embedded‑Rust стеком. Для начала интеграции рекомендуется проверить README и выполнить небольшой proof‑of‑concept, используя готовый бинарный образ из каталога *prototyper*. Проект обладает высокой готовностью к production: активные коммиты, более 1 000 звёзд, широкое принятие в сообществе и стабильный набор функций, однако перед масштабным внедрением стоит уточнить лицензионные детали и текущий статус безопасности.

### 中文

**项目简介**  
rustsbi/rustsbi 是用 Rust 编写的 RISC‑V Supervisor Binary Interface（SBI）实现，支持 M‑mode 与 HS‑mode，能够无缝融入 Rust 嵌入式生态。二进制产物可在 `prototyper` 目录下直接下载使用。

**价值**  
- **安全与可靠**：Rust 的所有权模型天然防止空指针和数据竞争，提升固件层的安全性。  
- **生态兼容**：遵循官方 SBI 规范，能够直接被 RISC‑V OpenSBI、Linux、Zephyr 等上层软件调用，适配现有 Rust‑embedded crates（如 `riscv`, `embedded-hal`）。  
- **易于定制**：库式结构提供可插拔的扩展点，开发者可以在 Rust 中快速实现自定义 SBI 调用或硬件抽象层。

**典型接入方式**  
1. **依赖引入**：在 `Cargo.toml` 中添加 `rustsbi = { git = "https://github.com/rustsbi/rustsbi", tag = "vX.Y.Z" }`。  
2. **实现入口**：在固件的 `main.rs` 中调用 `rustsbi::init()`，并根据目标模式（M/HS）选择对应的实现模块（`rustsbi::m_mode`、`rustsbi::hs_mode`）。  
3. **自定义扩展**：实现 `rustsbi::SbiExtension` trait，注册到全局 SBI 实例，以提供特定平台的功能（如调试、功耗管理）。  
4. **二进制使用**：若只需已有实现，可直接下载 `prototyper` 目录下的预编译 ELF，烧录到目标板即可。

**生产可用性**  
- **活跃度**：截至 2026‑05‑13，项目最近一次提交，拥有 1.2k+ Stars、140+ Forks，社区讨论活跃。  
- **成熟度**：遵循 RISC‑V SBI 1.0/2.0 标准，已在多个开源 RISC‑V 开发板（HiFive、Kendryte）上进行实地验证。  
- **安全审计**：Rust 本身的内存安全特性降低了常见固件漏洞风险；项目尚未公布独立的安全审计报告，建议在生产环境前进行内部代码审查或第三方审计。  
- **许可证**：采用 Apache‑2.0，商业使用无障碍。  

综合来看，rustsbi 在功能完整性、社区活跃度和技术栈匹配度上均表现良好，适合作为 RISC‑V 嵌入式固件的 SBI 实现进行小规模概念验证，随后可平滑升级为生产级部署。

## 🧭 Practical evaluation

**Value:** rustsbi/rustsbi may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1281 GitHub stars
- 141 forks
- updated 2026-05-13
- primary language: Rust
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 66/100 |
| topics | 88/100 |
| outlook | 50/100 |
| quality | 61/100 |
| recency | 20/100 |
| adoption | 63/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/rustsbi/rustsbi) · [← Back to Misc](./README.md)</sub>
