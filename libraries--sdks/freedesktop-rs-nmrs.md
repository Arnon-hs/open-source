# freedesktop-rs/nmrs

[![Stars](https://img.shields.io/github/stars/freedesktop-rs/nmrs?style=flat-square&color=yellow)](https://github.com/freedesktop-rs/nmrs/stargazers) [![Forks](https://img.shields.io/github/forks/freedesktop-rs/nmrs?style=flat-square&color=blue)](https://github.com/freedesktop-rs/nmrs/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> Rust bindings for NetworkManager over D-Bus.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 288 |
| 🍴 **Forks** | 29 |
| 💻 **Language** | Rust |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dbus` `linux` `networkmanager` `rust`

## 🎯 Categories

Libraries & SDKs

## 📝 Summary

### English

**Brief summary**  
`freedesktop-rs/nmrs` provides Rust bindings that wrap NetworkManager’s D‑Bus API, letting Rust applications manage network connections, devices, and VPNs without dealing directly with low‑level D‑Bus calls. The crate is actively maintained (last update 2026‑07‑12), has a modest community (≈ 288 ★, 29 forks), and targets developers who need programmatic control over NetworkManager from Rust code.

**Value**  
The library abstracts the verbose D‑Bus interface into idiomatic Rust types and async‑ready methods, dramatically reducing boilerplate for any tool or service that must create, monitor, or modify network configurations on Linux desktops or servers. It enables rapid prototyping of network‑aware applications (e.g., connection managers, automated VPN switches, or container‑orchestrated networking) while staying within the Rust ecosystem’s safety guarantees.

**Practical adoption path**  

1. **Read the README & examples** – verify that the crate covers the specific NetworkManager calls you need (e.g., `AddConnection`, `ActivateConnection`).  
2. **Create a small proof‑of‑concept** – write a tiny async binary that lists current connections or brings up a known Wi‑Fi network, using the crate’s `NetworkManagerProxy`.  
3. **Validate the D‑Bus environment** – ensure the target machines run NetworkManager and expose the standard D‑Bus service (`org.freedesktop.NetworkManager`).  
4. **Add as a dependency** – pin the version you tested, run `cargo test` and `cargo clippy` to catch any API changes or lint issues.  
5. **Integrate into your workflow** – replace existing shell‑script or Python D‑Bus calls with the Rust wrapper, adding error handling and logging as needed.

**Production readiness**  
The project sits at a medium readiness level: it is stable enough for prototypes and internal tools, but you should perform a few checks before deploying to production:

* **Dependency health** – confirm the crate’s transitive dependencies are actively maintained and have compatible licenses.  
* **API stability** – the crate follows semantic versioning, but review the changelog for any breaking changes since the last release.  
* **Runtime environment** – test on all target Linux distributions to ensure the D‑Bus service name and object paths match.  
* **Maintenance plan** – consider forking or vendorizing if you need long‑term support beyond the upstream activity.

If these steps pass, `nmrs` can be safely used in production for internal services; for critical, customer‑facing products, add a fallback (e.g., invoking `nmcli`) and monitor upstream updates.

### Русский

**freedesktop-rs/nmrs** — это набор Rust‑биндингов к NetworkManager через D‑Bus, позволяющий управлять сетевыми интерфейсами, профилями и соединениями прямо из кода. Типичный сценарий внедрения — написать небольшой proof‑of‑concept, проверив README и пример использования, а затем интегрировать библиотеку в прототипы или внутренние сервисы, где требуется динамическое управление сетью. Готовность к production — средняя: проект имеет активное развитие (обновление 2026‑07‑12, 288 звёзд), но перед выводом в продакшн следует оценить зависимости, стабильность API и план поддержки.

### 中文

**项目简介**  
`freedesktop-rs/nmrs` 为 Rust 提供了基于 D‑Bus 的 NetworkManager 绑定，使得在 Rust 应用中能够直接调用 NetworkManager 的管理接口（如连接、设备、状态监控等），从而实现网络配置的自动化和实时监控。

**价值**  
- **Rust 原生体验**：无需手写 D‑Bus 消息或使用 FFI，直接使用安全、类型化的 Rust API。  
- **跨平台网络管理**：利用 NetworkManager 的统一抽象，可在 Linux 桌面、服务器以及容器环境中统一管理网络。  
- **加速原型开发**：在需要动态网络配置（如 Wi‑Fi 扫描、VPN 启动、热点创建）的工具或服务时，提供即插即用的库。

**典型接入方式**  
1. **添加依赖**：在 `Cargo.toml` 中加入  
   ```toml
   nmrs = "0.1"
   ```  
2. **初始化 D‑Bus 连接**（推荐使用 async‑runtime）  
   ```rust
   use nmrs::NetworkManager;
   use zbus::Connection;

   #[tokio::main]
   async fn main() -> zbus::Result<()> {
       let conn = Connection::system().await?;
       let nm = NetworkManager::new(&conn).await?;
       // 读取当前激活的连接
       let active = nm.active_connections().await?;
       println!("Active connections: {:?}", active);
       Ok(())
   }
   ```  
3. **调用业务接口**：如创建 Wi‑Fi 连接、监控设备状态、设置 VPN 等，全部通过 `NetworkManager` 提供的方法完成。  
4. **事件订阅**：使用 D‑Bus 信号（`PropertiesChanged`、`StateChanged` 等）实现实时网络状态回调，适合构建监控或自恢复逻辑。

**生产可用性**  
- **成熟度**：项目已有 288 ★、29 🍴，最近一次提交在 2026‑07‑12，活跃度尚可。代码基于 `zbus`（成熟的 Rust D‑Bus 实现），API 已覆盖常用的 NetworkManager 功能。  
- **适用场景**：非常适合作为内部工具、原型或中小规模服务的网络管理层。对外部生产系统使用时，需要：  
  1. **依赖审计**：确认 `zbus`、`glib` 等底层库的安全更新策略。  
  2. **错误处理**：NetworkManager 的 D‑Bus 接口在网络异常时会返回各种错误码，建议在业务层统一包装并实现重试/回退。  
  3. **兼容性测试**：不同 Linux 发行版的 NetworkManager 版本可能存在细微差异，建议在目标环境做一次完整的功能回归。  
- **风险**：项目文档主要在 README，缺少完整的使用案例；集成路径需要自行探索 D‑Bus 信号的订阅方式。建议先在测试环境实现一个“列出所有连接并监控状态变化”的小 demo，验证集成成本后再决定是否投入生产。

综上，`freedesktop-rs/nmrs` 为 Rust 项目提供了便捷的 NetworkManager 接口，适合快速构建网络管理功能的原型或内部服务。经过充分的依赖审查和小规模验证后，可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** freedesktop-rs/nmrs may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 288 GitHub stars
- 29 forks
- updated 2026-07-12
- primary language: Rust
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 52/100 |
| topics | 50/100 |
| outlook | 63/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 48/100 |
| production | 64/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/freedesktop-rs/nmrs) · [← Back to Libraries--sdks](./README.md)</sub>
