# facebook/folly

[![Stars](https://img.shields.io/github/stars/facebook/folly?style=flat-square&color=yellow)](https://github.com/facebook/folly/stargazers) [![Forks](https://img.shields.io/github/forks/facebook/folly?style=flat-square&color=blue)](https://github.com/facebook/folly/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> An open-source C++ library developed and used at Facebook.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 30.4k |
| 🍴 **Forks** | 5.9k |
| 💻 **Language** | C++ |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Folly (Facebook Open‑Source Library) is a high‑performance C++ library that provides a wide range of reusable components—such as smart pointers, concurrent data structures, memory allocators, and networking utilities—originally built for Facebook’s own infrastructure. With over 30 k stars, active maintenance (last update 2026‑06‑30) and extensive internal adoption, it is a mature, production‑ready code base that can accelerate development of performance‑critical services.  

**Value**  
Folly supplies battle‑tested building blocks that would otherwise need to be written from scratch, saving engineering time and reducing bugs in low‑level systems (e.g., thread‑pools, futures, serialization, and high‑throughput I/O). Its tight focus on speed, memory efficiency, and modern C++ idioms makes it especially valuable for services where latency and throughput are paramount.  

**Practical Adoption Path**  

1. **Initial feasibility check** – Clone the repository and run the provided CMake/Make build on a sandbox to verify that the library compiles with your compiler version and target platform.  
2. **Feature scoping** – Identify the specific Folly modules you need (e.g., `folly::Future`, `folly::AtomicHashMap`). The README and source‑level documentation give usage examples; for missing details, consult the inline Doxygen comments or Facebook’s internal tutorials that are publicly mirrored.  
3. **Integration shim** – Add Folly as a submodule or fetch it via a package manager (e.g., vcpkg or Conan) to keep it version‑controlled alongside your code. Wrap the required headers in a thin abstraction layer to isolate your code from potential API changes.  
4. **Testing & validation** – Write unit tests that exercise the Folly components under your workload, paying particular attention to ABI compatibility and exception safety. Run the library’s own test suite to confirm that the build is healthy on your CI environment.  
5. **Gradual rollout** – Deploy the updated service to a staging environment, monitor latency, memory usage, and any runtime warnings. If the results are positive, promote the change to production.  

**Production Readiness**  
Folly scores high on production readiness: it has a large, active community, frequent commits, and is already used in Facebook’s critical services. The repository’s health metrics (30 k stars, 5.8 k forks, recent updates) indicate strong ecosystem support. The main risk lies in the integration effort—metadata provides limited guidance on build configuration and dependency management—so a careful validation step is essential before committing to a full rollout. Once the integration shim is in place and the needed modules are vetted, Folly can be treated as a stable, high‑performance foundation for C++ services in production.

### Русский

Резюме проекта facebook/folly:

facebook/folly - это открытое C++-библиотека, разрабатываемая и используемая в Facebook. Этот проект может быть полезен для конкретных рабочих процессов, если его README и активность соответствуют конкретной цели. facebook/folly готов к производственному использованию (Production readiness: High) и может быть использован в серьезных проектах, но требует тщательного инспектирования и валидации перед внедрением из-за неочевидной интеграционной практики.

### 中文

**Folly 简介**

Folly 是 Facebook 开发和使用的开源 C++ 库。它提供了一系列常用函数和数据结构，用于提高 C++ 代码的性能和可维护性。

**价值**

Folly 的价值在于它提供了一个开源的 C++ 库，能够帮助开发者提高代码的性能和可维护性。它的使用场景包括但不限于：

* 高性能计算
* 大规模数据处理
* 网络通信
* 数据结构和算法

**典型接入方式**

由于 Folly 的 README 文档和活动信息不够详细，因此需要手动检查和测试才能确定适合的接入方式。一般来说，Folly 可以通过以下方式接入：

* 将 Folly 的源代码直接包含在项目中
* 使用 CMake 或其他构建工具来编译和链接 Folly 库
* 使用 Folly 的 API 来调用其提供的函数和数据结构

**生产可用性**

Folly 的生产可用性非常高。它的 GitHub 星数超过 30,000，更新频率高，广泛被采用和使用。因此，Folly 是一个

## 🧭 Practical evaluation

**Value:** facebook/folly may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 30440 GitHub stars
- 5860 forks
- updated 2026-06-30
- primary language: C++

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 94/100 |
| stars | 95/100 |
| topics | 0/100 |
| outlook | 56/100 |
| quality | 68/100 |
| recency | 40/100 |
| adoption | 95/100 |
| production | 55/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/facebook/folly) · [← Back to Misc](./README.md)</sub>
