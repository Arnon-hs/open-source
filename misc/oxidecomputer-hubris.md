# oxidecomputer/hubris

[![Stars](https://img.shields.io/github/stars/oxidecomputer/hubris?style=flat-square&color=yellow)](https://github.com/oxidecomputer/hubris/stargazers) [![Forks](https://img.shields.io/github/forks/oxidecomputer/hubris?style=flat-square&color=blue)](https://github.com/oxidecomputer/hubris/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> A lightweight, memory-protected, message-passing kernel for deeply embedded systems.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.5k |
| 🍴 **Forks** | 233 |
| 💻 **Language** | Rust |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
Hubris (oxidecomputer/hubris) is a lightweight, memory‑protected, message‑passing kernel written in Rust for deeply embedded systems. It offers strong isolation between tasks while keeping the runtime footprint small enough for resource‑constrained microcontrollers. With a solid community signal (3.5 k stars, 233 forks) and recent activity, it can serve as a solid foundation for prototype firmware or internal tooling.

**Value**  
Hubris provides a modern, Rust‑based alternative to traditional bare‑metal kernels, giving developers built‑in safety guarantees (memory protection, type‑checked message passing) without the overhead of a full RTOS. This can accelerate development cycles, reduce hard‑to‑debug memory bugs, and make it easier to reason about inter‑task communication in safety‑critical or low‑power devices.

**Practical adoption path**  
1. **Evaluate the README and examples** – clone the repo, build the example boards, and run the provided unit tests to confirm the toolchain works on your target MCU.  
2. **Prototype a minimal task** – replace an existing bare‑metal loop with a Hubris task that sends/receives a simple message; this validates the integration steps (cargo‑xtensa, linker scripts, flash tool).  
3. **Port existing drivers** – adapt your peripheral drivers to Hubris’s driver model and message‑passing API, using the `hubris` crate as a dependency in your Cargo.toml.  
4. **Run integration tests** – verify timing, memory usage, and fault isolation on your hardware; adjust the kernel configuration (e.g., stack sizes, protection regions) as needed.  

Because the integration documentation is sparse, a manual code review and a small proof‑of‑concept are essential before committing to larger projects.

**Production readiness**  
The project sits at a medium readiness level: it is actively maintained (last update 2026‑06‑26) and has a healthy community, making it suitable for prototypes, internal tools, or products where the team can afford the upfront effort to validate the integration. For production use, ensure you:

* Audit the kernel version and any third‑party crates for security patches.  
* Confirm that the memory‑protection hardware on your MCU is fully supported.  
* Establish a maintenance plan for updating Hubris and its dependencies.  

With these checks in place, Hubris can be a reliable core for embedded firmware, but it is not a drop‑in solution for mission‑critical deployments without thorough validation.

### Русский

**Hubris** — это лёгкое, защищённое от переполнения памяти ядро с механизмом обмена сообщениями, написанное на Rust и ориентированное на глубоко встраиваемые системы. Оно подходит для прототипов и внутренних проектов, где требуется надёжное изоляция задач и минимальный оверхед, однако перед внедрением необходимо вручную оценить процесс интеграции и зависимости, так как готовых инструкций мало. Уровень готовности к production — средний: ядро стабильно развивается (обновления до 2026‑06‑26, 3548 звёзд), но требует проверки на совместимость и поддержки в конкретном workflow.

### 中文

**项目简介**  
Hubris（oxidecomputer/hubris）是一款面向深度嵌入式系统的轻量级内核，采用 Rust 编写，提供内存保护和基于消息传递的任务调度，适合资源受限的 MCU 环境。

**价值**  
- **安全性**：Rust 的零成本抽象和所有权模型天然防止缓冲区溢出、空指针等常见漏洞；内核本身再加入了内存保护（MPU）支持。  
- **实时性**：基于消息传递的调度模型简洁明确，能够在毫秒甚至微秒级别实现确定性响应。  
- **可移植性**：核心代码与平台无关，只需为目标 MCU 实现少量 HAL，即可在 Cortex‑M、RISC‑V 等多种架构上运行。  

**典型接入方式**  
1. **克隆仓库并选择目标平台**：`git clone https://github.com/oxidecomputer/hubris.git`，在 `hubris/targets/` 目录下挑选或自定义对应 MCU 的 target 配置。  
2. **实现硬件抽象层（HAL）**：按照 `hubris-hal` 规范提供 UART、GPIO、I2C、SPI、MPU 等外设的驱动实现，通常只需几百行 Rust 代码。  
3. **定义任务（Task）**：在 `src/tasks/` 中编写 Rust 模块，每个任务通过 `hubris::msg::Message` 与其他任务通信，使用 `#[task]` 宏注册。  
4. **编译并烧录**：使用 `cargo xbuild --target <target>.json` 生成二进制，配合 OpenOCD、JLink 或其他调试器写入 MCU。  
5. **集成测试**：利用 Hubris 自带的模拟器或在真实硬件上运行单元/集成测试，确保消息流和内存保护如预期工作。

**生产可用性**  
- **成熟度**：项目已有 3500+ 星、200+ fork，活跃维护至 2026‑06‑26，社区贡献相对活跃。  
- **适用场景**：非常适合原型验证、内部工具、工业控制或安全敏感的嵌入式产品；在对实时性和内存安全要求高、但资源受限的环境下表现出色。  
- **上线前检查**：  
  - **依赖审计**：确认所有 Rust crate 均已审计并符合公司合规要求。  
  - **平台适配**：验证目标 MCU 的 MPU、时钟和外设是否已完整实现 HAL。  
  - **维护成本**：评估团队对 Rust 与 Hubris 调度模型的熟悉度，必要时安排培训或保留内部维护人员。  
- **风险**：集成文档相对简略，需自行探索 HAL 接口和任务注册细节；缺乏商业级的长期支持渠道，生产环境应做好内部维护和安全审计。  

综上，Hubris 在需要高安全性、低开销的深度嵌入式项目中具有明确价值，接入流程清晰但需要一定的手动适配工作；在完成依赖审计和平台适配后，可作为原型或内部生产系统的可靠内核使用。

## 🧭 Practical evaluation

**Value:** oxidecomputer/hubris may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 3548 GitHub stars
- 233 forks
- updated 2026-06-26
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 76/100 |
| topics | 0/100 |
| outlook | 64/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 71/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/oxidecomputer/hubris) · [← Back to Misc](./README.md)</sub>
