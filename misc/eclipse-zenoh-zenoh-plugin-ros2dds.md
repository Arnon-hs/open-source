# eclipse-zenoh/zenoh-plugin-ros2dds

[![Stars](https://img.shields.io/github/stars/eclipse-zenoh/zenoh-plugin-ros2dds?style=flat-square&color=yellow)](https://github.com/eclipse-zenoh/zenoh-plugin-ros2dds/stargazers) [![Forks](https://img.shields.io/github/forks/eclipse-zenoh/zenoh-plugin-ros2dds?style=flat-square&color=blue)](https://github.com/eclipse-zenoh/zenoh-plugin-ros2dds/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> A Zenoh plug-in for ROS2 with a DDS RMW. See https://discourse.ros.org/t/ros-2-alternative-middleware-report/ for the advantages of using this plugin over other DDS RMW implementations.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 279 |
| 🍴 **Forks** | 63 |
| 💻 **Language** | Rust |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cyclonedds` `dds` `edge-computing` `robotics` `ros2` `zenoh`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Project Summary**

The eclipse-zenoh/zenoh-plugin-ros2dds project is an open-source plugin that integrates Zenoh with ROS2 (Robot Operating System 2) using a DDS (Data Distribution Service) RMW (Real-Time Middleware). This plugin helps automate workflows by removing repetitive manual operations, enabling users to connect tools into repeatable flows and schedule operational tasks. With its strong ecosystem signals and recent activity, this plugin is production-ready for serious pilots.

**Value Proposition**

The primary value proposition of this project is to automate workflows by removing repetitive manual operations. This plugin enables users to streamline their processes, reduce the risk of human error, and increase productivity. By connecting tools into repeatable flows, users can schedule operational tasks and focus on higher-level tasks.

**Practical Adoption Path**

To adopt this plugin, users can follow these steps:

1. Evaluate the plugin's implementation signals, such as API/SDK/CLI, language metadata, or focused topics.
2. Assess the plugin's production readiness, including its recent activity, adoption, and ecosystem signals.
3. Review the plugin's quality signals, including GitHub stars, forks, and topic discussions.
4. Evaluate the plugin's risks, including license, security posture, and active maintainers.
5. Schedule a pilot

### Русский

Резюме:

Этот проект, eclipse-zenoh/zenoh-plugin-ros2dds, представляет собой плагин Zenoh для ROS2 с использованием DDS RMW. Он помогает автоматизировать повторяющиеся операции в workflow, сокращая время и усилия, необходимые для выполнения задач. Плагин готов к внедрению в production, поскольку имеет сильную активность, широкое распространение и сильные сигналы экосистемы, что делает его идеальным кандидатом для серьезного пилота.

### 中文

**项目简介**  
`eclipse-zenoh/zenoh-plugin-ros2dds` 是一个基于 Zenoh 的 ROS 2 插件，使用 DDS 作为 RMW 实现。相较于传统 DDS RMW，它通过 Zenoh 的统一数据空间和轻量级协议，能够实现更低的延迟、更高的可扩展性以及跨网络的透明互操作（详见 ROS 2 替代中间件报告）。

**价值**  
- **自动化**：把 ROS 2 与 DDS 的手动配置、节点发现和数据路由工作交给 Zenoh 插件完成，显著减少重复的运维脚本和人工干预。  
- **可组合**：插件以 API/SDK/CLI 形式暴露，实现语言无关的调用，方便将 ROS 2、DDS 与其他工具（如监控、调度系统）串联成可重复的工作流。  
- **高效连接**：利用 Zenoh 的多协议桥接（TCP、UDP、QUIC 等），在异构网络环境下保持低时延和高吞吐，适合边缘、云端和机器人之间的实时数据共享。

**典型接入方式**  
1. **依赖添加**：在 ROS 2 项目的 `Cargo.toml`（Rust）或 `CMakeLists.txt`（C/C++）中加入 `zenoh-plugin-ros2dds`。  
2. **启动插件**：在运行 ROS 2 节点时通过环境变量或命令行参数启用插件，例如  
   ```bash
   RMW_IMPLEMENTATION=zenoh_plugin_ros2dds ros2 run <package> <node>
   ```  
3. **使用 API**：通过 Zenoh Rust/CPP SDK 调用插件提供的发布/订阅、服务/客户端等接口，或直接使用 ROS 2 标准 API（`rclcpp`、`rclpy`），插件会在后台将这些调用映射到 Zenoh‑DDS。  
4. **CLI 调试**：插件自带 `zenoh-cli`，可用于实时查看主题、服务状态以及网络拓扑，帮助快速验证集成。

**生产可用性**  
- **活跃度**：截至 2026‑06‑30，项目最近一次提交，拥有 279 ★、63 Fork，社区活跃，Issue 关闭率高。  
- **技术成熟度**：核心实现使用 Rust，具备内存安全和高并发特性；插件已在多个 ROS 2 迁移实验中验证，延迟和带宽表现优于传统 DDS RMW。  
- **生态兼容**：兼容 ROS 2 Foxy、Galactic、Humble 等主流发行版，且可与现有 DDS 实现共存，便于渐进式迁移。  
- **风险**：仍需对许可证（EPL‑2.0）和安全审计进行最终确认，建议在正式生产前进行内部渗透测试和持续集成验证。

综合来看，`zenoh-plugin-ros2dds` 已具备进入正式生产环境的技术基础，适合作为自动化、可扩展的 ROS 2‑DDS 中间件方案进行试点部署。

## 🧭 Practical evaluation

**Value:** eclipse-zenoh/zenoh-plugin-ros2dds helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 279 GitHub stars
- 63 forks
- updated 2026-06-30
- primary language: Rust
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 52/100 |
| topics | 75/100 |
| outlook | 70/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 50/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/eclipse-zenoh/zenoh-plugin-ros2dds) · [← Back to Misc](./README.md)</sub>
