# ROCm/rocm-libraries

[![Stars](https://img.shields.io/github/stars/ROCm/rocm-libraries?style=flat-square&color=yellow)](https://github.com/ROCm/rocm-libraries/stargazers) [![Forks](https://img.shields.io/github/forks/ROCm/rocm-libraries?style=flat-square&color=blue)](https://github.com/ROCm/rocm-libraries/network) [![Language](https://img.shields.io/badge/lang-Assembly-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-41%2F100-brightgreen?style=flat-square)](#)

> super repo for rocm libraries

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 334 |
| 🍴 **Forks** | 287 |
| 💻 **Language** | Assembly |
| 📈 **Score** | 41/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
ROCm/rocm‑libraries is a “super‑repo” that aggregates the various ROCm (Radeon Open Compute) libraries into a single source tree, making it easier to locate, build, and version‑align the components needed for GPU‑accelerated workloads on AMD hardware. Although the repository is actively maintained (last commit 2026‑05‑14) and has a modest community presence (≈ 330 ★, 287 forks), its primary language is Assembly and the README provides only high‑level guidance, so concrete integration details are sparse.

**Value**  
- **Convenient source of truth**: All ROCm library code (e.g., hipBLAS, rocFFT, MIOpen) lives under one roof, simplifying dependency tracking and ensuring compatible versions across the stack.  
- **Open‑source transparency**: You can inspect the implementation, contribute fixes, or tailor builds for custom hardware or research prototypes.  
- **Community momentum**: The star/fork count indicates a non‑trivial user base, which can be a source of community support and bug reports.

**Practical Adoption Path**  
1. **Initial feasibility check** – Clone the repo and run the provided build scripts on a supported AMD GPU platform; verify that the required toolchain (ROCm compiler, CMake, etc.) is installed.  
2. **Select needed sub‑libraries** – Identify which ROCm components your workflow requires (e.g., hipBLAS for linear algebra). Use the `CMake` options to enable only those, reducing build time and binary size.  
3. **Integrate with your codebase** – Link against the produced static/shared libraries or use the `hip` headers directly. Adjust your CI pipeline to pull a specific tag/commit to guarantee reproducibility.  
4. **Validate** – Run the library’s own test suites and a small set of your own workloads to confirm functional correctness and performance expectations.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively updated and widely forked, but the lack of detailed integration documentation means you’ll need to invest time in manual verification.  
- **Risk**: The integration path is not explicit; you must confirm that the build environment, driver versions, and hardware match your production stack.  
- **Recommendation**: Suitable for prototypes, internal tooling, or workloads where you can afford a validation phase. Before committing to production, lock down a specific release tag, perform regression testing, and establish a maintenance plan for future ROCm updates.

### Русский

**ROCм/rocm‑libraries** — это «супер‑репозиторий» с открытым кодом, собирающий набор библиотек ROCm (GPU‑вычисления AMD). Он подходит для прототипов или внутренних пайплайнов, где требуется быстрый доступ к готовым ROCm‑компонентам; однако из‑за скудной документации и неочевидных инструкций по интеграции проект требует ручного аудита и проверки совместимости перед использованием в продакшене. В текущем состоянии готовность к production — средняя: возможна работа в тестовой среде, но необходимо оценить затраты на настройку и обслуживание.

### 中文

**项目简介**  
ROCm/rocm‑libraries 是 AMD ROCm 生态的超级仓库，统一收集并维护了 ROCm 相关的底层库（如 rocBLAS、hipFFT、MIOpen 等），为 GPU 加速提供统一的源码和二进制发布入口。

**价值**  
- **一站式获取**：无需在多个仓库之间切换，所有官方 ROCm 库都集中在此 repo，便于版本对齐和依赖管理。  
- **最新实现**：保持与上游 ROCm 同步，提供最新的性能优化和硬件特性支持。  
- **开源透明**：源码可直接审计，方便在内部进行二次裁剪或安全合规检查。

**典型接入方式**  
1. **源码编译**  
   ```bash
   git clone https://github.com/ROCm/rocm-libraries.git
   cd rocm-libraries
   ./install.sh   # 或者使用 CMake + make 手动编译
   ```  
   编译完成后，将生成的库路径（`/opt/rocm/lib` 等）加入 `LD_LIBRARY_PATH`，并在 CMake/Makefile 中使用 `find_package(hip)`、`find_package(rocblas)` 等。

2. **二进制包**  
   - 在支持的 Linux 发行版（Ubuntu、RHEL）上使用 AMD 官方的 apt/yum 源：  
     ```bash
     sudo apt-get install rocm-dev rocm-libs
     ```  
   - 通过 Docker 镜像 `rocm/dev-ubuntu-22.04` 直接获取预装好的库，适合 CI/CD 与容器化部署。

3. **Python/Conda 接口**（部分库提供）  
   ```bash
   conda install -c rocm rocm-blas rocm-fft
   ```

**生产可用性**  
- **成熟度**：已有 300+ 星、近 300 次 fork，社区活跃，且最近一次提交在 2026‑05‑14，表明仍在维护。  
- **适用场景**：适合原型开发、内部实验平台以及对 ROCm 硬件依赖明确的生产服务。  
- **风险与准备**：  
  - 集成路径较为手动，需要自行确认目标平台的 ROCm 驱动、LLVM/hip 版本匹配。  
  - 建议在上线前进行完整的兼容性测试（驱动、库版本、CI 流水线），并做好库的版本锁定与安全审计。  
- **总体评估**：在已确认 AMD GPU 环境的前提下，ROCm/rocm‑libraries 可作为 **中等风险** 的生产组件使用；对依赖管理和维护有一定把控能力的团队能够顺利将其纳入正式业务。

## 🧭 Practical evaluation

**Value:** ROCm/rocm-libraries may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 334 GitHub stars
- 287 forks
- updated 2026-05-14
- primary language: Assembly

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 54/100 |
| topics | 0/100 |
| outlook | 39/100 |
| quality | 45/100 |
| recency | 20/100 |
| adoption | 56/100 |
| production | 42/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/ROCm/rocm-libraries) · [← Back to Misc](./README.md)</sub>
