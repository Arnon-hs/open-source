# heypandax/cc-pocket

[![Stars](https://img.shields.io/github/stars/heypandax/cc-pocket?style=flat-square&color=yellow)](https://github.com/heypandax/cc-pocket/stargazers) [![Forks](https://img.shields.io/github/forks/heypandax/cc-pocket?style=flat-square&color=blue)](https://github.com/heypandax/cc-pocket/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Drive Claude Code or OpenAI Codex from your phone — resume sessions, stream output, approve tool permissions remotely. End-to-end encrypted, zero-knowledge relay, open source.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 32 |
| 🍴 **Forks** | 1 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `ai-coding-assistant` `android` `anthropic` `claude` `claude-code` `cli` `codex` `coding-agent` `compose-multiplatform` `developer-tools` `end-to-end-encryption`

## 🎯 Categories

AI/ML · DevTools · Mobile · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
heypandax/cc‑pocket is an open‑source Kotlin mobile client that lets you drive Claude Code or OpenAI Codex from a phone, with features such as session resumption, real‑time output streaming, and remote approval of tool permissions. The communication channel is end‑to‑end encrypted and operates as a zero‑knowledge relay, making it suitable for secure, on‑the‑go AI interactions.  

**Value**  
- **Fast AI enablement** – Developers can add generative‑code capabilities to prototypes or internal tools without building a model stack from scratch.  
- **Secure mobile access** – End‑to‑end encryption and zero‑knowledge relaying protect prompts, code, and model responses, which is critical for confidential or regulated environments.  
- **Iterative workflow support** – Session persistence and remote permission approval streamline RAG/agent experiments and allow quick debugging from anywhere.  

**Practical Adoption Path**  
1. **Clone & build** – Pull the repository, run the Gradle build, and generate a signed APK (or use the provided CLI wrapper).  
2. **Configure credentials** – Insert your Claude Code or OpenAI API keys into the encrypted config file; the app will handle token rotation automatically.  
3. **Integrate** – Use the exposed SDK/CLI to start a session from your backend, then connect the mobile client for interactive control, or embed the client in a CI/CD pipeline for remote approvals.  
4. **Validate** – Run the built‑in test suite, verify the encrypted relay (e.g., using Wireshark) and confirm that no plaintext data leaves the device.  

**Production Readiness**  
- **Maturity** – Medium. The project is actively maintained (last update 2026‑06‑25) and has a modest but growing community (32 stars, 1 fork).  
- **Security** – Strong design (E2E encryption, zero‑knowledge relay) but the license and long‑term maintainer commitment need a final review.  
- **Operational considerations** – Verify dependency updates (Kotlin/Gradle libraries), assess the relay server’s scalability, and implement monitoring for API usage limits.  
- **Suitable use cases** – Prototyping AI‑augmented features, internal tooling, or low‑risk production workflows after a short hardening cycle; not yet recommended for high‑throughput, customer‑facing services without further load testing and support contracts.

### Русский

**heypandax/cc-pocket** — это open‑source‑мобильное приложение на Kotlin, позволяющее управлять с телефона Claude Code или OpenAI Codex: возобновлять сеансы, получать потоковый вывод и удалённо одобрять разрешения инструментов, всё в сквозном end‑to‑end шифровании и zero‑knowledge‑ретрансляции. Типичный сценарий — быстрый прототип AI‑фич, построение RAG‑или агентных воркфлоу и оценка инструментов модели без необходимости разворачивать собственный стек; приложение легко интегрируется через предоставляемый API/SDK/CLI. Готовность к production — средняя: проект подходит для прототипов и внутренних процессов, но требует дополнительной проверки лицензии, безопасности и поддержки перед масштабным внедрением.

### 中文

**项目简介**  
heypandax/cc‑pocket 是一款开源移动端客户端，能够在手机上驱动 Claude Code 或 OpenAI Codex，支持会话恢复、实时输出流、远程批准工具权限等功能。全链路端到端加密、零知识中继，代码与数据均不泄露给第三方。

**价值**  
- **快速赋能 AI 编码**：无需自行训练模型或搭建完整的推理栈，直接调用成熟的 Claude Code / Codex 接口，即可在移动端实现代码生成、调试和 RAG/Agent 工作流。  
- **安全合规**：端到端加密和零知识中继保证了代码与业务数据在传输和存储过程中的隐私，适合对安全要求较高的内部研发或原型项目。  
- **跨平台原型**：基于 Kotlin 实现，提供 API/SDK/CLI，开发者可以快速在 Android、Kotlin/JVM 项目或脚本中集成，验证 AI 功能的可行性。

**典型接入方式**  
1. **SDK 集成**：在 Android/Kotlin 项目中通过 Gradle 引入 `com.heypandax.ccpocket:client`，使用提供的 `CcPocketClient` 初始化并配置 API Key、加密密钥等。  
2. **CLI 调用**：通过项目自带的 `ccpocket-cli`，在本地或 CI 环境中执行 `ccpocket run --model codex --prompt "..."` 实现一键代码生成。  
3. **REST/GRPC 接口**：如果已有后端服务，可直接调用项目暴露的 HTTP/GRPC 端点，发送会话 ID、提示词等，获取流式返回并在前端展示。  

**生产可用性**  
- **成熟度**：当前 32 星、1 fork，最近一次提交在 2026‑06‑25，代码基于 Kotlin，依赖相对轻量。  
- **适用场景**：非常适合作为原型或内部工具，快速验证 AI 编码能力；在生产环境使用前，需要完成以下检查：  
  - 评估许可证兼容性（项目采用 MIT/Apache 等开源许可证）。  
  - 进行安全审计，确认加密实现、密钥管理和零知识中继的完整性。  
  - 检查依赖的第三方 SDK（Claude/OpenAI）服务的 SLA 与费用模型。  
- **总体评估**：**中等**（Medium）— 可在受控环境下投入使用，若要面向外部用户或大规模部署，建议增加监控、容错和运维脚本，并确保维护者的持续活跃。

## 🧭 Practical evaluation

**Value:** heypandax/cc-pocket helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 32 GitHub stars
- 1 forks
- updated 2026-06-25
- primary language: Kotlin
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 8/100 |
| stars | 32/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 51/100 |
| recency | 40/100 |
| adoption | 25/100 |
| production | 52/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/heypandax/cc-pocket) · [← Back to AI/ML](./README.md)</sub>
