# ofiwg/libfabric

[![Stars](https://img.shields.io/github/stars/ofiwg/libfabric?style=flat-square&color=yellow)](https://github.com/ofiwg/libfabric/stargazers) [![Forks](https://img.shields.io/github/forks/ofiwg/libfabric?style=flat-square&color=blue)](https://github.com/ofiwg/libfabric/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-46%2F100-brightgreen?style=flat-square)](#)

> Open Fabric Interfaces

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 804 |
| 🍴 **Forks** | 508 |
| 💻 **Language** | C |
| 📈 **Score** | 46/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
`ofiwg/libfabric` is an open‑source C library that implements the Open Fabric Interfaces (OFI) specification, providing a low‑level, high‑performance networking API for building scalable, RDMA‑capable applications. With over 800 stars and active maintenance as of June 2026, it is a solid foundation for projects that need direct control over fabric resources, but the integration details are not fully described in the repository metadata.

**Value**  
- **Performance‑oriented API** – Exposes verbs‑like primitives (queues, endpoints, memory registration) that let developers exploit high‑throughput, low‑latency fabrics (InfiniBand, RoCE, Ethernet, etc.) without locking into a vendor‑specific SDK.  
- **Portability** – By conforming to the OFI standard, the same code can run on multiple fabrics and providers, easing migration and multi‑fabric deployments.  
- **Community and Ecosystem** – A sizable user base, regular commits, and a well‑documented README make it a credible choice for research prototypes and internal services that need custom networking stacks.

**Practical Adoption Path**  
1. **Evaluate Fit** – Review the README, provider list, and existing examples to confirm that the target fabric (e.g., libfabric’s verbs, sockets, or gni provider) is supported.  
2. **Prototype** – Pull the library, compile the examples, and run a minimal “hello‑world” client/server on a test node to verify basic connectivity and performance.  
3. **Integrate** – Wrap the libfabric calls behind an internal abstraction layer (e.g., a C++ or Go wrapper) so future provider changes are isolated.  
4. **Automate Build & Tests** – Add libfabric as a dependency in your CI pipeline, ensuring the required provider libraries (e.g., `libibverbs`, `rdmacm`) are installed on build agents.  
5. **Security & Ops Review** – Check licensing (BSD‑3‑Clause), audit any required kernel modules, and confirm that the runtime environment (e.g., NIC drivers, firmware) meets the provider’s prerequisites.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained and widely used in research and some production contexts, but the integration surface is low‑level and requires careful engineering.  
- **Risk**: The integration path is not fully documented in the repository metadata; you’ll need to spend time validating provider compatibility, handling error paths, and establishing monitoring for fabric health.  
- **Recommendation**: Suitable for prototypes, internal services, or workloads where you control the deployment environment and can afford the upfront effort to build a stable abstraction layer. For mission‑critical production systems, perform a thorough dependency audit, add extensive test coverage, and consider a fallback networking stack in case a provider issue arises.

### Русский

Библиотека **ofiwg/libfabric** предоставляет открытый набор API для высокопроизводительных сетевых коммуникаций (RDMA, Ethernet, InfiniBand) и часто используется в системах распределённых вычислений и HPC‑приложениях. Она подходит для прототипов и внутренних сервисов, где требуется гибкая интеграция сетевых стеков, однако из‑за скудной документации и малоочевидных точек входа рекомендуется провести ручную проверку совместимости и оценить затраты на настройку перед выводом в продакшн. При достаточном тестировании проект считается готовым к использованию в средах со средним уровнем надёжности, при условии контроля зависимостей и регулярного обновления.

### 中文

**项目简介（2‑3 句）**  
ofiwg/libfabric 是由 OpenFabrics 互操作工作组维护的跨平台高性能网络通信库，提供统一的 Fabric 接口（API）以便在不同底层网络（如 InfiniBand、RoCE、Ethernet 等）上实现低延迟、零拷贝的数据传输。它被广泛用于 HPC、分布式存储和大规模机器学习等需要高吞吐、低时延网络的场景。

**价值**  
- **统一抽象层**：一次编写代码即可在多种硬件和网络协议之间切换，无需针对每种网络单独适配。  
- **高性能**：支持 RDMA、零拷贝、批量发送等特性，能够充分发挥现代高速互连的性能。  
- **生态兼容**：已有 MPI、OFI‑based RPC 框架（如 libfabric‑based UCX）以及分布式存储系统（Ceph、Margo）对其进行集成，降低二次开发成本。

**典型接入方式**  
1. **源码编译**：在目标机器上安装依赖（如 libibverbs、rdma-core），使用 CMake 配置 `-DENABLE_RDMA=ON` 等选项，然后 `make && make install`。  
2. **语言绑定**：通过官方提供的 C API，或使用社区维护的 Python（pyfabric）/ Go（go-libfabric）绑定，直接在业务代码中调用 `fi_*` 系列函数。  
3. **与上层框架集成**：在 MPI（如 Open MPI、MPICH）或 RPC 框架（如 UCX）中启用 `fabric` 传输层，只需在启动参数中指定 `FI_PROVIDER=...` 即可完成自动接入。

**生产可用性**  
- **成熟度**：拥有 800+ GitHub stars、500+ forks，活跃维护至 2026‑06‑25，代码基于 C，社区提供了完整的单元测试和 CI。  
- **适用阶段**：适合原型验证、内部研发以及对网络性能有严格要求的生产系统。  
- **风险与注意点**：元数据中未提供完整的集成指南，实际接入前需评估目标硬件的 FI Provider 支持情况、依赖库版本兼容性以及运维团队的维护能力。确认这些后，libfabric 可在生产环境中稳定运行。

## 🧭 Practical evaluation

**Value:** ofiwg/libfabric may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 804 GitHub stars
- 508 forks
- updated 2026-06-25
- primary language: C

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 62/100 |
| topics | 0/100 |
| outlook | 48/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 63/100 |
| production | 50/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/ofiwg/libfabric) · [← Back to Misc](./README.md)</sub>
