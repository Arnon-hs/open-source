# jonhoo/rust-ibverbs

[![Stars](https://img.shields.io/github/stars/jonhoo/rust-ibverbs?style=flat-square&color=yellow)](https://github.com/jonhoo/rust-ibverbs/stargazers) [![Forks](https://img.shields.io/github/forks/jonhoo/rust-ibverbs?style=flat-square&color=blue)](https://github.com/jonhoo/rust-ibverbs/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> Bindings for RDMA ibverbs through rdma-core

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 215 |
| 🍴 **Forks** | 58 |
| 💻 **Language** | Rust |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Libraries & SDKs

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`jonhoo/rust-ibverbs` provides Rust bindings for the RDMA ibverbs API via the `rdma‑core` library, enabling low‑latency, zero‑copy networking directly from Rust code. With 215 stars and recent activity (last commit 2026‑06‑24), it is a mature community project but its integration documentation is sparse, so a quick proof‑of‑concept is advisable before deeper adoption.

**Value**  
- Lets Rust applications tap into high‑performance RDMA hardware without writing C wrappers, preserving Rust’s safety guarantees while exposing the full ibverbs feature set.  
- Accelerates development of storage, database, or HPC services that require microsecond‑scale messaging or bulk data transfers.

**Practical Adoption Path**  
1. **Environment Setup** – Install the `rdma‑core` development packages (libibverbs, librdmacm) on the target hosts and verify that the NICs support RDMA.  
2. **Prototype** – Add `rust-ibverbs` as a Cargo dependency, compile a minimal “hello‑RDMA” program to open a device, create a protection domain, and perform a simple send/receive.  
3. **Integration Review** – Examine the crate’s `examples/` and the upstream `rdma‑core` docs to map required verbs (e.g., QP creation, CQ polling) to your application’s workflow.  
4. **Testing & CI** – Add unit and integration tests that run on RDMA‑enabled nodes; use Docker or Vagrant with SR‑IOV/NVMe‑over‑Fabric to automate validation.  
5. **Maintenance Plan** – Pin the crate version, monitor upstream `rdma‑core` releases, and schedule periodic rebuilds to capture security patches.

**Production Readiness**  
- **Maturity:** Medium. The library is stable enough for prototypes and internal services, but the lack of extensive integration guides means you’ll need to invest time in understanding ibverbs semantics.  
- **Risk Mitigation:** Conduct a pilot on a staging cluster, verify error handling and resource cleanup, and ensure you have a fallback path (e.g., TCP) if RDMA is unavailable.  
- **Operational Concerns:** Track the `rdma‑core` dependency for security updates, and allocate ownership for maintaining the native bindings as the Rust ecosystem evolves.  

Overall, `rust-ibverbs` is a solid building block for high‑performance Rust networking, provided you allocate resources for initial validation and ongoing native‑library maintenance.

### Русский

**rust‑ibverbs** — это набор Rust‑обёрток над библиотекой rdma‑core, позволяющий использовать RDMA‑операции через ibverbs напрямую из кода на Rust. Подходит для прототипов и внутренних сервисов, где требуется низкоуровневый доступ к сетевому ускорителю (например, реализация высокопроизводительных распределённых хранищ или RPC‑систем); перед вводом в продакшн рекомендуется проверить совместимость с текущей версией rdma‑core и оценить нагрузку на поддержку зависимостей. При достаточном тестировании проект считается готовым к ограниченному production‑использованию, но требует ручной проверки интеграции.

### 中文

**项目简介**  
`jonhoo/rust-ibverbs` 为 Rust 提供了对 RDMA **ibverbs** 接口的绑定，底层使用 `rdma-core` 实现。它让开发者能够在 Rust 程序中直接调用高性能的 RDMA 原语，适用于需要低延迟、零拷贝网络传输的场景。

**价值**  
- **高性能网络**：利用 RDMA 的硬件直通特性，显著降低网络延迟和 CPU 负载。  
- **Rust 生态**：提供安全的 FFI 包装，保持 Rust 的所有权模型和错误处理机制，降低使用 C 库的风险。  
- **原型与内部工具**：对需要快速验证 RDMA 思路的原型或内部服务尤为便利。

**典型接入方式**  
1. **依赖声明**：在 `Cargo.toml` 中加入  
   ```toml
   [dependencies]
   ibverbs = { git = "https://github.com/jonhoo/rust-ibverbs.git" }
   ```  
2. **环境准备**：确保宿主机已安装 `rdma-core`（包括 `libibverbs`、`libmlx5` 等），并且网络设备支持 RDMA。  
3. **代码使用**：通过库提供的 `ibv_*` 类型创建 `Context`、`ProtectionDomain`、`QueuePair` 等对象，随后调用 `post_send`、`post_recv` 等方法完成数据传输。  
4. **编译链接**：Cargo 会自动链接系统的 `libibverbs`，如有缺失需手动安装对应的系统包（如 `apt install libibverbs-dev`）。

**生产可用性**  
- **成熟度**：项目已有 215 ★、58 Fork，最近一次提交在 2026‑06‑24，活跃度尚可。  
- **适用场景**：适合内部原型、性能基准测试或对 RDMA 有明确需求的服务。  
- **风险与准备**：  
  - 文档和示例较少，接入前需自行验证 API 与业务流程的匹配度。  
  - 依赖 `rdma-core`，部署时需保证底层驱动、固件与硬件兼容。  
  - 维护频率不如大型社区库，生产环境建议锁定特定 commit 并加入内部 CI 进行回归测试。  

总体而言，`rust-ibverbs` 在原型阶段或对 RDMA 有明确需求的内部项目中价值突出；在正式生产环境使用前，需要进行充分的集成测试和运维准备。

## 🧭 Practical evaluation

**Value:** jonhoo/rust-ibverbs may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 215 GitHub stars
- 58 forks
- updated 2026-06-24
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 50/100 |
| topics | 0/100 |
| outlook | 58/100 |
| quality | 57/100 |
| recency | 80/100 |
| adoption | 48/100 |
| production | 61/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/jonhoo/rust-ibverbs) · [← Back to Libraries--sdks](./README.md)</sub>
