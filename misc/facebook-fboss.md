# facebook/fboss

[![Stars](https://img.shields.io/github/stars/facebook/fboss?style=flat-square&color=yellow)](https://github.com/facebook/fboss/stargazers) [![Forks](https://img.shields.io/github/forks/facebook/fboss?style=flat-square&color=blue)](https://github.com/facebook/fboss/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-43%2F100-brightgreen?style=flat-square)](#)

> Facebook Open Switching System  Software for controlling network switches.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 967 |
| 🍴 **Forks** | 385 |
| 💻 **Language** | C++ |
| 📈 **Score** | 43/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
facebook/fboss is an open‑source software stack that provides control plane and data‑plane functionality for Facebook’s high‑performance network switches. Written mainly in C++, the project offers a modular, programmable interface for configuring ASICs, managing links, and collecting telemetry. With a solid community footprint (≈ 967 stars, 385 forks) and recent updates, it can serve as a foundation for custom switching solutions or research prototypes.

**Value**  
- **Deep switch control**: Exposes low‑level ASIC primitives and high‑level abstractions, enabling fine‑grained traffic steering, QoS, and telemetry that are difficult to achieve with generic SDN controllers.  
- **Extensible architecture**: Plug‑in support for different hardware platforms and a well‑documented API make it adaptable to bespoke networking hardware or lab‑grade testbeds.  
- **Open‑source transparency**: All code, issue tracking, and CI pipelines are public, allowing teams to audit security, contribute fixes, and align the stack with internal policies.

**Practical Adoption Path**  
1. **Initial Feasibility** – Clone the repo, build the C++ components on a supported Linux distribution, and run the provided unit‑test suite to verify the baseline build.  
2. **Hardware Matching** – Identify whether the target switch ASIC (e.g., Broadcom, Intel, or custom Facebook ASIC) is already supported; if not, use the existing hardware abstraction layer as a template to add the necessary drivers.  
3. **Integration Prototype** – Deploy fboss on a small set of test switches, connect it to your orchestration system (e.g., Ansible, Kubernetes‑based CNI), and validate basic functions such as port enable/disable, VLAN provisioning, and telemetry collection.  
4. **Feedback Loop** – Iterate on missing features or bugs, contributing patches upstream to reduce maintenance overhead.  
5. **Scale‑out** – Once the prototype meets functional and performance criteria, roll out the stack across the production fleet, establishing CI/CD pipelines for continuous delivery and monitoring.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑05‑13) and widely used internally at Facebook, but its documentation and integration guides are sparse for external users.  
- **Risk Factors**: Integration effort can be high because hardware‑specific adapters may need custom development; dependency management (Boost, Folly, gflags, etc.) must be vetted for compatibility with your environment.  
- **Recommended Use**: Suitable for internal prototypes, research labs, or organizations willing to invest in a dedicated networking team to handle build, driver adaptation, and ongoing maintenance. With proper validation and a clear ownership model, fboss can be hardened for production, but it is not a drop‑in solution for turnkey deployments.

### Русский

**Краткое резюме:**  
`facebook/fboss` — это открытая система управления сетевыми коммутаторами, написанная на C++ и поддерживаемая Facebook; её активная разработка (967 звёзд, 385 форков, последний коммит 2026‑05‑13) делает её подходящей для прототипов и внутренних проектов, где требуется гибкая настройка коммутируемой инфраструктуры. Типичный сценарий внедрения — интеграция в кастомные сетевые решения с последующей проверкой совместимости и затрат на настройку, поскольку из метаданных проекта сложно вывести готовый путь интеграции. Уровень готовности к production — средний: проект достаточно зрелый для экспериментального использования, но перед выводом в продакшн требуется тщательная проверка зависимостей, стабильности и процессов поддержки.

### 中文

**项目简介**  
facebook/fboss（Facebook Open Switching System）是 Facebook 开源的网络交换机控制软件，使用 C++ 编写，提供对硬件交换芯片的统一管理、转发表下发、监控与诊断等功能。

**价值**  
- **统一抽象层**：通过统一的 API 把不同厂商的 ASIC（如 Broadcom、Mellanox 等）封装成一致的控制接口，降低多平台运维成本。  
- **高性能与可扩展**：基于 C++ 的高效实现，适合大规模数据中心的低时延转发需求。  
- **活跃社区**：拥有近千颗星、数百个 Fork，近期仍在维护，能够获取社区的 bug 修复和新特性。

**典型接入方式**  
1. **源码编译**：克隆仓库后按照官方 README 安装依赖（Boost、gflags、protobuf 等），在目标交换机的 Linux 环境中交叉编译。  
2. **硬件适配**：在 `fboss/platform` 目录下选择对应 ASIC 的平台实现或自行实现 `Platform` 接口，以适配自研或商用交换芯片。  
3. **控制平面接入**：通过 Thrift/gRPC 暴露的控制 API 与上层 SDN 控制器或自研调度系统对接，完成路由、ACL、QoS 等下发。  
4. **监控/运维**：利用内置的 Prometheus 导出指标和日志收集，结合现有监控体系实现可观测性。

**生产可用性**  
- **成熟度**：项目已在 Facebook 内部大规模部署多年，代码质量较高，社区仍在活跃维护。  
- **适配成本**：需要对目标 ASIC 完成平台适配并进行充分的功能验证，集成路径不够透明，建议在原型或内部测试环境先行评估。  
- **运维要求**：依赖特定的构建工具链和运行时库，升级时需关注 API 兼容性和底层硬件驱动的同步。  

综上，fboss 适合作为原型或内部网络自动化平台的基础设施，具备向生产环境迁移的潜力，但在正式上线前应完成硬件适配、功能验证以及运维流程的完整评估。

## 🧭 Practical evaluation

**Value:** facebook/fboss may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 967 GitHub stars
- 385 forks
- updated 2026-05-13
- primary language: C++

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 65/100 |
| stars | 64/100 |
| topics | 0/100 |
| outlook | 41/100 |
| quality | 49/100 |
| recency | 20/100 |
| adoption | 64/100 |
| production | 44/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/facebook/fboss) · [← Back to Misc](./README.md)</sub>
