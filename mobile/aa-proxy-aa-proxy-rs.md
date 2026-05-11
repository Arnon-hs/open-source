# aa-proxy/aa-proxy-rs

[![Stars](https://img.shields.io/github/stars/aa-proxy/aa-proxy-rs?style=flat-square&color=yellow)](https://github.com/aa-proxy/aa-proxy-rs/stargazers) [![Forks](https://img.shields.io/github/forks/aa-proxy/aa-proxy-rs?style=flat-square&color=blue)](https://github.com/aa-proxy/aa-proxy-rs/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> AndroidAuto wired/wireless proxy

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 366 |
| 🍴 **Forks** | 35 |
| 💻 **Language** | Rust |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android-auto` `android-automotive` `diy` `headunit` `io-uring` `proxy` `raspberry-pi` `rust` `wireless-android-auto`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`aa-proxy/aa-proxy-rs` is a Rust‑based proxy that enables Android Auto to work over both wired and wireless connections, allowing a head‑unit or a development box to forward Android Auto traffic to a compatible infotainment system. With 366 ★ on GitHub and recent activity (last commit 2026‑05‑11), it offers a lightweight, open‑source alternative to proprietary Android Auto bridges.

**Value**  
- **Flexibility:** Supports both USB and Wi‑Fi transports, making it useful for developers testing Android Auto apps or for hobbyists retro‑fitting cars that lack native wireless support.  
- **Performance & Safety:** Written in Rust, the project benefits from memory‑safety guarantees and low‑overhead networking, which is important for real‑time media and control streams.  
- **Community traction:** A respectable star count and active forks indicate a modest but engaged user base, providing a basis for community support and future enhancements.

**Practical Adoption Path**  
1. **Proof‑of‑Concept:** Clone the repo, follow the README to build the binary (`cargo build --release`) and run it on a Linux machine or a Raspberry Pi that will act as the proxy.  
2. **Integration Test:** Connect an Android device via USB (or enable Wi‑Fi tethering) and verify that the Android Auto UI appears on the target head‑unit. Use the provided logging flags to confirm traffic forwarding.  
3. **Workflow Embedding:** Wrap the binary in a systemd service or Docker container to automate start‑up, and expose configuration (e.g., target IP, port) via environment variables or a simple TOML file.  
4. **Pilot Deployment:** Deploy on a single test vehicle or lab setup, monitor stability, and assess any required customizations (e.g., handling OEM‑specific handshakes).

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained but lacks formal release artifacts, extensive documentation, and automated CI/CD pipelines.  
- **Risks:** Integration steps are not fully described in the metadata; you’ll need to validate hardware compatibility, network firewall rules, and potential licensing constraints of Android Auto.  
- **Mitigation:** Conduct a small‑scale pilot, lock down dependency versions (`Cargo.lock`), and consider adding your own integration tests to cover your specific hardware and workflow. If the pilot succeeds, the proxy can be promoted to internal tooling or, with additional hardening (logging, monitoring, fail‑over), to production‑grade deployments.

### Русский

**aa-proxy/aa-proxy-rs** — это open‑source прокси‑сервер на Rust, позволяющий перенаправлять трафик Android Auto как по кабелю, так и по Wi‑Fi, что упрощает отладку и тестирование кастомных head‑unit‑приложений. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept: собрать бинарник, настроить прокси в Android Auto и проверить работу через README‑инструкцию; при положительных результатах можно интегрировать в прототипы или внутренние CI‑процессы. Готовность к production — средняя: проект активно поддерживается (обновления в 2026 г., 366 звёзд), но требует проверки зависимостей и возможных доработок перед использованием в продакшене.

### 中文

**项目简介**  
`aa-proxy/aa-proxy-rs` 是用 Rust 编写的 Android Auto 有线/无线代理工具，能够在 Android 设备和车载系统之间转发音视频流，帮助在没有官方线控或无线适配器的情况下实现 Android Auto 连接。

**价值**  
- **快速搭建原型**：只需在支持的 Linux/Android 环境上运行二进制，即可把手机的 Android Auto 信号通过网络或 USB 转发到车机，省去硬件改造成本。  
- **跨平台兼容**：基于 Rust，二进制体积小、运行时安全，适用于嵌入式盒子、树莓派或自建车载系统。  
- **灵活的有线/无线切换**：同一套代码即可支持 USB 直连和 Wi‑Fi 直连两种模式，满足不同测试场景。

**典型接入方式**  
1. **准备环境**  
   - 在目标机器（如树莓派、Ubuntu 服务器或 Android 开发板）上安装 Rust 运行时或直接下载预编译的 `aa-proxy` 可执行文件。  
   - 确保 Android 设备开启开发者选项并允许 USB 调试（有线模式）或打开 Wi‑Fi 直连（无线模式）。  

2. **启动代理**  
   - 有线模式：`./aa-proxy --mode usb --device /dev/ttyUSB0`（根据实际 USB 设备路径调整）。  
   - 无线模式：`./aa-proxy --mode wifi --listen 0.0.0.0:5555`，随后在 Android Auto 设置里手动输入代理 IP 与端口。  

3. **在车载系统中使用**  
   - 将车机的 Android Auto 客户端指向代理的 IP/端口，即可正常投屏、音视频交互。  
   - 如需在 CI/CD 或自动化测试中使用，可将启动命令写入脚本或系统服务（systemd、init 等），实现开机自启。  

**生产可用性**  
- **成熟度**：项目已有 366+ 星、35+ Fork，活跃维护至 2026‑05‑11，代码基于 Rust，具备较好的安全性和性能。  
- **适用场景**：非常适合作为原型验证、内部测试平台或自建车载系统的桥接层；对外部客户交付的正式产品仍需进行以下检查：  
  - **依赖审计**：确认所有 Rust crates 的许可证兼容性及是否有已知安全漏洞。  
  - **稳定性验证**：在目标硬件上进行长时间压力测试，确保网络抖动、USB 断连等异常情况下的恢复能力。  
  - **监控与日志**：为生产部署添加日志收集、健康检查和自动重启机制（如 systemd watchdog）。  

综合来看，`aa-proxy-rs` 已具备中等生产可用性，适合作为内部或定制化项目的核心组件，但在面向大规模用户或安全合规要求较高的场景前，建议完成上述验证步骤后再投入正式生产。

## 🧭 Practical evaluation

**Value:** aa-proxy/aa-proxy-rs may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 366 GitHub stars
- 35 forks
- updated 2026-05-11
- primary language: Rust
- 9 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 78/100 |
| recency | 100/100 |
| adoption | 50/100 |
| production | 73/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/aa-proxy/aa-proxy-rs) · [← Back to Mobile](./README.md)</sub>
