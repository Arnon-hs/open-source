# facebook/hhvm

[![Stars](https://img.shields.io/github/stars/facebook/hhvm?style=flat-square&color=yellow)](https://github.com/facebook/hhvm/stargazers) [![Forks](https://img.shields.io/github/forks/facebook/hhvm?style=flat-square&color=blue)](https://github.com/facebook/hhvm/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> A virtual machine for executing programs written in Hack.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 18.6k |
| 🍴 **Forks** | 3.1k |
| 💻 **Language** | C++ |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`hack` `hacklang` `hhvm` `php`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
Facebook’s HHVM is an open‑source virtual machine that runs programs written in the Hack language (a PHP dialect) and can also execute PHP code. It offers just‑in‑time compilation and a JIT engine that dramatically improve runtime performance for web workloads. With a large community (≈18 k stars, 3 k forks) and active maintenance, HHVM is a mature candidate for projects that need a high‑performance Hack/PHP execution environment.

**Value**  
HHVM delivers substantial speed gains (often 2‑10× faster than standard PHP interpreters) and provides built‑in tools for type checking, profiling, and debugging of Hack code. For teams already using Hack or looking to migrate legacy PHP applications to a more performant stack, HHVM offers a drop‑in runtime that can reduce server costs and improve latency without rewriting business logic.

**Practical adoption path**  

1. **Proof‑of‑concept** – Clone the repo, follow the README to build the VM, and run a small existing Hack or PHP service inside HHVM to verify compatibility.  
2. **Integration checklist** – Confirm that required extensions (e.g., APC, MySQL) are supported, and test the CI pipeline with HHVM‑specific build flags.  
3. **Pilot deployment** – Deploy the service to a staging environment using Docker images provided by the project, monitor performance metrics, and compare against the current interpreter.  
4. **Gradual rollout** – If the pilot succeeds, incrementally replace PHP‑FPM instances with HHVM across services, updating deployment scripts and observability hooks as needed.

**Production readiness**  
HHVM scores high on production readiness: it is actively maintained (last update 2026‑06‑24), widely adopted in Facebook’s own infrastructure, and has a robust ecosystem of extensions and community support. The primary risk is the integration effort—metadata does not expose a turnkey setup, so teams should allocate time to validate build dependencies, containerization, and any custom extensions before committing to a full migration. With a careful PoC and staged rollout, HHVM can be safely used in production for performance‑critical Hack/PHP workloads.

### Русский

HHVM — это высокопроизводительная виртуальная машина от Facebook, позволяющая исполнять программы, написанные на языке Hack, и использовать JIT‑компиляцию для ускорения веб‑приложений. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept, проверка README и совместимости с текущим стеком, а затем масштабирование до production‑окружения после оценки стоимости интеграции. По метрикам активности, популярности (18636 звёзд, 3069 форков) и поддержке сообщества проект готов к серьёзным пилотным запускам.

### 中文

**项目简介**  
facebook/hhvm 是 Facebook 开源的 Hack 语言运行时（HipHop Virtual Machine），用 C++ 实现的高性能虚拟机，能够将 Hack 代码即时编译为机器码并执行。

**价值**  
- **性能提升**：通过 JIT 编译，HHVM 在多数 Web 工作负载下比传统 PHP 解释器快 2‑3 倍，显著降低响应时间和服务器资源消耗。  
- **生态兼容**：兼容大部分 PHP 代码，同时提供 Hack 语言的类型系统和异步特性，帮助团队在保持现有代码的同时逐步迁移到更安全、更高效的 Hack。  
- **成熟社区**：拥有 18k+ 星、3k+ Fork，活跃的维护者和企业级使用案例（如 Facebook、Shopify），可为生产环境提供可靠的支持。

**典型接入方式**  
1. **准备环境**：在目标机器上安装依赖（CMake、Boost、jemalloc 等），或直接使用官方提供的 Docker 镜像 `hhvm/hhvm`.  
2. **代码迁移**：将现有的 PHP 项目拷贝到 HHVM 容器/服务器，修改入口文件（如 `index.php`）的 shebang 为 `#!/usr/bin/env hhvm`，或在 Nginx/Apache 中将 `fastcgi_pass` 指向 HHVM 的 FastCGI 监听端口。  
3. **配置优化**：通过 `hhvm.server.*`、`hhvm.repo.*` 等配置项调优 JIT 缓存、代码存储库（repo‑authoritative）和内存限制，以匹配业务的并发和响应需求。  
4. **验证与回滚**：先在预生产或灰度环境跑一套自动化测试，确认兼容性后逐步切流；如出现兼容问题，可通过 `hhvm.server.allow_hhas` 等开关回退到 PHP 模式。

**生产可用性**  
- **成熟度**：项目仍在活跃维护（截至 2026‑06‑24 最近一次提交），并已在多家大规模互联网公司投入生产，具备高可用性和安全补丁响应能力。  
- **部署经验**：官方提供的 Docker 镜像、官方文档以及社区案例足以支撑从小型服务到千兆流量的全链路部署。  
- **风险与建议**：虽然核心功能稳定，但某些第三方 PHP 扩展在 HHVM 上可能不兼容，建议在正式上线前完成完整的兼容性测试，并准备好回滚到标准 PHP-FPM 的方案。  

综上，HHVM 具备显著的性能优势和成熟的生态，适合作为高并发 Web 应用的后端运行时；典型的接入流程是通过容器或 FastCGI 替换现有 PHP 环境，经过充分的灰度验证后即可在生产环境安全使用。

## 🧭 Practical evaluation

**Value:** facebook/hhvm may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 18636 GitHub stars
- 3069 forks
- updated 2026-06-24
- primary language: C++
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 87/100 |
| stars | 91/100 |
| topics | 50/100 |
| outlook | 60/100 |
| quality | 73/100 |
| recency | 40/100 |
| adoption | 90/100 |
| production | 57/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/facebook/hhvm) · [← Back to Misc](./README.md)</sub>
