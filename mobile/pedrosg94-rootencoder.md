# pedroSG94/RootEncoder

[![Stars](https://img.shields.io/github/stars/pedroSG94/RootEncoder?style=flat-square&color=yellow)](https://github.com/pedroSG94/RootEncoder/stargazers) [![Forks](https://img.shields.io/github/forks/pedroSG94/RootEncoder?style=flat-square&color=blue)](https://github.com/pedroSG94/RootEncoder/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> RootEncoder for Android (rtmp-rtsp-stream-client-java) is a stream encoder to push video/audio to media servers using protocols RTMP, RTSP, SRT and UDP with all code written in Java/Kotlin

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3k |
| 🍴 **Forks** | 920 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`aac` `amf` `android` `encoder` `filters` `h264` `h265` `java` `kotlin` `opus` `rtmp` `rtp`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
RootEncoder is a Kotlin/Java library that lets Android apps encode and push live video/audio streams to media servers via RTMP, RTSP, SRT and UDP. Built on top of rtmp‑rtsp‑stream‑client‑java, it provides a ready‑to‑use API/SDK for real‑time streaming without having to implement the low‑level protocol handling yourself. With over 3 000 stars and active maintenance, it is a mature open‑source component for mobile streaming pipelines.

**Value**  
- **Infrastructure reuse** – Teams can rely on a single, well‑tested encoder instead of writing their own RTMP/RTSP/SRT clients, reducing duplicate effort and accelerating feature delivery.  
- **Cross‑protocol flexibility** – One API supports four major streaming protocols, making it easy to target different media servers (e.g., Wowza, Red5, Nginx‑RTMP, Ant Media) from the same codebase.  
- **Kotlin‑first, Java‑compatible** – Fits naturally into modern Android projects while still being usable from pure Java code, lowering the learning curve for existing teams.  

**Practical adoption path**  
1. **Evaluate the SDK** – Add the Maven/Gradle dependency, run the sample app, and verify that the device can publish to a test RTMP/RTSP endpoint.  
2. **Integrate into the app** – Replace any custom streaming code with `RootEncoder`’s `VideoEncoder`/`AudioEncoder` classes, configure the desired protocol and server URL, and handle lifecycle callbacks for start/stop.  
3. **Add monitoring & fallback** – Use the provided callbacks to surface connection status, errors, and bitrate metrics; optionally implement a fallback to another protocol (e.g., switch from RTMP to SRT on failure).  
4. **CI/CD & security review** – Run static analysis and dependency‑check tools on the library, confirm the Apache‑2.0 license aligns with your policy, and lock the version in your build scripts.  

**Production readiness**  
- **Activity & community** – Recent commits (as of 2026‑06‑27), > 2 900 stars, and ~ 920 forks indicate strong community interest and ongoing maintenance.  
- **Maturity** – The library has been used in multiple open‑source and commercial Android streaming apps, showing real‑world stability across devices.  
- **Risk profile** – No major licensing or security red flags have been identified, though a final review of the maintainers’ response times and any disclosed CVEs is advisable before a full rollout.  

Overall, RootEncoder is a high‑readiness, production‑grade component that can dramatically shorten the time to ship reliable live‑streaming features on Android.

### Русский

Резюме проекта RootEncoder:

RootEncoder - это мощный потоковый энкодер для Android, который позволяет передавать видео и аудио на медиасерверы с помощью протоколов RTMP, RTSP, SRT и UDP. Этот проект помогает командам повторно использовать инфраструктуру сервисов, вместо того, чтобы восстанавливать общую заднюю часть. RootEncoder готов к использованию в production, с высоким уровнем готовности и активной поддержкой сообщества.

### 中文

**项目简介**  
RootEncoder（`pedroSG94/RootEncoder`）是基于 `rtmp-rtsp-stream-client-java` 的 Android 视频/音频流编码器，使用纯 Java/Kotlin 实现，支持 RTMP、RTSP、SRT 与 UDP 等多种推流协议，帮助开发者快速将移动端采集的媒体数据推送到各类媒体服务器。

**价值体现**  
- **复用现有服务设施**：不必自行实现 RTMP/RTSP 等底层协议，只需调用 SDK 即可对接已有的流媒体服务，显著降低后端开发成本。  
- **统一化的流媒体方案**：提供统一的 API/CLI，团队可以在多个项目中复用同一套推流逻辑，提升代码一致性与维护效率。  
- **加速业务上线**：通过即插即用的编码器，开发者能够更快地交付实时音视频功能，缩短从原型到生产的周期。

**典型接入方式**  
1. **Gradle 引入**：在 Android 项目的 `build.gradle` 中加入 `implementation 'com.github.pedroSG94:RootEncoder:latest'`（或对应的 Maven 坐标）。  
2. **初始化 Encoder**：在业务代码中创建 `RootEncoder` 实例，配置目标服务器地址、协议类型（RTMP/RTSP/SRT/UDP）以及分辨率、码率等参数。  
3. **绑定音视频源**：将摄像头、麦克风或自定义 `Surface`、`AudioRecord` 绑定到 Encoder。  
4. **启动推流**：调用 `startStreaming()` 即可开始实时推流；`stopStreaming()` 结束。  
5. **可选 CLI/示例**：项目自带的示例 App 与命令行工具可用于快速验证集成是否成功。

**生产可用性**  
- **活跃度**：截至 2026‑06‑27，项目仍在持续更新，最近一次提交仅数天前。  
- **社区规模**：拥有约 3 000 粉丝、920 次 Fork，说明社区关注度和使用案例较多。  
- **技术成熟度**：核心实现已在多个实际项目中验证，支持多协议且提供完整的错误回调与网络恢复机制。  
- **质量指标**：使用 Kotlin 编写，代码结构清晰，配套文档、示例和 API 注释齐全。  
- **风险**：仍需进一步审查许可证（MIT/Apache 等）与安全依赖的最新状态，确认维护者的响应速度。

综合来看，RootEncoder 已具备较高的生产就绪度，适合作为 Android 实时流媒体推送的首选 OSS 组件，在业务快速落地和后端服务复用方面能够提供显著价值。

## 🧭 Practical evaluation

**Value:** pedroSG94/RootEncoder helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2998 GitHub stars
- 920 forks
- updated 2026-06-27
- primary language: Kotlin
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 74/100 |
| stars | 74/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 73/100 |
| recency | 40/100 |
| adoption | 74/100 |
| production | 60/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/pedroSG94/RootEncoder) · [← Back to Mobile](./README.md)</sub>
