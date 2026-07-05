# tanlethanh/zedra

[![Stars](https://img.shields.io/github/stars/tanlethanh/zedra?style=flat-square&color=yellow)](https://github.com/tanlethanh/zedra/stargazers) [![Forks](https://img.shields.io/github/forks/tanlethanh/zedra?style=flat-square&color=blue)](https://github.com/tanlethanh/zedra/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Remote control for AI coding agents. Rust + GPUI + QUIC/UDP. Available on iOS/Android

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 115 |
| 🍴 **Forks** | 14 |
| 💻 **Language** | Rust |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-07-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude-code` `code-editor` `codex` `gpui` `mobile` `opencode` `p2p` `pi-agent` `remote-control` `terminal`

## 🎯 Categories

AI/ML · Frontend · Mobile

## 📝 Summary

### English

**Project Summary:**

Zedra is an open-source remote control for AI coding agents, allowing developers to add AI capabilities to their projects without starting from scratch. This Rust-based project utilizes GPU acceleration and QUIC/UDP for efficient performance on both iOS and Android platforms. With its potential for rapid prototyping and evaluation, Zedra is suitable for developers looking to integrate AI features into their workflows.

**Value:**

The primary value proposition of Zedra lies in its ability to simplify the integration of AI capabilities into existing projects. By leveraging a pre-built remote control for AI coding agents, developers can focus on building their applications rather than developing a complete AI model stack from scratch.

**Practical Adoption Path:**

To adopt Zedra, developers should start by evaluating the project through a small proof of concept and carefully reviewing the README documentation. This will help them understand the integration path and potential setup costs. Once familiar with the project, developers can begin integrating Zedra into their workflows, taking into account the project's medium production readiness and potential dependency and maintenance checks.

**Production Readiness:**

Zedra is considered production-ready with medium readiness, indicating that it is suitable for use in prototypes or internal workflows. However, before deploying Zedra in a production environment, developers

### Русский

Резюме:

Проект tanlethanh/zedra представляет собой удаленный контроллер для агентов AI-кодирования, написанный на Rust с использованием GPUI и QUIC/UDP. Он доступен на iOS и Android, что позволяет добавлять AI-способности к существующим продуктам без необходимости начинать с нуля. Проект можно использовать для прототипирования AI-функций, создания рабочих процессов RAG или оценки инструментов моделирования, но требует тщательного проверки на этапе интеграции и поддержки перед внедрением в production.

### 中文

**项目简介（2‑3 句）**  
Zedra（tanlethanh/zedra）是一款基于 Rust、GPUI 与 QUIC/UDP 的远程控制平台，专为 AI 编码代理提供轻量化的交互层。它可在 iOS 与 Android 设备上运行，让开发者无需从零搭建模型堆栈，即可快速为移动端产品加入 AI 能力。

---

## 价值点

1. **快速原型**：通过统一的远程控制协议，开发者可以在本地机器上运行强大的 AI 代理，而在移动端仅需一个轻量客户端，即可完成代码补全、RAG（检索增强生成）或多步骤工作流的演示。  
2. **统一模型接入**：Zedra 抽象了模型调用细节，支持多种后端（OpenAI、Claude、LLaMA 等），因此团队可以在不更换代码的前提下切换或评估不同模型。  
3. **跨平台一致性**：一次实现的控制逻辑可同时部署到 iOS 与 Android，降低移动端 AI 功能的研发成本。  

## 典型接入方式

1. **阅读 README 与示例**  
   - 项目根目录提供了最小化的 “Hello World” 示例，展示如何在 Rust 端启动 QUIC/UDP 服务器并通过 GPUI 渲染 UI。  
2. **在本地搭建后端服务**  
   - 使用 `cargo run --release` 启动 Rust 代理服务，配置 `config.toml` 中的模型 API 密钥与网络参数（QUIC/UDP 端口）。  
3. **移动端集成**  
   - 将 `zedra-ios` 或 `zedra-android` 子模块作为 CocoaPods / Gradle 依赖引入，或直接复制 `client` 目录的 Swift/Kotlin 代码。  
   - 在移动端代码中调用 `ZedraClient.connect(serverAddress, port)`，随后通过回调发送指令（如 `run_code`, `fetch_context`）并接收 JSON 格式的响应。  
4. **小范围 PoC**  
   - 在现有项目中添加一个 “AI 助手” 按钮，触发 `ZedraClient` 与后端交互，验证网络延迟、模型响应时长以及错误处理逻辑。  

> **提示**：因为项目依赖 GPUI（一个仍在快速演进的 UI 框架），建议先在桌面环境（macOS/Linux）验证完整链路，再迁移到移动端。

## 生产可用性评估

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | ★★☆☆☆（中等） | 项目已有 115 星、14 Fork，最近一次提交是 2026‑07‑05，活跃度尚可，但文档仍偏简略，部分依赖（GPUI、QUIC）在移动端的兼容性需要自行验证。 |
| **功能完整度** | ★★★☆☆ | 基础的远程控制、模型调用已实现，RAG 与多轮对话等高级特性仍需自行组合。 |
| **集成成本** | ★★☆☆☆ | 需要了解 Rust、QUIC/UDP 配置以及 iOS/Android 原生网络层，入门门槛相对较高。推荐先做 PoC，确认网络、模型费用与 latency 再决定大规模落地。 |
| **运维风险** | ★★☆☆☆ | 依赖 Rust 编译链和 GPUI，升级时可能出现二进制不兼容；QUIC/UDP 在企业防火墙环境下可能被拦截，需要额外的网络策略。 |
| **适用场景** | ★★★★☆ | 原型开发、内部工具、AI 功能快速验证、跨平台 AI 代理实验。 |
| **生产建议** | **中等** | 适合作为内部或 B2B 产品的 AI 能力入口。若要面向大规模终端用户，需进行：<br>1. 完整的安全审计（QUIC/UDP 加密、身份验证）<br>2. 稳定的 CI/CD 流程（Rust 编译、移动端打包）<br>3. 监控与日志系统（模型调用计费、网络异常） |

**结论**：Zedra 为希望在移动端快速加入 AI 编码/协作能力的团队提供了一个可行的起点，尤其适合原型验证和内部工具。若计划在生产环境大规模使用，建议在小范围 PoC 成功后，投入资源完善文档、自动化部署以及网络安全策略。

## 🧭 Practical evaluation

**Value:** tanlethanh/zedra helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 115 GitHub stars
- 14 forks
- updated 2026-07-05
- primary language: Rust
- 10 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 73/100 |
| recency | 100/100 |
| adoption | 40/100 |
| production | 72/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/tanlethanh/zedra) · [← Back to AI/ML](./README.md)</sub>
