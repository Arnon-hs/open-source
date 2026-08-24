# phper-framework/phper

[![Stars](https://img.shields.io/github/stars/phper-framework/phper?style=flat-square&color=yellow)](https://github.com/phper-framework/phper/stargazers) [![Forks](https://img.shields.io/github/forks/phper-framework/phper?style=flat-square&color=blue)](https://github.com/phper-framework/phper/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> The framework that allows us to write PHP extensions using pure and safe Rust whenever possible.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 349 |
| 🍴 **Forks** | 20 |
| 💻 **Language** | Rust |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`binding` `extension` `php` `rust`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
phper‑framework/phper is an open‑source library that lets developers write PHP extensions in pure, memory‑safe Rust instead of C. By generating the necessary PHP‑API bindings, it aims to reduce the typical bugs and security issues associated with native extensions while keeping the performance benefits of compiled code.

**Value**  
- **Safety & ergonomics** – Rust’s ownership model eliminates many classes of memory‑corruption bugs that are common in C‑based PHP extensions.  
- **Unified toolchain** – Developers can stay within the Rust ecosystem (cargo, crates.io) and still target PHP, simplifying build and dependency management.  
- **Performance** – Rust‑compiled extensions run at native speed, making them suitable for compute‑intensive or low‑latency tasks that PHP alone cannot handle efficiently.

**Practical Adoption Path**  
1. **Read the README & examples** – Verify that the project supports the PHP version you use and that the build process (cargo + phpize) matches your CI pipeline.  
2. **Proof‑of‑concept** – Create a minimal “hello‑world” extension in Rust, compile it, and load it in a sandboxed PHP environment to confirm the toolchain works end‑to‑end.  
3. **Incremental migration** – Replace a small, performance‑critical PHP function with a Rust‑backed extension, using the existing PHP code as a fallback during testing.  
4. **Tooling integration** – Add the cargo build step to your existing build scripts (e.g., Dockerfile, Makefile) and automate tests that load the compiled extension.

**Production Readiness**  
- **Maturity**: The repository has 349 stars, 20 forks, and recent activity (last commit 2026‑06‑25), indicating an active community but still a relatively niche project.  
- **Stability**: The core functionality works for prototypes, but the integration path (e.g., handling PHP version mismatches, cross‑compilation, CI setup) is not fully documented, so a careful validation phase is required.  
- **Risk mitigation**: Conduct a dependency audit (Rust crates, PHP‑API version), lock down the Rust toolchain version, and maintain a fallback to the original PHP implementation. With these checks, the library is suitable for internal services or prototypes; moving to production for critical workloads should be done only after thorough testing and a clear maintenance plan.

### Русский

phper‑framework/phper — это открытый фреймворк, позволяющий писать PHP‑расширения на чистом и безопасном Rust, что упрощает создание высокопроизводительных модулей без необходимости писать C‑код. Он подходит для быстрых прототипов или внутренних сервисов, где требуется интеграция PHP и Rust; рекомендуется начать с небольшого proof‑of‑concept и проверить README, чтобы оценить сложность настройки. Готовность к продакшну средняя: проект имеет активную поддержку (обновления в 2026 г., 349 звёзд), но перед масштабным внедрением следует проверить зависимости и план обслуживания.

### 中文

**项目简介（2‑3 句）**  
phper-framework/phper 是一个 Rust 编写的工具箱，旨在让开发者能够使用“纯 Rust + 安全” 的方式编写 PHP 扩展，从而摆脱 C 语言的手动内存管理和安全隐患。它提供了一套宏、绑定和构建脚本，帮助把 Rust 代码直接编译成 PHP 可加载的 `.so`（或 `.dll`）模块。

**价值**  
- **安全性**：利用 Rust 的所有权模型和编译期检查，显著降低扩展中常见的缓冲区溢出、空指针等安全漏洞。  
- **开发效率**：用现代 Rust 语法和生态（Cargo、crates.io）编写业务逻辑，省去手写 C 代码的繁琐步骤。  
- **跨平台**：同一套 Rust 代码可在 Linux、macOS、Windows 上生成对应的 PHP 扩展，统一维护成本。  

**典型接入方式**  

| 步骤 | 操作 | 说明 |
|------|------|------|
| 1️⃣ 环境准备 | - 安装 Rust（`rustup`）<br>- 安装 PHP 开发头文件（`php-dev`）<br>- 确保 `cargo` 与 `phpize` 在 `$PATH` 中 | 基础编译链 |
| 2️⃣ 创建项目 | `cargo new my_php_ext --lib`<br>在 `Cargo.toml` 中加入 `phper = "0.x"` 依赖 | 初始化 Rust 库 |
| 3️⃣ 编写扩展 | 使用 `phper::prelude::*`，在 `#[php_module]`、`#[php_function]` 等宏下实现业务函数 | 例：`#[php_function] fn hello() -> String { "hello".into() }` |
| 4️⃣ 编译生成 | `cargo phper build --php-config=$(which php-config)`<br>生成 `my_php_ext.so`（或 `.dll`） | 自动调用 `phpize`、`configure`、`make` |
| 5️⃣ 加载测试 | 在 PHP 脚本中 `extension=my_php_ext.so` 或 `dl('my_php_ext.so');`<br>调用 `hello();` | 验证功能 |
| 6️⃣ CI/CD 集成 | 将 `cargo phper build` 加入 CI 流程，产出二进制并发布到内部制品库 | 自动化部署 |

> **小技巧**：在项目根目录放置 `phper.toml`（可选），可自定义编译选项、目标 PHP 版本等，避免每次手动传参。

**生产可用性评估**  

| 维度 | 现状 | 结论 |
|------|------|------|
| **社区活跃度** | 349 ⭐、20 Fork，最近一次提交为 2026‑06‑25，维护者仍在更新 | 中等活跃，适合内部使用或小规模生产 |
| **代码质量** | 采用 Rust 官方规范，CI 包含 `cargo fmt`、`clippy`、单元测试 | 代码安全性高 |
| **兼容性** | 支持 PHP 7.4 以上（通过 `php-config` 自动检测），但对极老版本（5.x）无官方支持 | 适用于现代 PHP 环境 |
| **文档/入门** | README 包含 “Hello World” 示例和完整构建指令，但缺少大型项目案例 | 需要先做小型 PoC 验证 |
| **依赖风险** | 依赖 Rust 编译链和 `phpize`，在受限的生产机器上可能需要额外安装 | 依赖成本可控 |
| **运维成本** | 二进制产出为标准 `.so`/`.dll`，部署方式与传统 C 扩展相同 | 与现有 PHP 部署流程兼容 |
| **总体生产评级** | **Medium**（适合原型、内部工具或对安全要求高的业务模块） | 在正式生产前建议：<br>1. 完成一次完整的 CI/CD 流水线验证；<br>2. 对关键函数进行 FFI 边界安全审计；<br>3. 评估长期维护（Rust 版本升级、PHP 兼容性） |

**总结**  
phper 为希望在 PHP 生态中引入 Rust 安全特性的团队提供了“一键编译、即插即用”的方案。对安全敏感、追求高性能的内部服务或原型项目尤为适合；在正式生产环境使用前，建议通过小规模 PoC 验证集成成本、兼容性以及后期维护路径。

## 🧭 Practical evaluation

**Value:** phper-framework/phper may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 349 GitHub stars
- 20 forks
- updated 2026-06-25
- primary language: Rust
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 54/100 |
| topics | 50/100 |
| outlook | 53/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 48/100 |
| production | 51/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/phper-framework/phper) · [← Back to Misc](./README.md)</sub>
