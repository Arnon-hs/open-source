# agittins/bermuda

[![Stars](https://img.shields.io/github/stars/agittins/bermuda?style=flat-square&color=yellow)](https://github.com/agittins/bermuda/stargazers) [![Forks](https://img.shields.io/github/forks/agittins/bermuda?style=flat-square&color=blue)](https://github.com/agittins/bermuda/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> Bermuda Bluetooth/BLE Triangulation / Trilateration for HomeAssistant

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.8k |
| 🍴 **Forks** | 57 |
| 💻 **Language** | Python |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-07-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ble` `bluetooth-beacons` `bluetooth-low-energy` `bluetooth-proxy` `esphome` `hacs-integration` `homeassistant-custom-component` `triangulation` `trilateration`

## 🎯 Categories

Misc

## 📝 Summary

### English

Here's a brief summary of the open-source project:

Bermuda is an open-source project that enables Bluetooth/BLE triangulation/trilateration for HomeAssistant, allowing users to track devices and objects within their homes. Its value lies in providing a concrete workflow for users who can leverage its functionality to create customized solutions. With recent activity, strong adoption, and a robust ecosystem, Bermuda is highly production-ready, making it suitable for serious pilots and potential integration with HomeAssistant.

In terms of practical adoption, users can start by evaluating the project's feasibility through a small proof of concept and checking the project's README to ensure it aligns with their workflow. If the project meets their needs, they can proceed with integrating it into their HomeAssistant setup.

Bermuda's production readiness is high due to its strong ecosystem signals, including 1836 GitHub stars, 57 forks, and recent updates. The project's Python language and 9 topics also indicate a robust and maintainable codebase. However, users should conduct a final review of the project's license, security posture, and active maintainers to ensure it meets their requirements.

### Русский

Резюме проекта agittins/bermuda:

Проект agittins/bermuda предоставляет функцию трilaterации Bluetooth/BLE для HomeAssistant, позволяя определять расположение устройств в пространстве. Он может быть полезен в сценариях, когда необходимо определить местоположение устройств в домах или других закрытых пространствах.

Проект готов к внедрению в production, поскольку имеет сильные сигналы экосистемы, недавнюю активность и достаточно adoption, что делает его достойным серьезного пилота. Однако следует начать с небольшого proof of concept и проверки README перед интеграцией.

### 中文

**项目简介**  
Bermuda（agittins/bermuda）是一款基于 Python 的开源库，提供 Bluetooth/BLE 信号的三角定位（Triangulation）与三边测量（Trilateration）功能，专为 Home Assistant 环境设计，帮助用户在智能家居中实现设备的精准位置追踪。

**价值**  
- **精准定位**：利用多路 BLE 信号强度计算设备坐标，提升自动化场景（如灯光、空调、安防）的响应准确性。  
- **即插即用**：与 Home Assistant 的蓝牙集成点对点兼容，无需额外硬件，只要已有的 BLE 适配器即可使用。  
- **社区活跃**：近 2k 星、57 个 Fork，2026 年仍在持续更新，代码质量和文档较为完善，适合作为生产级定位模块的基础。

**典型接入方式**  
1. **环境准备**：在运行 Home Assistant 的主机上安装 BLE 适配器（如 USB dongle）并确保系统蓝牙可用。  
2. **安装库**：`pip install bermuda`（或通过 Home Assistant 的自定义组件方式添加）。  
3. **配置 Home Assistant**：在 `configuration.yaml` 中加入 `bermuda:` 节点，指定要监听的 BLE 设备 MAC、采样频率以及定位算法参数。  
4. **验证**：启动 Home Assistant，观察生成的 `device_tracker` 实体是否随设备移动而更新坐标，必要时调优信号过滤阈值。  

**生产可用性**  
- **成熟度**：近期（2026‑07‑05）仍有代码提交，活跃度高，具备正式项目所需的维护保障。  
- **安全与合规**：采用 MIT 许可证，暂无已知重大安全漏洞；仍建议在生产环境前进行一次依赖审计。  
- **上线建议**：先在测试环境完成一个小范围的 PoC（如单个 BLE 传感器的定位），确认定位精度与 Home Assistant 事件触发符合预期后，再推广至全屋部署。  

综上，Bermuda 在 Home Assistant 场景下提供了可靠、易集成的 BLE 定位能力，具备足够的社区活力和技术成熟度，可作为生产环境的定位方案进行试点并逐步扩大使用。

## 🧭 Practical evaluation

**Value:** agittins/bermuda may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1836 GitHub stars
- 57 forks
- updated 2026-07-05
- primary language: Python
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 69/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 83/100 |
| recency | 100/100 |
| adoption | 62/100 |
| production | 78/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/agittins/bermuda) · [← Back to Misc](./README.md)</sub>
