# WiVRn/WiVRn

[![Stars](https://img.shields.io/github/stars/WiVRn/WiVRn?style=flat-square&color=yellow)](https://github.com/WiVRn/WiVRn/stargazers) [![Forks](https://img.shields.io/github/forks/WiVRn/WiVRn?style=flat-square&color=blue)](https://github.com/WiVRn/WiVRn/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> The Linux OpenXR streaming application to standalone headsets

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.5k |
| 🍴 **Forks** | 165 |
| 💻 **Language** | C++ |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`oculus` `oculus-quest` `oculus-quest-2` `openxr` `vr`

## 🎯 Categories

Misc

## 📝 Summary

### English

Here's a brief summary of the WiVRn/WiVRn project:

WiVRn/WiVRn is an open-source Linux application that enables OpenXR streaming to standalone headsets, offering a valuable solution for developers and organizations seeking to integrate virtual reality capabilities into their workflows. The project's usefulness is contingent upon its README and activity aligning with a concrete workflow, making it essential to evaluate its integration path and setup costs before adoption. While it holds moderate production readiness, WiVRn/WiVRn is best suited for prototype development or internal workflows, requiring dependency and maintenance checks before deployment.

### Русский

Резюме:

WiVRn/WiVRn - облачное приложение Linux для потоковой передачи в standalone головные устройства через OpenXR. Это утилитарное решение, которое может быть полезно для прототипирования или внутренних потоков, когда README и активность соответствуют конкретному рабочему процессу. Однако, перед внедрением необходимо проверить стоимость настройки и потенциальные риски интеграции.

### 中文

**价值**  
WiVRn 是一款基于 Linux 的 OpenXR 流媒体客户端，能够把 PC 上的 XR 内容实时投射到独立的头显（如 Meta Quest、Pico 等），从而在不依赖专有 SDK 的情况下实现高质量的 VR/AR 体验。它适合原型开发、内部演示以及需要快速验证 XR 场景的团队，省去自行编写跨平台渲染和网络同步代码的成本。

**典型接入方式**  

1. **环境准备**  
   - 在 Linux 主机上安装 `cmake`、`gcc/g++`、`libopenxr`、`ffmpeg` 等依赖（项目的 README 已提供完整的依赖列表）。  
   - 在目标独立头显上通过 Side‑load 安装生成的 `WiVRnClient.apk`（Android 包）或直接使用官方提供的预编译二进制。

2. **构建服务器端**  
   ```bash
   git clone https://github.com/WiVRn/WiVRn.git
   cd WiVRn
   mkdir build && cd build
   cmake .. -DCMAKE_BUILD_TYPE=Release
   make -j$(nproc)
   sudo make install
   ```
   生成的 `wivrn_server` 可直接运行，默认监听本机 5555 端口。

3. **启动流媒体**  
   - 在服务器上执行 `wivrn_server`，它会自动检测本机的 OpenXR 应用（如 SteamVR、Godot、Unity 导出的 OpenXR 项目）并开启流媒体会话。  
   - 在头显上打开 WiVRn 客户端，搜索同一局域网内的服务器并点击连接，即可看到实时渲染的画面。

4. **集成到现有工作流**  
   - 对于已有的 OpenXR 项目，只需保证在启动时加载 `XR_KHR_opengl_enable`（或 Vulkan）扩展，WiVRn 会拦截并压缩帧数据，无需修改业务代码。  
   - 如需自定义编解码参数（分辨率、码率、帧率），可在服务器端的配置文件 `wivrn.conf` 中调整。

**生产可用性**  

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | ★★☆☆☆（中等） | 项目活跃（2026‑07‑01 最近更新），拥有 1.5k+ 星、165 个 fork，社区贡献相对稳定。 |
| **功能完整性** | ★★★☆☆ | 支持 OpenXR 1.0、主流独立头显、常用编解码（H.264/H.265），但缺少企业级监控与自动化部署工具。 |
| **集成成本** | ★★☆☆☆ | 需要自行编译服务器端并完成依赖配置，文档虽完整但示例较少，建议先做小规模 PoC 验证网络与性能。 |
| **可靠性** | ★★☆☆☆ | 实时流媒体对网络质量敏感；在不稳定的 Wi‑Fi 环境下可能出现卡顿或掉帧，建议使用千兆有线或 5GHz Wi‑Fi。 |
| **维护性** | ★★☆☆☆ | 代码基于 C++，依赖 OpenXR 与 FFmpeg，升级时需关注上游库的兼容性。 |
| **适用场景** | 原型、内部演示、研发测试 | 适合需要快速在独立头显上验证 PC 端 XR 内容的团队；不建议直接用于面向终端用户的大规模生产环境。 |

**结论**  
WiVRn 在原型阶段和内部工作流中能够显著降低跨平台 XR 开发的门槛，接入方式相对直接（编译服务器、Side‑load 客户端）。若要在生产环境使用，需要对网络、编解码参数以及依赖库的版本进行严格测试，并可能需要自行实现监控、日志以及自动化部署脚本。整体来看，它是一个 **中等成熟度、适合原型验证** 的解决方案，进入生产前建议先完成小规模的概念验证（PoC），并评估长期维护成本。

## 🧭 Practical evaluation

**Value:** WiVRn/WiVRn may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1488 GitHub stars
- 165 forks
- updated 2026-07-01
- primary language: C++
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 68/100 |
| topics | 63/100 |
| outlook | 55/100 |
| quality | 63/100 |
| recency | 40/100 |
| adoption | 64/100 |
| production | 54/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/WiVRn/WiVRn) · [← Back to Misc](./README.md)</sub>
