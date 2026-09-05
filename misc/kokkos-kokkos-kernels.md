# kokkos/kokkos-kernels

[![Stars](https://img.shields.io/github/stars/kokkos/kokkos-kernels?style=flat-square&color=yellow)](https://github.com/kokkos/kokkos-kernels/stargazers) [![Forks](https://img.shields.io/github/forks/kokkos/kokkos-kernels?style=flat-square&color=blue)](https://github.com/kokkos/kokkos-kernels/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Kokkos C++ Performance Portability Programming Ecosystem: Math Kernels - Provides BLAS, Sparse BLAS and Graph Kernels

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 383 |
| 🍴 **Forks** | 117 |
| 💻 **Language** | C++ |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`blas` `hpsf` `kokkos` `linear-algebra` `performance-portability` `sparse-matrix`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Kokkos‑Kernels is the math‑kernel library of the Kokkos performance‑portability ecosystem, offering BLAS, Sparse‑BLAS and graph kernels that run efficiently on CPUs, GPUs and other accelerator architectures from a single C++ code base. It enables scientific‑computing teams to write high‑performance linear‑algebra and graph‑processing code once and have it scale across heterogeneous hardware without hand‑crafted, platform‑specific plumbing.

**Value Proposition**  
- **Performance portability** – The same source code compiles to optimized kernels on NVIDIA, AMD, Intel, and CPU‑only platforms, eliminating the need for separate vendor‑specific libraries.  
- **Rich mathematical primitives** – Ready‑to‑use dense, sparse, and graph operations accelerate prototype development and reduce the effort of implementing or tuning low‑level kernels.  
- **Open‑source and actively maintained** – With ~380 stars, regular commits (last update 2026‑05‑12) and a modest dependency footprint (pure C++ + Kokkos), it can be adopted without licensing concerns.

**Practical Adoption Path**  

| Step | Action | Goal |
|------|--------|------|
| 1️⃣ **Environment check** | Verify that your build environment can compile Kokkos (C++14+, CMake, supported compilers) and that the target hardware (CPU, CUDA, ROCm, SYCL) is listed in Kokkos‑Kernels’ CI matrix. | Ensure basic compile‑time compatibility. |
| 2️⃣ **Prototype a small PoC** | Clone the repo, run the provided examples (e.g., `example_spmv.cpp`) on a single node, and compare performance against a baseline BLAS library. | Validate that the library builds, runs, and delivers expected speedups. |
| 3️⃣ **Integrate via CMake** | Add `find_package(Kokkos REQUIRED)` and `find_package(KokkosKernels REQUIRED)` to your project’s CMakeLists, link against `${KokkosKernels_LIBRARIES}`. | Minimal, documented integration; no code changes required beyond linking. |
| 4️⃣ **Replace hot‑spot calls** | Swap existing dense/sparse calls (e.g., `cblas_dgemm`, `mkl_sparse_...`) with the equivalent Kokkos‑Kernels APIs (`KokkosBlas::gemm`, `KokkosSparse::spmv`). | Leverage portability while keeping algorithmic logic unchanged. |
| 5️⃣ **Continuous‑integration testing** | Add a CI job that builds the project with at least two back‑ends (e.g., Host + CUDA) to catch regressions early. | Guard against future portability breakage. |
| 6️⃣ **Production hardening** | Pin Kokkos/Kokkos‑Kernels versions, audit third‑party dependencies, and run performance regression suites on target clusters. | Stabilize the stack for long‑term use. |

**Production Readiness Assessment**  

| Dimension | Rating | Rationale |
|-----------|--------|-----------|
| **Stability** | **Medium** | The library is mature (several releases, active CI) but the API evolves; pinning a version is recommended. |
| **Performance** | **High** | Benchmarks show near‑native performance on all supported back‑ends; many scientific codes already rely on it. |
| **Ease of Integration** | **Low‑Medium** | Requires a functional Kokkos installation and CMake integration; documentation is decent but not exhaustive for every back‑end. |
| **Maintenance Overhead** | **Medium** | You must track both Kokkos and Kokkos‑Kernels releases and test against your hardware stack. |
| **Support & Community** | **Medium** | Active GitHub issues and a modest community; no formal commercial support, but many academic groups contribute. |

**Bottom Line** – Kokkos‑Kernels is a solid choice for teams that need high‑performance linear‑algebra or graph kernels across heterogeneous hardware and are comfortable managing a C++ build ecosystem. Start with a small proof‑of‑concept to confirm build and performance on your target platforms, then lock the versions and embed the library via CMake for broader adoption. With proper version pinning and CI testing, it can move from prototype to production for internal workflows and, eventually, for customer‑facing services.

### Русский

**kokkos/kokkos‑kernels** — открытая библиотека C++ для переносимого высокопроизводительного вычисления, предоставляющая реализации BLAS, Sparse BLAS и графовых ядер. Она позволяет командам ускорять операции над данными (матричные, разреженные и графовые) без написания собственного кода‑обёртки, что упрощает построение прототипов и внутренних сервисов, где важна быстрая обработка больших объёмов данных. Проект имеет средний уровень готовности к production: достаточное количество звёзд и форков, активные обновления, но требуется предварительная проверка зависимости и небольшого proof‑of‑concept для подтверждения простоты интеграции в существующий стек.

### 中文

**项目简介**  
Kokkos‑Kernels 是 Kokkos C++ 性能可移植编程生态系统中的数学内核库，提供 BLAS、稀疏 BLAS 与图算法实现，能够在 CPU、GPU 以及其他异构硬件上保持高效且一致的性能。

**价值**  
- **一次编写、跨平台运行**：基于 Kokkos 的抽象层，开发者只需编写一次代码，即可在不同硬件（如 x86、ARM、NVIDIA、AMD GPU）上获得接近原生优化的数值计算性能。  
- **丰富的数值基元**：提供完整的向量、矩阵、稀疏矩阵以及图遍历等核心算子，省去团队自行实现和维护 BLAS/SpBLAS 的工作量。  
- **加速科学与工程应用**：在求解线性系统、稀疏求解、图分析等场景中显著提升吞吐和并行效率，帮助项目更快进入原型和生产阶段。

**典型接入方式**  
1. **依赖管理**：在 CMake 项目中使用 `FetchContent` 或 `ExternalProject_Add` 拉取 `kokkos/kokkos-kernels`，并确保先行集成 Kokkos 本体（`kokkos/kokkos`）。  
   ```cmake
   FetchContent_Declare(
       kokkos
       GIT_REPOSITORY https://github.com/kokkos/kokkos.git
       GIT_TAG        master)
   FetchContent_MakeAvailable(kokkos)

   FetchContent_Declare(
       kokkos_kernels
       GIT_REPOSITORY https://github.com/kokkos/kokkos-kernels.git
       GIT_TAG        master)
   FetchContent_MakeAvailable(kokkos_kernels)
   ```
2. **编译选项**：根据目标硬件开启对应后端（`-DKokkos_ENABLE_OPENMP`, `-DKokkos_ENABLE_CUDA`, `-DKokkos_ENABLE_HIP` 等），并在链接时加入 `Kokkos::kokkos` 与 `KokkosKernels::kokkoskernels`。  
3. **代码使用**：通过 `Kokkos::View` 管理数据布局，调用 `KokkosKernels::Experimental::spmv`、`gemm`、`graph::graph_color` 等高层 API 完成计算。  
4. **验证步骤**：先在 README 中的示例程序跑通，确认编译链路与硬件后端正常，然后在项目中实现一个小的 PoC（比如稀疏矩阵向量乘），评估性能与集成成本。

**生产可用性**  
- **成熟度**：项目已有 383+ 星、117+ Fork，活跃维护至 2026‑05‑12，社区贡献和 issue 处理较为及时，属于中等成熟度库。  
- **适用场景**：非常适合作为原型开发、内部科研平台或需要高性能数值计算的服务（如 CFD、机器学习前处理、图分析）。  
- **生产注意事项**  
  - **依赖管理**：需要同步 Kokkos 与 Kokkos‑Kernels 的版本，避免 ABI 不匹配。  
  - **编译时间与二进制体积**：开启多后端会显著增加编译时间和库体积，建议在生产环境仅保留实际使用的后端。  
  - **持续维护**：定期跟进 upstream 更新，尤其是对新 GPU 架构的支持和安全补丁。  
  - **测试覆盖**：在 CI 中加入 Kokkos‑Kernels 的单元测试，确保不同硬件上的数值一致性。  

综上，Kokkos‑Kernels 为需要跨异构平台的高性能数值计算提供了即插即用的数学内核，接入成本主要集中在 Kokkos 环境的配置与 CMake 集成。经过一次小规模 PoC 验证后，可在内部项目或面向性能敏感的生产服务中安全使用。

## 🧭 Practical evaluation

**Value:** kokkos/kokkos-kernels helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 383 GitHub stars
- 117 forks
- updated 2026-05-12
- primary language: C++
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 55/100 |
| topics | 75/100 |
| outlook | 67/100 |
| quality | 71/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 66/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/kokkos/kokkos-kernels) · [← Back to Misc](./README.md)</sub>
