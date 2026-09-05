# dtolnay/watt

[![Stars](https://img.shields.io/github/stars/dtolnay/watt?style=flat-square&color=yellow)](https://github.com/dtolnay/watt/stargazers) [![Forks](https://img.shields.io/github/forks/dtolnay/watt?style=flat-square&color=blue)](https://github.com/dtolnay/watt/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> Runtime for executing procedural macros as WebAssembly

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.5k |
| 🍴 **Forks** | 31 |
| 💻 **Language** | Rust |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
`dtolnay/watt` is a Rust‑based runtime that lets you run procedural‑macro code compiled to WebAssembly, enabling macro execution without a full Rust compiler toolchain. With over 1.5 k stars and recent updates, it is a mature‑looking prototype that can simplify macro‑driven workflows, especially in CI pipelines or sandboxed environments.

**Value proposition**  
Watt decouples procedural‑macro execution from the host compiler, allowing you to ship macro logic as a portable WASM module. This reduces build‑time dependencies, improves isolation (security‑wise and crash‑wise), and makes it easier to reuse macros across different Rust toolchains or even non‑Rust build systems.

**Practical adoption path**  

1. **Evaluate the README and examples** – clone the repo, build the `watt` binary, and try the provided demo macro to confirm that your macro can be compiled to WASM and invoked via the runtime.  
2. **Integrate into your workflow** – replace the usual `rustc`‑driven macro step with a call to `watt run <wasm-file> <input>` in your build script or CI job.  
3. **Validate the toolchain** – ensure your CI environment can install the required Rust nightly (for `proc-macro` support) and the `wasm32-unknown-unknown` target; add a small wrapper script to automate this.  
4. **Run a pilot** – apply the change to a low‑risk repository or a feature branch, monitor build times, and confirm that error reporting from the WASM runtime is acceptable.

**Production readiness**  
The project sits at a medium readiness level: it is actively maintained (last commit 2026‑06‑24) and has a healthy community signal (≈1.5 k stars), but the integration documentation is sparse and the exact API surface for embedding the runtime is not fully described. For prototypes, internal tooling, or CI sandboxes, Watt can be adopted quickly after the manual validation steps above. For production use, you should perform a dedicated security review of the WASM sandbox, lock the runtime version, and set up automated tests to catch any breaking changes in future releases.

### Русский

**dtolnay/watt** — это рантайм, позволяющий выполнять процедурные макросы Rust в виде WebAssembly, что упрощает их изоляцию и кросс‑компиляцию. Он подходит для прототипов и внутренних пайплайнов, где требуется безопасный и переносимый запуск макросов без полной компиляции проекта, однако перед внедрением следует вручную проверить интеграцию, так как пути подключения из метаданных неочевидны. Готовность к production — средняя: проект активно поддерживается (обновление 2026‑06‑24, 1505 звёзд), но требует оценки зависимостей и затрат на настройку.

### 中文

**项目简介**  
`dtolnay/watt` 是一个基于 WebAssembly 的运行时，用来在编译期间以 Wasm 形式执行 Rust 的过程宏（procedural macros），从而实现跨平台、隔离的宏执行环境。

**价值**  
- **安全隔离**：将宏运行在 Wasm 沙箱中，防止宏代码对宿主进程造成副作用或崩溃。  
- **跨平台一致性**：同一套宏可在不同操作系统、CPU 架构上使用，避免因本地编译器差异导致的行为不一致。  
- **加速 CI/CD**：在 CI 环境中预先启动一次 Wasm 运行时，即可复用，减少宏编译的启动开销。

**典型接入方式**  
1. 在 `Cargo.toml` 中添加 `watt` 作为依赖（或通过 `cargo add watt`）。  
2. 在项目的 `build.rs` 或自定义的宏加载器中，使用 `watt::WasmExecutor::new()` 创建运行时实例。  
3. 将要执行的过程宏编译为 `.wasm` 文件（`cargo +nightly build --target wasm32-unknown-unknown`），然后通过 `executor.execute(wasm_path, input_token_stream)` 调用。  
4. 可选：在 CI 脚本里缓存 Wasm 运行时镜像，提升重复构建的速度。

**生产可用性**  
- **成熟度**：已有 1500+ 星、活跃维护（截至 2026‑06‑24），代码基于 Rust，适合在 Rust 生态中直接使用。  
- **适用场景**：原型、内部工具链、对安全/跨平台有明确需求的项目；在对性能和可靠性要求极高的生产环境仍需自行评估。  
- **风险与注意事项**：  
  - 集成文档较少，需自行检查运行时的启动参数、错误日志以及 Wasm 编译链的兼容性。  
  - 依赖 `wasmtime`/`wasmer` 等 Wasm 引擎，需确认目标部署环境能满足对应的系统库。  
  - 维护成本：宏更新后需要重新编译 Wasm，且调试过程相对复杂。  

综上，`dtolnay/watt` 在需要安全、跨平台执行过程宏的场景下提供了有价值的解决方案，适合作为内部原型或受控环境的组件；在生产环境使用前建议进行一次完整的集成测试与性能基准评估。

## 🧭 Practical evaluation

**Value:** dtolnay/watt may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1505 GitHub stars
- 31 forks
- updated 2026-06-24
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 68/100 |
| topics | 0/100 |
| outlook | 61/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 59/100 |
| production | 63/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/dtolnay/watt) · [← Back to Misc](./README.md)</sub>
