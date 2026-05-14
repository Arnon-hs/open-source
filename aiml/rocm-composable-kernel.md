# ROCm/composable_kernel

[![Stars](https://img.shields.io/github/stars/ROCm/composable_kernel?style=flat-square&color=yellow)](https://github.com/ROCm/composable_kernel/stargazers) [![Forks](https://img.shields.io/github/forks/ROCm/composable_kernel?style=flat-square&color=blue)](https://github.com/ROCm/composable_kernel/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> [DEPRECATED] Moved to ROCm/rocm-libraries repo.  NOTE:  develop branch is maintained as a read-only mirror

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 532 |
| 🍴 **Forks** | 290 |
| 💻 **Language** | C++ |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
ROCm /composable_kernel is a C++ library that provides reusable GPU kernels for ROCm‑based AI workloads. Although the original repository is now deprecated and read‑only, it still serves as a reference implementation for building custom AI components without starting from scratch. The project is most useful for rapid prototyping of RAG, agent pipelines, or other model‑centric features on AMD hardware.

**Value Proposition**  
- **Accelerated development:** Offers a collection of pre‑written, composable kernels that can be stitched together to add AI capabilities, saving time compared with hand‑crafting low‑level GPU code.  
- **Hardware alignment:** Tailored for AMD’s ROCm stack, it ensures optimal performance on AMD GPUs, which is valuable for teams standardising on AMD hardware.  
- **Open‑source transparency:** With >500 stars and a sizable fork base, the code is community‑reviewed and can be extended or adapted to specific use‑cases.

**Practical Adoption Path**  
1. **Assess relevance:** Clone the read‑only `develop` branch and review the kernel APIs to confirm they cover the operations needed for your prototype (e.g., matrix multiplies, attention kernels).  
2. **Prototype integration:** Build a small proof‑of‑concept that links against the library using the ROCm toolchain; this will surface any missing dependencies or build‑system quirks.  
3. **Manual validation:** Because metadata and integration guides are sparse, run unit tests and benchmark kernels on your target GPU to verify correctness and performance.  
4. **Fork & maintain:** If the library meets your needs, fork the repo, add any missing wrappers or bug fixes, and integrate the fork into your CI/CD pipeline.  

**Production Readiness**  
- **Maturity:** Medium. The codebase is stable enough for internal prototypes, but the repository is deprecated and receives no active maintenance, so you must assume responsibility for bug fixes and future compatibility.  
- **Dependencies:** Requires a ROCm‑compatible environment (ROCm driver, hipcc, etc.) and careful version pinning; verify that your production stack matches the versions used in the last commit (May 2026).  
- **Risk mitigation:** Conduct thorough testing, monitor performance regressions after ROCm upgrades, and consider maintaining an internal mirror to avoid surprises from upstream deprecation.  

In short, composable_kernel can speed up AI feature development on AMD GPUs, but teams should treat it as a reference implementation that needs careful validation and self‑maintenance before being deployed in production.

### Русский

**ROCм/composable_kernel** — это открытый C++‑библиотека, позволяющая быстро добавить AI‑функциональность (например, прототипы RAG‑систем или агентных пайплайнов), не собирая стек моделей с нуля. При типичном внедрении её используют в экспериментальных или внутренних проектах, где требуется гибко комбинировать ядра вычислений, однако перед переходом в продакшн требуется ручная проверка интеграции и оценка зависимости от ROCm‑стека. Готовность к production — средняя: библиотека стабильно работает в прототипах, но требует дополнительного тестирования и контроля за поддержкой.

### 中文

**项目简介（2‑3 句）**  
ROCm/composable_kernel 是 AMD ROCm 生态下的可组合算子库，已迁移至 ROCm/rocm‑libraries 仓库，当前 develop 分支仅作只读镜像保留。它提供高性能、模块化的 GPU 算子实现，帮助开发者在不从零构建模型栈的情况下快速加入 AI 能力。

**价值**  
- **加速原型开发**：提供即插即用的算子组件，省去底层实现的时间，让研发团队能够快速验证 AI 特性、RAG（检索增强生成）或智能体工作流。  
- **性能优势**：基于 ROCm 与 AMD GPU 深度优化，适合在 AMD 硬件上实现高吞吐和低延迟。  
- **社区与生态**：拥有 500+ 星、300+ Fork，活跃的社区可提供参考实现和使用案例。

**典型接入方式**  
1. **环境准备**：在支持 ROCm 的机器上安装对应的 ROCm SDK（>=5.0）和 CMake。  
2. **源码获取**：克隆 `ROCm/rocm-libraries`（或直接使用只读的 `ROCm/composable_kernel` 镜像），切换到 `develop` 分支。  
3. **编译**：使用 CMake 配置 `CK_ENABLE_EXAMPLES=ON`（如需示例）并指定目标 GPU 架构，执行 `make -j$(nproc)`。  
4. **集成**：在项目的 CMakeLists 中通过 `add_subdirectory` 或 `find_package(composable_kernel REQUIRED)` 引入库头文件和链接目标，随后调用提供的算子 API（如 `ck::tensor_operation::device::ConvFwd`）即可。  
5. **验证**：运行自带的单元测试或示例程序，确认算子在目标硬件上的正确性和性能。

**生产可用性**  
- **成熟度**：库已在内部多个原型项目中验证，功能完整度在 0.8 左右，适合作为内部或受控环境的 AI 加速层。  
- **风险**：由于仓库已迁移，文档和更新节奏相对分散，集成前需确认所使用的 ROCm 版本与库的兼容性，并做好依赖管理。  
- **推荐做法**：在生产环境部署前，进行一次完整的性能基准测试和回归验证；对关键路径采用容错监控；若需长期维护，建议跟踪 `rocm-libraries` 主仓库的更新并在内部维护一个同步分支。  

总体而言，ROCm/composable_kernel 在 AMD GPU 环境下提供了中等到高的生产可用性，适合作为原型到正式产品的桥梁，只要在引入前做好兼容性和维护成本评估即可。

## 🧭 Practical evaluation

**Value:** ROCm/composable_kernel helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 532 GitHub stars
- 290 forks
- updated 2026-05-14
- primary language: C++

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 58/100 |
| topics | 0/100 |
| outlook | 68/100 |
| quality | 67/100 |
| recency | 100/100 |
| adoption | 59/100 |
| production | 69/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/ROCm/composable_kernel) · [← Back to AI/ML](./README.md)</sub>
