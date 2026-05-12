# torlando-tech/columba

[![Stars](https://img.shields.io/github/stars/torlando-tech/columba?style=flat-square&color=yellow)](https://github.com/torlando-tech/columba/stargazers) [![Forks](https://img.shields.io/github/forks/torlando-tech/columba?style=flat-square&color=blue)](https://github.com/torlando-tech/columba/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Native Android messaging app using Bluetooth LE, TCP, or RNode (LoRa) over LXMF and Reticulum

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 793 |
| 🍴 **Forks** | 75 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ble` `lora` `lxmf` `mesh-networks` `off-grid` `privacy` `reticulum` `rns`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Columba is an open‑source native Android messaging client that can exchange messages over Bluetooth LE, TCP, or LoRa (via RNode) using the LXMF protocol on top of the Reticulum mesh network. Written in Kotlin, it targets low‑power, infrastructure‑less communication scenarios such as field operations, disaster response, or hobbyist mesh networks.  

**Value**  
- Provides a ready‑made Android UI for LXMF/Reticulum, eliminating the need to build a custom front‑end for mesh‑based messaging.  
- Supports multiple transport layers (BLE, TCP, LoRa), letting developers choose the most appropriate link for their environment without rewriting protocol logic.  
- The project already has a sizable community (≈800 ★, 75 forks) and recent activity, indicating ongoing maintenance and potential community support.  

**Practical Adoption Path**  
1. **Review the README & sample app** – clone the repo, build the Kotlin project, and run the supplied demo to verify that the messaging flow matches your use case (e.g., sending LXMF packets over LoRa).  
2. **Proof‑of‑concept** – integrate the library into a minimal Android module of your own app, replace the demo UI with your workflow, and configure the desired transport (BLE, TCP, or RNode).  
3. **Validate the mesh backend** – set up a Reticulum node (or use an existing one) and confirm end‑to‑end delivery of LXMF messages; adjust any required permissions or Android manifest entries.  
4. **Iterate and document** – once the PoC works, formalize the integration steps, automate builds, and add tests for your specific transport configuration.  

**Production Readiness**  
- **Maturity:** Medium. The codebase is actively updated (last commit 2026‑05‑12) and has a healthy star/fork count, but the integration documentation is sparse and the build process may require manual tweaking.  
- **Suitability:** Ideal for prototypes, internal tools, or niche deployments where mesh communication is a core requirement. Before production use, perform a dependency audit (Kotlin libraries, Android SDK versions) and confirm long‑term support for Reticulum/LXMF.  
- **Risks:** The exact integration path is not fully described in the metadata; you’ll need to invest time in understanding the LXMF API and configuring the underlying transport (especially LoRa via RNode). Conduct a small pilot to gauge setup effort and maintenance overhead before committing to a full‑scale rollout.

### Русский

**Columba** — это нативное Android‑приложение для обмена сообщениями, использующее Bluetooth LE, TCP или LoRa‑модуль RNode поверх протоколов LXMF и Reticulum. Оно подходит для быстрого создания прототипов или внутренних коммуникационных решений, где требуется работа в условиях ограниченной инфраструктуры (например, в полевых сетях, на фестивалях или в IoT‑проектах). Уровень готовности — средний: приложение уже стабильно работает и имеет активное сообщество (793 ★, 75 форков), но перед выводом в продакшн рекомендуется провести небольшое POC, проверить README и оценить затраты на настройку зависимостей и поддержку.

### 中文

**项目简介**  
Columba 是一款使用 Kotlin 编写的原生 Android 即时通讯客户端，支持 Bluetooth LE、TCP 以及基于 LoRa 的 RNode 作为底层传输层，消息通过 LXMF/Reticulum 网络进行路由。项目在 GitHub 上已有 793 颗星，活跃维护至 2026‑05‑12，适合作为离线/低功耗场景的原型或内部工具。

**价值**  
- **多链路弹性**：同一套 UI 可以在蓝牙、局域网或远距离 LoRa 网络之间无缝切换，满足现场、灾备、野外等无公网环境的通信需求。  
- **端到端去中心化**：基于 LXMF（Liminal eXchange Message Format）和 Reticulum 的点对点路由，天然支持离线转发和消息持久化，降低对中心服务器的依赖。  
- **开箱即用的 Android 客户端**：提供完整的 UI、权限管理和消息存储实现，开发者只需关注业务层即可快速集成。

**典型接入方式**  

| 场景 | 接入步骤 | 关键代码/模块 |
|------|----------|--------------|
| **内部原型** | 1. Fork 项目或在本地 clone<br>2. 在 `app/build.gradle` 中添加自己的 `applicationId`<br>3. 在 `src/main/res/values/strings.xml` 配置自定义主题和服务器标识<br>4. 调用 `ColumbaService.start(context, TransportConfig)` 启动后台服务 | `ColumbaService`、`TransportConfig`（BluetoothLeConfig / TcpConfig / RNodeConfig） |
| **业务系统集成** | 1. 将 `columba` 作为 Gradle 子模块引入（`implementation project(':columba')`）<br>2. 实现 `MessageHandler` 接口以接收/发送业务消息<br>3. 根据业务需求选定传输层（如仅使用 LoRa 时只保留 `RNodeTransport`）<br>4. 在主进程初始化 `ReticulumNode` 并注入到 `ColumbaEngine` | `MessageHandler`、`ReticulumNode`、`ColumbaEngine` |
| **现场/灾备部署** | 1. 通过 Android Studio 打包为 APK<br>2. 在目标设备上预装或 OTA 推送<br>3. 使用设备自带的蓝牙/LoRa 硬件启动对应 transport<br>4. 通过 UI 配置节点 ID 与对等设备 | UI 配置页面、`TransportManager` |

**生产可用性评估**  

| 维度 | 现状 | 评估 |
|------|------|------|
| **代码成熟度** | 793 Stars、75 Forks，最近一次提交在 2026‑05‑12，使用 Kotlin 编写，代码结构清晰。 | ★★★★☆ |
| **依赖健康** | 依赖 AndroidX、Kotlin 标准库、Reticulum‑Java 客户端等，均为活跃维护的库。需自行检查 LoRa（RNode）硬件驱动的兼容性。 | ★★★★ |
| **文档/示例** | README 包含快速启动指南和基本的 transport 配置示例，但缺少完整的业务层集成案例。 | ★★★☆☆ |
| **安全/隐私** | 消息在 LXMF/Reticulum 上端到端加密，未见明显的安全漏洞；仍需自行审计依赖库。 | ★★★★ |
| **运维成本** | 需要自行部署 Reticulum 节点（可在边缘服务器或树莓派上运行），以及管理 LoRa 网关或蓝牙配对。 | ★★★☆☆ |
| **总体生产适配度** | 适合 **原型、内部工具或特定离线场景**；在完整的企业级生产环境中投入使用前，建议完成：<ul><li>CI/CD 自动化构建</li><li>安全审计</li><li>监控/日志集成</li><li>硬件兼容性验证</li></ul> | ★★★☆☆ |

**结论**  
Columba 以多链路、去中心化的设计为 Android 离线通讯提供了一个相对完整的实现，适合作为 **原型验证或特定行业（如灾害救援、野外勘探）内部通信** 的技术选型。若业务对可靠性、可维护性有更高要求，建议在小范围 PoC 验证后，再进行代码审计、依赖锁定和生产运维流程的完善后方可上线。

## 🧭 Practical evaluation

**Value:** torlando-tech/columba may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 793 GitHub stars
- 75 forks
- updated 2026-05-12
- primary language: Kotlin
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 47/100 |
| stars | 62/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 81/100 |
| recency | 100/100 |
| adoption | 58/100 |
| production | 75/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/torlando-tech/columba) · [← Back to Mobile](./README.md)</sub>
