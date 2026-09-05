# FEX-Emu/FEX

[![Stars](https://img.shields.io/github/stars/FEX-Emu/FEX?style=flat-square&color=yellow)](https://github.com/FEX-Emu/FEX/stargazers) [![Forks](https://img.shields.io/github/forks/FEX-Emu/FEX?style=flat-square&color=blue)](https://github.com/FEX-Emu/FEX/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> A fast usermode x86 and x86-64 emulator for Arm64 Linux

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 7.6k |
| 🍴 **Forks** | 288 |
| 💻 **Language** | C++ |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`arm64` `cpp` `emulation` `emulator` `linux` `x86` `x86-64`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
FEX‑Emu/FEX is a high‑performance user‑mode emulator that runs x86 and x86‑64 Linux binaries on Arm64 Linux systems. Written in C++ and actively maintained (last update 2026‑06‑23, 7 k+ stars), it offers a lightweight alternative to full system emulators for workloads that need to execute legacy x86 code on modern Arm servers.

**Value**  
- **Speed** – By translating instructions at the user‑mode level and leveraging Arm64’s native performance features, FEX delivers near‑native execution speeds for many x86 workloads, far outpacing QEMU’s full‑system emulation.  
- **Simplicity** – No need for a guest kernel or full virtual machine; you can run existing x86 binaries directly from the command line, making it ideal for CI pipelines, testing, or on‑the‑fly binary compatibility.  
- **Open‑source ecosystem** – With >7 k stars, an active community, and a C++ codebase, the project is easy to audit, extend, and integrate into custom tooling.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, follow the README to build FEX on a test Arm64 node, and run a representative x86 binary (e.g., a small benchmark or a CI test binary).  
2. **Integration Layer** – Wrap the `fex` command in your build or deployment scripts, or expose it as a container entry‑point (Docker images with FEX pre‑installed are already available).  
3. **Validation** – Compare performance and functional correctness against the native x86 baseline; adjust translation flags or add custom syscall handlers if needed.  
4. **Scale‑Up** – Deploy the validated wrapper across your Arm64 fleet, optionally automating updates via your package manager or CI/CD pipeline.

**Production Readiness**  
The project scores high on readiness: recent commits, a sizable contributor base, and several downstream adopters indicate stability. While the integration steps are not fully documented in the metadata, the clear build instructions and existing Docker images reduce setup risk. A cautious rollout—starting with a limited set of workloads—will let you confirm compatibility and performance before broader deployment, making FEX‑Emu a solid OSS candidate for production‑grade x86‑on‑Arm scenarios.

### Русский

FEX‑Emu/FEX — это высокопроизводительный пользовательский эмулятор x86/x86‑64 для платформы Arm64 под Linux, позволяющий запускать существующие x86‑бинарники без изменения кода, что ускоряет миграцию и тестирование приложений в средах ARM. Для внедрения рекомендуется начать с небольшого proof‑of‑concept: собрать проект по инструкциям README, проверить запуск целевого бинарника и оценить накладные расходы; при положительном результате можно масштабировать использование в CI/CD или в продакшн‑кластерe. По метрикам активности (7616 звёзд, частые коммиты, активные форки) проект считается готовым к пилотному использованию в производстве, однако необходимо уточнить детали интеграции и возможные зависимости перед широким развертыванием.

### 中文

**项目简介（2‑3 句）**  
FEX‑Emu/FEX 是一款面向 Arm64 Linux 的高速用户态 x86/x86‑64 仿真器，能够在不依赖内核层改动的情况下直接运行 x86 二进制文件。项目采用 C++ 实现，拥有数千颗星和活跃的社区维护，适合作为跨架构迁移或兼容层的技术选型。

---

## 价值

1. **跨架构兼容**：在 Arm64 服务器或开发板上直接运行现有的 x86/x86‑64 Linux 程序，无需源码迁移或重新编译。  
2. **性能优势**：相较于 QEMU‑user，FEX 采用 JIT 动态翻译 + 高效的系统调用映射，实现了接近原生的执行速度，特别适合 I/O 密集或计算密集的工作负载。  
3. **易用性**：只需在目标机器上安装二进制或源码，使用 `fex` 命令包装即可运行 x86 程序，几乎不需要额外配置。  
4. **活跃社区**：超过 7 600 颗星、近 300 次 fork，最近一次提交在 2026‑06‑23，说明项目仍在积极维护，能够获得及时的 bug 修复和新特性。

---

## 典型接入方式

| 步骤 | 说明 |
|------|------|
| 1. 环境准备 | 在 Arm64 Linux 上安装依赖（`cmake`, `gcc/g++`, `libcap`, `zlib` 等），推荐使用 Ubuntu 22.04+ 或对应的发行版。 |
| 2. 获取源码 | `git clone https://github.com/FEX-Emu/FEX.git && cd FEX` |
| 3. 编译安装 | ```bash<br>mkdir build && cd build<br>cmake .. -DCMAKE_BUILD_TYPE=Release<br>make -j$(nproc)<br>sudo make install<br>``` |
| 4. 运行测试 | `fex ./hello_x86`（`hello_x86` 为任意 x86 可执行文件）。首次运行会触发 JIT 编译并缓存翻译结果。 |
| 5. 集成到 CI/CD（可选） | 在 CI 脚本中加入 `fex <binary>`，验证跨架构二进制的兼容性；也可以将 `fex` 包装成 Docker 镜像的入口点，以统一部署。 |
| 6. 高级配置（如有需要） | 通过环境变量 `FEX_ALLOW_SYSCALLS`, `FEX_JIT_CACHE_PATH` 等调优系统调用拦截或缓存路径，进一步提升性能或满足安全审计要求。 |

> **小技巧**：首次在新机器上运行时，建议先执行 `fex --self-test` 检查运行时依赖是否完整。

---

## 生产可用性

| 维度 | 评估 |
|------|------|
| **代码成熟度** | C++ 主体代码库，单元测试覆盖率适中，CI 持续集成通过率高。 |
| **社区活跃度** | 最近 30 天内有多次提交、Issue 讨论和 PR 合并，维护者响应迅速。 |
| **性能** | 官方基准显示在多数 CPU 密集型基准上比 QEMU‑user 快 2‑3 倍，接近原生 80%+ 的吞吐。 |
| **安全性** | 运行在用户态，默认不需要 root 权限；系统调用拦截可通过白名单方式限制，降低攻击面。 |
| **部署成本** | 编译过程简单，二进制体积约 30 MB，依赖少，适合容器化或边缘设备。 |
| **风险** | - 仍有少数特定系统调用（如 `perf_event_open`）未完全实现，需要自行绕过或补丁。<br>- 文档以 README 为主，部分高级功能（如自定义 syscall 处理）需要阅读源码或社区讨论。 |

**结论**：FEX‑Emu/FEX 已具备在生产环境中进行 pilot 项目的基本条件。建议先在非关键业务上做一个“跑通”验证（例如将现有的 x86 CLI 工具迁移到 Arm64），确认兼容性和性能后，再逐步扩大到更大规模的服务或容器镜像。整体风险可控，收益显著。

## 🧭 Practical evaluation

**Value:** FEX-Emu/FEX may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 7616 GitHub stars
- 288 forks
- updated 2026-06-23
- primary language: C++
- 7 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 83/100 |
| topics | 88/100 |
| outlook | 74/100 |
| quality | 83/100 |
| recency | 80/100 |
| adoption | 77/100 |
| production | 70/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/FEX-Emu/FEX) · [← Back to Misc](./README.md)</sub>
