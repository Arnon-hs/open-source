# guardianproject/orbot-android

[![Stars](https://img.shields.io/github/stars/guardianproject/orbot-android?style=flat-square&color=yellow)](https://github.com/guardianproject/orbot-android/stargazers) [![Forks](https://img.shields.io/github/forks/guardianproject/orbot-android?style=flat-square&color=blue)](https://github.com/guardianproject/orbot-android/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> The Github home of Orbot: Tor on Android (Also available on gitlab!)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.4k |
| 🍴 **Forks** | 462 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anonymity` `anticensorship` `censorship-circumvention` `security` `tor`

## 🎯 Categories

Mobile · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Orbot is the Guardian Project’s open‑source Android app that routes device traffic through the Tor network, providing on‑device anonymity and censorship‑circumvention. Written in Kotlin and backed by a large community (3.3 k ★, 462 forks), it automates the otherwise manual steps of configuring VPN‑style proxies, making it easy to embed Tor connectivity into Android workflows.

**Value**  
- **Automation of security‑critical steps** – Orbot eliminates the repetitive, error‑prone process of manually installing, configuring, and starting Tor on each device, turning it into a one‑click service that can be scripted or invoked from other apps.  
- **Reusable security layer** – By exposing a local SOCKS proxy and VPN interface, developers can route any network‑enabled component (e.g., browsers, messaging apps, custom APIs) through Tor without rewriting their own networking code.  
- **Open‑source transparency** – The code is publicly auditable, which is essential for security‑focused products that need to demonstrate privacy guarantees to users or regulators.

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – Clone the repository, follow the README to build the app, and verify that a test client can reach the internet via the Orbot SOCKS proxy on a development device.  
2. **Integration Wrapper** – Create a thin Android library or service that starts Orbot in the background (using the provided `Intent` API) and monitors its status, exposing a simple “Tor ready” callback to your app.  
3. **Workflow Embedding** – Replace existing direct‑network calls with proxy‑aware ones (e.g., OkHttp with a SOCKS proxy) or enable the VPN mode for full‑device routing, then add UI controls to let users enable/disable Tor as needed.  
4. **Iterative Testing** – Run automated UI tests on multiple Android versions, verify that traffic is indeed exiting the Tor network (e.g., checking IP via a test endpoint), and assess battery/network impact.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑06‑30) and widely used, but its integration surface (intents, callbacks, permission handling) is not fully documented in the metadata, requiring some exploratory work.  
- **Stability**: Suitable for internal tools, prototypes, or consumer‑facing apps that can tolerate occasional Tor‑related latency and the need for periodic updates to keep up with upstream security patches.  
- **Risks**:  
  * Integration effort may be higher than implied; verify the exact steps to start Orbot silently and handle failure modes.  
  * Dependency on the Guardian Project’s release cadence—ensure you have a process for monitoring and applying security updates.  
  * Battery and data‑usage considerations on mobile devices; plan for user‑opt‑in and clear communication about Tor’s performance characteristics.  

Overall, Orbot provides a robust, community‑validated way to add Tor anonymity to Android applications, with a clear path from PoC to production once the integration details are validated and operational monitoring is put in place.

### Русский

Резюме проекта guardianproject/orbot-android:

Проект Orbot: Tor на Android позволяет автоматизировать повторяющиеся задачи и уменьшить ручную работу, что особенно полезно для удаления повторяющихся операций из рабочего процесса. Типовой сценарий внедрения проекта - подключение инструментов к повторяющимся потокам и планирование операционных задач. Проект готов к использованию в прототипах или внутренних рабочих процессах, но требует проверки зависимости и поддержки перед внедрением в производство.

### 中文

**项目简介**  
Orbot 是 Guardian Project 开发的 Android 平台 Tor 客户端，提供系统级的网络流量匿名化。项目托管在 GitHub（亦有 GitLab 镜像），使用 Kotlin 编写，已获 3371 星、462 Fork，活跃维护至 2026‑06‑30。

**价值**  
- **自动化安全**：通过一键启动本地 Tor 代理，免去手动配置 VPN、代理或自行搭建匿名网络的繁琐步骤。  
- **可重复的工作流**：可把 Orbot 作为后台服务嵌入 CI/CD、移动安全测试或数据采集脚本，实现“启动‑使用‑关闭”全链路的自动化。  
- **降低运维成本**：统一的 API（Intent、Broadcast）让其他 Android 应用或脚本无需自行管理 Tor 节点，即可获得匿名通信能力。

**典型接入方式**  
1. **依赖声明**：在 `build.gradle` 中添加 `implementation 'org.torproject:orbot:latest'`（或直接引用项目源码）。  
2. **启动代理**：通过 `Intent`（`ACTION_START_TOR`）或 `OrbotHelper.startTor(context)` 启动 Tor 服务。  
3. **获取本地代理信息**：读取 `OrbotHelper.getProxyPort()`，在网络请求库（OkHttp、Retrofit、Volley 等）中配置 `Proxy(Proxy.Type.SOCKS, InetSocketAddress("127.0.0.1", port))`。  
4. **监控状态**：注册 `BroadcastReceiver` 监听 `ACTION_STATUS`，在代理就绪后再发起网络请求，确保可靠性。  
5. **脚本化/CI**：在 Android Instrumentation 测试或 Gradle Task 中调用上述步骤，实现自动化安全测试或数据抓取。

**生产可用性**  
- **成熟度**：项目活跃、星数高、Kotlin 代码质量良好，适合作为内部原型或安全敏感的业务组件。  
- **准备度**：中等。虽然功能完整，但缺乏官方的 Maven/Gradle 发行版，需要自行编译或引用源码；文档主要是 README，集成细节需自行验证。  
- **建议**：先在测试环境完成 **PoC**，确认启动时延、资源占用以及与现有网络栈的兼容性；随后进行依赖审计（Tor 版本、第三方库）并加入监控/日志后方可投入生产。  

总体而言，Orbot-android 能显著简化 Android 应用的匿名网络接入，适合需要快速实现安全通信的内部工具或原型开发；在正式生产环境使用前，建议完成小规模验证并做好运维监控。

## 🧭 Practical evaluation

**Value:** guardianproject/orbot-android helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 3371 GitHub stars
- 462 forks
- updated 2026-06-30
- primary language: Kotlin
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 67/100 |
| stars | 75/100 |
| topics | 63/100 |
| outlook | 71/100 |
| quality | 77/100 |
| recency | 80/100 |
| adoption | 73/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/guardianproject/orbot-android) · [← Back to Mobile](./README.md)</sub>
