# Enet4/dicom-rs

[![Stars](https://img.shields.io/github/stars/Enet4/dicom-rs?style=flat-square&color=yellow)](https://github.com/Enet4/dicom-rs/stargazers) [![Forks](https://img.shields.io/github/forks/Enet4/dicom-rs?style=flat-square&color=blue)](https://github.com/Enet4/dicom-rs/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> Rust implementation of the DICOM standard

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 546 |
| 🍴 **Forks** | 120 |
| 💻 **Language** | Rust |
| 📈 **Score** | 48/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dicom` `dicom-standard` `hacktoberfest` `medical-imaging` `rust`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`Enet4/dicom-rs` is a Rust library that implements the DICOM (Digital Imaging and Communications in Medicine) standard, enabling reading, writing, and manipulating medical imaging data directly from Rust applications. With over 500 GitHub stars and recent activity (last commit 2026‑06‑26), it offers a modern, memory‑safe alternative to existing C/C++ DICOM toolkits. The project is most suitable for teams that already use Rust or are evaluating Rust for imaging‑related prototypes.

**Value**  
- **Safety & Performance** – Leveraging Rust’s ownership model, the library provides thread‑safe handling of large DICOM files without the typical memory‑management bugs of C‑based solutions.  
- **Ecosystem Fit** – For organizations building microservices, data pipelines, or command‑line tools in Rust, `dicom-rs` eliminates the need for foreign‑function interfaces or external binaries.  
- **Community Momentum** – 546 stars and 120 forks indicate an active community, which can help with troubleshooting and extending functionality.

**Practical Adoption Path**  
1. **Read the README & Examples** – Verify that the supported DICOM features (e.g., transfer syntaxes, anonymization, tag parsing) align with your workflow.  
2. **Proof‑of‑Concept** – Create a small Rust crate that loads a sample DICOM file, extracts key tags, and optionally writes a modified file. This validates the API surface and build integration.  
3. **Dependency Review** – Audit the crate’s transitive dependencies for licensing, security advisories, and maintenance frequency.  
4. **Integration Layer** – If your system is not Rust‑native, wrap the library in a thin FFI or expose it via a gRPC/HTTP microservice to keep the rest of the stack language‑agnostic.  
5. **Testing & CI** – Add unit and integration tests that cover your specific DICOM use cases; run the library’s own test suite to catch regressions early.

**Production Readiness**  
- **Maturity**: Medium. The library is actively maintained and stable enough for prototypes or internal tooling, but it lacks the extensive validation suites and regulatory certifications (e.g., IEC 62304) typical of medical‑device‑grade SDKs.  
- **Risks**: Integration pathways are not fully documented; you’ll need to invest time in understanding the API and handling edge‑case DICOM variants.  
- **Mitigations**: Conduct a thorough code audit, pin the crate version, and consider adding a fallback to a proven C/C++ DICOM library for critical paths until you are confident in `dicom‑rs`’ coverage.

In short, `dicom‑rs` is a promising option for Rust‑centric teams looking to handle DICOM data safely and efficiently, provided you start with a small proof of concept, verify feature coverage, and perform the usual production‑grade checks before rolling it out to mission‑critical systems.

### Русский

Enet4/dicom-rs — это открытая библиотека на Rust, реализующая стандарт DICOM и позволяющая быстро парсить, создавать и модифицировать медицинские изображения в проектах, где уже используется Rust‑стек. Типичный сценарий внедрения — небольшая proof‑of‑concept‑модуль, который читает DICOM‑файлы из PACS, извлекает метаданные и передаёт их в аналитический pipeline; после проверки README и примеров можно расширять интеграцию в более крупные внутренние сервисы. Библиотека имеет средний уровень готовности к production: 546 звёзд, активные коммиты и хорошая документация делают её подходящей для прототипов и внутренних workflow, но перед выпуском в продакшн стоит оценить зависимости, стабильность API и планировать небольшие тесты на совместимость.

### 中文

**项目价值**  
Enet4/dicom‑rs 是用 Rust 编写的 DICOM（医学影像）标准实现，具备以下优势：  
- **安全高效**：Rust 的所有权模型天然防止内存泄漏与数据竞争，适合处理大容量医学影像数据。  
- **生态友好**：提供完整的 DICOM 元数据解析、文件 I/O、网络传输（C‑STORE / C‑GET 等）等核心功能，能够直接在 Rust 项目中复用，省去自行实现协议的成本。  
- **活跃社区**：已有 546+ Stars、120+ Forks，且最近一次提交在 2026‑06‑26，说明代码仍在维护。

**典型接入方式**  

| 场景 | 接入步骤 | 关键代码示例 |
|------|----------|------------|
| **原型/内部工具** | 1. 在 `Cargo.toml` 中加入 `dicom-rs = { git = "https://github.com/Enet4/dicom-rs", branch = "main" }` <br>2. 使用库的 `dicom_object::open_file` 读取 DICOM 文件 <br>3. 通过 `dicom_transfer::client::Client` 发起 C‑STORE | ```rust\nuse dicom_object::open_file;\nuse dicom_transfer::client::Client;\nlet obj = open_file(\"sample.dcm\").unwrap();\nlet client = Client::new(\"127.0.0.1:104\");\nclient.store(&obj).await.unwrap();\n``` |
| **后端服务** | 1. 将库封装为内部服务（如 gRPC/REST），提供 `upload`, `download`, `query` 接口 <br>2. 结合 `tokio` 异步运行时，实现并发的 DICOM 传输 <br>3. 使用 `serde` 将 DICOM 元数据序列化为 JSON 供前端展示 | ```rust\n#[tokio::main]\nasync fn main() {\n    let svc = DicomService::new();\n    tonic::transport::Server::builder()\n        .add_service(svc)\n        .serve(\"[::1]:50051\".parse().unwrap())\n        .await.unwrap();\n}\n``` |
| **CI/CD 验证** | 在 CI 中加入 `cargo test --features=network`，利用库的测试套件对 DICOM 文件的合法性进行自动检查 | ```yaml\n- name: Run dicom-rs tests\n  run: cargo test --all-features\n``` |

**生产可用性评估**  

| 维度 | 评估 | 说明 |
|------|------|------|
| **代码成熟度** | ★★☆☆☆ (中等) | 代码活跃，Star 数可观，但缺少官方的 LTS 发行版，需自行锁定 commit 或 tag。 |
| **文档/示例** | ★★☆☆☆ | README 基本覆盖常用 API，示例代码有限，建议先阅读 `examples/` 目录并在本地跑通。 |
| **依赖安全** | ★★★☆☆ | 依赖主要是 Rust 标准库和少量网络/async crates，需使用 `cargo audit` 检查安全漏洞。 |
| **社区支持** | ★★☆☆☆ | 有一定的 Issue 活动，响应速度一般，适合内部使用或原型开发。 |
| **部署成本** | ★★★★☆ | 只需在 Rust 环境中 `cargo build`，二进制体积小，易于容器化部署。 |
| **总体生产适配度** | **中等** | 适合作为 **原型、内部工作流或非关键业务** 的 DICOM 处理层。若计划用于高可用、监管严格的临床系统，建议在正式投入前：<br>1. 固定依赖版本（使用 `Cargo.lock` 或 Git tag）。<br>2. 完成安全审计与性能基准测试。<br>3. 编写包装层，隐藏库的内部实现细节，以便后期替换。 |

**结论**  
dicom‑rs 为 Rust 项目提供了一个相对完整且性能优秀的 DICOM 实现，适合快速构建医学影像处理原型或内部服务。生产环境使用时，需要对依赖进行锁定、进行安全审计，并通过小规模 PoC 验证与现有 PACS 系统的兼容性后再逐步推广。

## 🧭 Practical evaluation

**Value:** Enet4/dicom-rs may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 546 GitHub stars
- 120 forks
- updated 2026-06-26
- primary language: Rust
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 58/100 |
| topics | 63/100 |
| outlook | 53/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 57/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/Enet4/dicom-rs) · [← Back to Misc](./README.md)</sub>
