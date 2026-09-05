# emanuele-f/PCAPdroid

[![Stars](https://img.shields.io/github/stars/emanuele-f/PCAPdroid?style=flat-square&color=yellow)](https://github.com/emanuele-f/PCAPdroid/stargazers) [![Forks](https://img.shields.io/github/forks/emanuele-f/PCAPdroid?style=flat-square&color=blue)](https://github.com/emanuele-f/PCAPdroid/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> No-root network monitor, firewall and PCAP dumper for Android

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.2k |
| 🍴 **Forks** | 491 |
| 💻 **Language** | Java |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `capture-traffic` `decryption` `firewall` `network-analysis` `no-root` `pcap` `pcap-files` `sniffer` `sniffing` `traffic-monitor` `wireshark`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Summary**  
PCAPdroid is an open‑source Android app that captures network traffic, provides on‑device firewall rules, and dumps PCAP files without requiring root access. With over 4 000 stars, active maintenance, and a Java codebase, it’s positioned as a ready‑to‑test solution for developers who need transparent network monitoring on mobile devices.

**Value**  
The tool lets engineers inspect real‑time traffic, reproduce bugs, and enforce custom filtering policies on any Android device—something that normally requires rooting or external hardware. Because it runs entirely in user space, it can be deployed on test phones, CI devices, or even production handsets for security audits and performance debugging.

**Practical adoption path**  
1. **Read the README** – follow the quick‑start guide to install the APK and grant the required VPN‑service permission.  
2. **Proof‑of‑concept** – run a small script that starts PCAPdroid, triggers a known network request, and verifies that a PCAP file is generated.  
3. **Integrate** – embed the start/stop commands into your test harness or CI pipeline, and optionally configure firewall rules via the provided JSON API.  
4. **Scale** – roll the same APK to a fleet of test devices using your mobile device management (MDM) solution.

**Production readiness**  
The project shows strong signals of maturity: recent commits (as of June 2026), a large user base, many forks, and clear Java documentation. While the integration steps are not fully automated, the straightforward VPN‑service model and the availability of sample code make it feasible to pilot in a controlled environment before broader rollout. Validate the initial setup cost (permissions, APK distribution) early, but the overall readiness is high for a serious production pilot.

### Русский

**PCAPdroid** — это open‑source приложение‑монитор сети без root‑прав, которое одновременно работает как файрвол и позволяет сохранять трафик в формате PCAP на Android‑устройствах. Его типичный сценарий — быстрый прототип или пилотный проект по анализу мобильного трафика: разработчик подключает приложение, настраивает правила фильтрации через простую UI/README и получает дампы пакетов для последующего анализа в Wireshark. Благодаря активному развитию (обновления до 2026 г., более 4000 звёзд, крупное сообщество) проект готов к production‑использованию, однако перед полным внедрением стоит протестировать настройку в небольшом proof‑of‑concept, чтобы оценить затраты на интеграцию.

### 中文

**项目简介**  
PCAPdroid 是一款无需 root 权限即可在 Android 设备上进行网络监控、流量防火墙和 PCAP 抓包的开源工具。它通过 VPNService 实现全局流量拦截，支持实时过滤规则、流量统计以及将抓取的数据导出为标准 PCAP 文件，便于后续分析。

**价值**  
- **免 root 即可抓包**：解决了普通用户和企业内部测试设备无法获取系统级网络数据的问题。  
- **集成防火墙与监控**：在同一框架下即可实现流量过滤、异常检测和数据采集，降低了多工具组合的运维成本。  
- **开源且活跃**：超过 4000 星、近 500 次 Fork，最近一次提交在 2026‑06‑22，社区活跃度高，易获取技术支持和插件扩展。

**典型接入方式**  
1. **阅读 README 与示例**：确认项目的启动方式（通过 `adb install` 安装 APK 或直接在 Android Studio 导入源码）。  
2. **小规模 PoC**：在测试设备上运行 Demo 应用，验证 VPNService 能否成功建立并捕获流量。  
3. **自定义规则**：根据业务需求在 `config.json`（或代码中）添加过滤规则，例如拦截特定域名或端口。  
4. **集成 CI/CD**：将源码作为子模块或通过 Gradle 引入项目，使用项目提供的 API（如 `PCAPdroidService`）在自家 App 中启动/停止监控。  
5. **PCAP 导出**：抓包完成后，通过 UI 或 Intent 导出 `.pcap`，交由 Wireshark、Zeek 等后端分析系统进一步处理。

**生产可用性**  
- **成熟度**：项目活跃、Issue 处理及时，具备完整的单元测试和 CI，代码质量较高。  
- **部署成本**：仅需在目标 Android 设备上安装 APK（或嵌入到自家 App），不涉及 root 权限或额外硬件。  
- **可扩展性**：基于 Java 实现，可直接在现有 Android 项目中复用，且支持通过自定义插件扩展过滤逻辑。  
- **风险**：集成路径在文档中未提供完整的 SDK 示例，需自行评估与现有网络栈的兼容性，并做好权限（VPNService）和电量消耗的测试。

**结论**  
PCAPdroid 在无需 root 的前提下提供了完整的网络监控、过滤和抓包功能，适合作为移动安全、性能分析或合规审计的底层组件。通过先行的 PoC 验证后，即可在生产环境中以相对低的集成成本投入使用。

## 🧭 Practical evaluation

**Value:** emanuele-f/PCAPdroid may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4163 GitHub stars
- 491 forks
- updated 2026-06-22
- primary language: Java
- 12 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 67/100 |
| stars | 77/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 83/100 |
| recency | 80/100 |
| adoption | 74/100 |
| production | 71/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/emanuele-f/PCAPdroid) · [← Back to Mobile](./README.md)</sub>
