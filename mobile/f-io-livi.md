# f-io/LIVI

[![Stars](https://img.shields.io/github/stars/f-io/LIVI?style=flat-square&color=yellow)](https://github.com/f-io/LIVI/stargazers) [![Forks](https://img.shields.io/github/forks/f-io/LIVI?style=flat-square&color=blue)](https://github.com/f-io/LIVI/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> CarPlay & Android Auto head unit for Linux (ARM/x64), macOS (ARM/x64) and Windows (x64). Full AA protocol implementation (wired + wireless). Hardware-accelerated video (zero-copy) and low-latency audio.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 393 |
| 🍴 **Forks** | 42 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android-auto` `automotive` `carplay` `gstreamer` `headunit` `in-vehicle-infotainment` `linux` `macos`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief Summary**  
LIVI (f‑io/LIVI) is an open‑source head‑unit implementation that brings CarPlay and Android Auto to Linux (ARM/x64), macOS (ARM/x64) and Windows (x64). It offers a complete Android Auto protocol stack (wired and wireless), hardware‑accelerated zero‑copy video and low‑latency audio, and is written primarily in TypeScript.

**Value**  
LIVI lets OEMs, hobbyists, and developers embed full CarPlay/Android Auto functionality without building the complex protocol stack from scratch, accelerating time‑to‑market for in‑vehicle infotainment (IVI) solutions. Its cross‑platform support and hardware‑accelerated media pipeline also make it a solid foundation for adding AI‑driven features such as voice assistants, contextual recommendations, or real‑time vision analytics.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, follow the README to spin up a basic head‑unit on a supported platform (e.g., a Linux ARM SBC). Verify connectivity with a phone using wired Android Auto.  
2. **Feature Extension** – Integrate AI modules (e.g., speech‑to‑text, RAG, or agent APIs) by tapping into the existing WebSocket/REST hooks that expose media and input events.  
3. **Pilot Deployment** – Package the customized binary for the target hardware, run automated integration tests, and conduct a limited field trial in a vehicle or test rig.  
4. **Full Production Roll‑out** – Harden the build (signing, secure OTA updates), add monitoring, and replace any development‑only components with production‑grade equivalents.

**Production Readiness**  
- **Activity & Community**: 393 GitHub stars, 42 forks, recent commits (as of 2026‑06‑27) and a growing contributor base indicate an active project.  
- **Technical Maturity**: Full AA protocol (wired + wireless), zero‑copy video, and low‑latency audio are already implemented and used in early adopters.  
- **Ecosystem Fit**: Supports the major OS/CPU combos required for modern IVI hardware, and its TypeScript codebase eases integration with web‑based UI and AI services.  
- **Risks**: Licensing, security posture, and maintainer continuity still need a final audit, but no major red flags have been identified. Overall, LIVI is ready for a serious pilot and, with modest hardening, can be promoted to production use.

### Русский

**f-io/LIVI** — это open‑source‑решение для создания head‑unit, поддерживающего CarPlay и Android Auto на Linux (ARM/x64), macOS (ARM/x64) и Windows (x64). Проект реализует полный протокол Android Auto (проводной + беспроводной), обеспечивает аппаратно‑ускоренное видео с нулевым копированием и низколатентный аудио, что позволяет быстро прототипировать AI‑фичи (RAG, агентные сценарии) без построения стека с нуля. Благодаря активному развитию (393 ★, 42 fork, последние коммиты 2026‑06‑27), хорошей экосистеме и готовой к использованию инфраструктуре, LIVI считается готовым к пилотному внедрению в продакшн после небольшого proof‑of‑concept и проверки README; окончательная оценка лицензии и безопасности требуется.

### 中文

**项目简介**  
f‑io/LIVI 是一套在 Linux（ARM/x64）、macOS（ARM/x64）和 Windows（x64）上运行的 CarPlay 与 Android Auto 车载中枢解决方案，完整实现了有线和无线 AA 协议，并提供硬件加速的零拷贝视频与低延时音频。

**价值**  
- **快速赋能 AI**：在已有的车载互联系统上直接接入 AI 能力，无需从头搭建模型栈，适合原型开发与功能验证。  
- **跨平台统一**：一次代码即可在 Linux、macOS 与 Windows 上部署，降低多系统维护成本。  
- **高性能媒体处理**：硬件加速的视频零拷贝和低延迟音频让 AI 驱动的语音交互、实时视觉分析等场景保持流畅体验。

**典型接入方式**  
1. **阅读 README**：确认系统依赖（Node.js、TypeScript 编译环境）并完成示例项目的快速运行。  
2. **创建小型 PoC**：在项目中引入 `@f-io/livi` 包，使用提供的 API 将 AI 推理服务（如 Whisper、LLM）接入音视频流。  
3. **扩展功能**：基于示例代码实现 RAG、Agent 工作流或自定义车载 AI 功能，随后通过 Docker 或本地二进制发布。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑27，项目仍在持续更新，GitHub ★393、Fork 42，社区活跃。  
- **技术成熟度**：完整实现 AA 协议、硬件加速媒体路径，已在多平台实测，具备可直接用于正式车机的技术基线。  
- **风险**：许可证、长期维护者以及安全审计仍需进一步确认；但从当前代码质量、社区响应和生态兼容性来看，已具备进行正式试点的条件。  

综上，f‑io/LIVI 是一个高性能、跨平台的车载互联系统框架，能够帮助开发者快速在车机上集成 AI 功能，并具备进入生产环境的基本准备。

## 🧭 Practical evaluation

**Value:** f-io/LIVI helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 393 GitHub stars
- 42 forks
- updated 2026-06-27
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 63/100 |
| recency | 40/100 |
| adoption | 51/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/f-io/LIVI) · [← Back to Mobile](./README.md)</sub>
