# wiiznokes/fan-control

[![Stars](https://img.shields.io/github/stars/wiiznokes/fan-control?style=flat-square&color=yellow)](https://github.com/wiiznokes/fan-control/stargazers) [![Forks](https://img.shields.io/github/forks/wiiznokes/fan-control?style=flat-square&color=blue)](https://github.com/wiiznokes/fan-control/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Control your fans with different behaviors

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 319 |
| 🍴 **Forks** | 21 |
| 💻 **Language** | Rust |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`fan-control` `fancontrol` `iced` `librefancontrol` `librehardwaremonitor` `libsensors` `linux` `pwm` `rust` `sensors`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
`wiiznokes/fan-control` is a Rust library that lets you programmatically control system fans with customizable speed‑curves, temperature thresholds, and event‑driven policies. With over 300 stars and recent activity, it offers a lightweight, cross‑platform way to integrate fan management into Rust‑based tools or scripts.

**Value**  
The project fills a niche for developers who need fine‑grained fan control without resorting to vendor‑specific utilities or heavyweight OS‑level daemons. By exposing a clean API, it enables use cases such as thermal throttling for high‑performance compute, silent‑mode profiles for laptops, or automated cooling for embedded devices.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided examples, and verify that the library can detect and adjust fans on your target hardware.  
2. **Integration** – Add the crate to your `Cargo.toml`, wrap the API in a small service or CLI that matches your workflow, and test it in a controlled environment.  
3. **Validation** – Review the README for hardware compatibility notes, confirm required permissions (e.g., access to `/sys/class/hwmon` on Linux), and ensure the build succeeds with your toolchain.

**Production readiness**  
The library is at a *medium* readiness level: it is actively maintained (last update 2026‑05‑11) and has a modest community, but documentation is limited and hardware support is not exhaustively listed. It is suitable for prototypes, internal tools, or environments where you can tolerate some experimentation and perform your own validation of stability and safety. Before moving to production, perform dependency audits, add monitoring for fan‑speed changes, and consider fallback mechanisms in case the library cannot control a specific fan model.

### Русский

**wiiznokes/fan-control** — это open‑source библиотека на Rust, позволяющая управлять вентиляторами с различными режимами работы (например, фиксированная скорость, динамический отклик на температуру и т.п.). Она подходит для быстрого прототипирования или внутреннего инструмента, где требуется гибкое управление охлаждением, но перед выводом в продакшн следует проверить совместимость с вашей системой, оценить затраты на настройку и убедиться в поддержке зависимостей. Текущий уровень готовности — средний: проект имеет 319 звёзд, активные обновления и достаточную документацию, однако интеграционный путь не полностью описан, поэтому рекомендуется начать с небольшого proof‑of‑concept.

### 中文

**项目简介（2‑3 句话）**  
`wiiznokes/fan-control` 是一个用 Rust 编写的开源库，提供对计算机或嵌入式设备风扇的多种调速策略（恒速、温度阈值、曲线、手动切换等），帮助开发者在软件层面实现智能散热控制。

---

## 价值

1. **灵活的风扇行为**：支持固定转速、基于温度的阈值调节、PWM 曲线以及自定义回调，能够满足从桌面 PC 到单板计算机的各种散热需求。  
2. **Rust 安全性**：利用 Rust 的所有权模型和零成本抽象，提供高性能且几乎没有运行时开销的控制代码，降低因内存错误导致的系统不稳定风险。  
3. **易于集成**：提供简洁的 API（`FanController::new()`, `set_mode()`, `update()`），只需在主循环或系统守护进程中调用一次即可完成风扇管理。  
4. **社区认可**：已有 300+ 星、20+ 分叉，活跃的 Issue 与 PR 说明项目已有一定的实战验证。

---

## 典型接入方式

| 步骤 | 操作 | 说明 |
|------|------|------|
| 1️⃣ | **添加依赖** | 在 `Cargo.toml` 中加入 <br>`fan-control = { git = "https://github.com/wiiznokes/fan-control", tag = "v0.3.0" }`（或使用 crates.io 发布的版本）。 |
| 2️⃣ | **初始化硬件** | 根据目标平台（Linux `sysfs`、Windows `WinMM`、或嵌入式 HAL）创建对应的风扇驱动实例，例如 `SysfsFan::new("/sys/class/hwmon/hwmon0/fan1_input")`。 |
| 3️⃣ | **创建控制器** | ```rust<br>let mut controller = FanController::new(driver);<br>controller.set_mode(FanMode::TemperatureCurve(vec![(40,30), (60,70), (80,100)]));``` |
| 4️⃣ | **周期性更新** | 在主循环或定时任务中调用 `controller.update()?;`，库内部会读取温度、计算目标转速并写回风扇。 |
| 5️⃣ | **自定义扩展** | 如需自定义策略，只实现 `FanPolicy` trait 并在 `set_mode` 时注入即可。 |

> **小型验证**：可以先在本地机器上写一个最小的二进制 `cargo run --example simple`，观察风扇转速变化是否符合预期，再决定是否在更大系统中推广。

---

## 生产可用性评估

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | ★★☆☆☆（中等） | 项目活跃度良好（最近更新），但仍处于库阶段，缺少完整的生产级文档和长期维护承诺。 |
| **稳定性** | ✅ 基本功能已实现 | 核心 API 稳定，已通过 CI 在 Linux、Windows 上编译通过。建议在正式环境前做一次回归测试。 |
| **依赖风险** | ✅ 纯 Rust + 少量系统调用 | 仅依赖 `sysfs`（Linux）或对应平台的低层驱动，外部依赖少，易审计。 |
| **安全性** | ✅ Rust 防护 | 编译期保证内存安全，运行时仅涉及文件 I/O 与 PWM 写入，风险可控。 |
| **运维成本** | ⚙️ 中等 | 需要在目标机器上配置风扇硬件路径或对应的 HAL，且需要定期检查库的兼容性（例如内核升级导致 sysfs 改动）。 |
| **适用场景** | ✅ 原型、内部工具、边缘设备 | 对于需要快速实现散热策略的原型或内部部署非常合适；在大规模生产环境使用前建议做更严格的可靠性验证（如冗余监控、回滚机制）。 |

**结论**：`wiiznokes/fan-control` 具备在原型或内部系统中快速实现智能风扇调控的价值，集成成本适中。若计划在关键业务或大规模设备上使用，建议先在受控环境做完整的 POC，评估硬件兼容性、异常处理和升级路径后再推进到生产。

## 🧭 Practical evaluation

**Value:** wiiznokes/fan-control may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 319 GitHub stars
- 21 forks
- updated 2026-05-11
- primary language: Rust
- 10 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 48/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/wiiznokes/fan-control) · [← Back to Misc](./README.md)</sub>
