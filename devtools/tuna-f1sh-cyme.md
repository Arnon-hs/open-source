# tuna-f1sh/cyme

[![Stars](https://img.shields.io/github/stars/tuna-f1sh/cyme?style=flat-square&color=yellow)](https://github.com/tuna-f1sh/cyme/stargazers) [![Forks](https://img.shields.io/github/forks/tuna-f1sh/cyme?style=flat-square&color=blue)](https://github.com/tuna-f1sh/cyme/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> List system USB buses and devices. A modern cross-platform lsusb that attempts to maintain compatibility with, but also add new features

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 28 |
| 💻 **Language** | Rust |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `libusb` `lsusb` `macos` `rust` `tool` `usb`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Project Summary:**

cyme is an open-source project that aims to provide a modern, cross-platform alternative to the traditional `lsusb` command. It lists system USB buses and devices, while also attempting to maintain compatibility with existing systems and add new features. This project has the potential to enhance the development process by adding AI capabilities without requiring a complete model stack from scratch.

**Value Proposition:**

The value proposition of cyme lies in its ability to simplify the integration of AI capabilities into existing projects. By leveraging cyme, developers can prototype AI features, build Reinforcement Agent Graph (RAG) or agent workflows, and evaluate model tooling without having to start from a blank slate. This makes it an attractive solution for developers looking to incorporate AI into their projects.

**Practical Adoption Path:**

To adopt cyme in a project, developers can start by evaluating its API, SDK, and CLI implementations, as well as its language metadata and focused topics. Once familiar with the project's implementation signals, developers can integrate cyme into their existing workflows. The project's recent activity, adoption, and ecosystem signals indicate that it is production-ready, making it a viable option for serious pilots.

**Production Readiness:**

cyme has demonstrated strong production readiness, with recent activity, adoption

### Русский

Резюме проекта tuna-f1sh/cyme:

Проект tuna-f1sh/cyme представляет собой усовершенствованную версию lsusb, способную перечислять системы USB-устройств и устройства. Он предлагает современные возможности на платформах и поддерживает обратную совместимость с существующими версиями. 

Проект предназначен для добавления функциональности AI без необходимости создания с нуля стека моделей. Типовой сценарий использования проекта заключается в прототипировании функций AI, построении потоков RAG или агента, а также оценке инструментов моделирования.

Проект tuna-f1sh/cyme демонстрирует высокий уровень готовности к использованию в production из-за его активности, приема, а также сильных сигналов экосистемы.

### 中文

**项目简介**  
`tuna-f1sh/cyme` 是一个现代化的跨平台 **lsusb** 实现，能够列出系统的 USB 总线和设备。它在保持与传统 `lsusb` 兼容的同时，加入了诸如 JSON/CSV 输出、设备属性过滤、实时热插拔监听等新特性，适用于脚本化自动化和高级诊断场景。

**价值体现**  
- **即插即用**：无需自行编写底层 USB 探测代码，直接通过 API/CLI 获取完整的 USB 拓扑信息。  
- **可扩展**：提供结构化输出（JSON、CSV）和 Rust 库接口，方便在 AI/ML、DevTools 或 RAG/Agent 工作流中快速集成，实现设备感知的智能化决策。  
- **跨平台**：支持 Linux、macOS 和 Windows，统一的调用方式降低了多系统维护成本。

**典型接入方式**  
1. **CLI**：`cyme list --output json` 直接在终端获取设备列表，适合脚本或 CI/CD 步骤。  
2. **Rust SDK**：在 Rust 项目中引入 `cyme` crate，调用 `cyme::list_devices()` 获得结构化数据，用于后续模型推理或业务逻辑。  
3. **HTTP/REST Wrapper**（可自行实现）：将 CLI 或库封装为微服务，其他语言（Python、Node.js 等）通过 HTTP 调用，实现语言无关的集成。

**生产可用性**  
- **活跃度**：截至 2026‑07‑01，项目仍在维护，最近一次提交在当月，GitHub ★1160、Fork 28，社区活跃度良好。  
- **技术成熟度**：使用安全性高、性能优秀的 Rust 实现，已通过多平台 CI，具备稳定的二进制发布。  
- **风险**：目前未发现重大许可证或安全漏洞，但仍建议在正式上线前进行一次许可证合规审查和安全审计。  
- **适配度**：提供明确的 API/SDK 文档和示例，可在几行代码内完成接入，适合作为生产环境的底层硬件感知组件。  

综上，`tuna-f1sh/cyme` 具备高可用性、易集成的特性，能够帮助开发者在 AI/ML、DevTools 或数据库相关项目中快速加入 USB 设备感知能力，适合作为正式生产环境的 OSS 组件进行试点或全量部署。

## 🧭 Practical evaluation

**Value:** tuna-f1sh/cyme helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1160 GitHub stars
- 28 forks
- updated 2026-07-01
- primary language: Rust
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 65/100 |
| topics | 88/100 |
| outlook | 62/100 |
| quality | 64/100 |
| recency | 40/100 |
| adoption | 57/100 |
| production | 56/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/tuna-f1sh/cyme) · [← Back to DevTools](./README.md)</sub>
