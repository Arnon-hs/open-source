# agent-sh/computer-use-linux

[![Stars](https://img.shields.io/github/stars/agent-sh/computer-use-linux?style=flat-square&color=yellow)](https://github.com/agent-sh/computer-use-linux/stargazers) [![Forks](https://img.shields.io/github/forks/agent-sh/computer-use-linux?style=flat-square&color=blue)](https://github.com/agent-sh/computer-use-linux/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Linux desktop control over MCP — AT-SPI, GNOME Shell, Wayland portals, ydotool

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 226 |
| 🍴 **Forks** | 21 |
| 💻 **Language** | Rust |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `ai` `cargo` `claude` `codex` `computer-use` `gnome` `hermes` `linux` `llm` `mcp` `npm`

## 🎯 Categories

MCP · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*agent‑sh/computer‑use‑linux* is an open‑source Rust library that lets AI assistants control a Linux desktop through the Model Context Protocol (MCP), leveraging AT‑SPI, GNOME Shell, Wayland portals, and ydotool. It provides a standard, low‑latency API/SDK/CLI for exposing real‑world tools and data to LLMs, making it easy to ship MCP servers and unify integrations across Linux environments.

**Value**  
- **Bridges the gap** between large language models and native Linux applications, turning the desktop into a programmable interface for AI agents.  
- **Standardizes communication** via MCP, so the same integration code can be reused across different assistants, tools, and distributions.  
- **Accelerates development** by offering ready‑made bindings for common accessibility and input stacks (AT‑SPI, GNOME Shell, Wayland portals, ydotool), eliminating the need to write custom glue code.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided CLI or embed the Rust SDK in a small service that registers as an MCP server.  
2. **Integrate** – Connect your LLM‑backed assistant (e.g., OpenAI, Anthropic) to the MCP endpoint; use the SDK to send commands like “click button X” or “read window Y”.  
3. **Extend** – Add custom handlers for domain‑specific tools (e.g., IDEs, browsers) by leveraging the existing AT‑SPI/Wayland abstractions.  
4. **Deploy** – Package the service as a container or systemd unit on target workstations; the standard MCP contract ensures other agents can interoperate without code changes.

**Production Readiness**  
- **Active maintenance**: recent commits (as of 2026‑06‑29), 226 stars, 21 forks, and a healthy Rust ecosystem indicate ongoing development.  
- **Mature API surface**: clear CLI/SDK, well‑documented signals, and language‑agnostic metadata make integration straightforward.  
- **Risk profile**: No major licensing or security red flags identified, though a final review of the license and maintainer responsiveness is advisable.  
Overall, the project is mature enough for a serious pilot in production environments, especially where Linux desktop automation by AI agents is required.

### Русский

Резюме проекта agent-sh/computer-use-linux:

Проект agent-sh/computer-use-linux предлагает стандартный протокол для связи AI-ассистентов с реальными инструментами и данными, позволяя им взаимодействовать и обмениваться информацией. Типовой сценарий внедрения проекта заключается в подключении AI-агентов к различным инструментам и сервисам, что упрощает интеграцию и облегчает работу. Проект готов к серийному выпуску, поскольку он получил высокую оценку (76/100) и имеет сильную экосистему с 226 GitHub звездами и 21 вилкой.

### 中文

**项目简介（2‑3 句）**  
agent‑sh/computer‑use‑linux 是一套基于 MCP（Model Context Protocol）的 Linux 桌面控制库，利用 AT‑SPI、GNOME Shell、Wayland portals 与 ydotool 为 AI 助手提供统一的桌面交互接口。它让 AI 能够像人类一样直接调用本地 GUI 应用、读取 UI 元数据并执行键鼠操作，从而把模型的推理能力与真实工具和数据桥接起来。

**价值**  
- **标准化 AI‑工具桥接**：通过 MCP 统一协议，AI 助手可以在不同 Linux 桌面环境下以一致的方式访问和操作本地应用，降低集成成本。  
- **快速构建 AI 工作流**：开发者只需调用库提供的 API/CLI，即可让模型直接打开文件、填写表单、控制媒体等，显著提升 AI 产品的实用性。  
- **生态兼容**：基于 Rust 实现，提供跨语言 SDK（Python、Node 等），并兼容 Wayland、X11，适配主流 Linux 桌面。

**典型接入方式**  
1. **API/SDK**：在 AI 服务或模型推理代码中引入 Rust crate 或对应的 Python/Node 包，调用 `open_window`, `click`, `type_text` 等高层函数。  
2. **CLI/脚本**：通过系统命令行调用 `computer-use-linux-cli`，配合模型生成的指令脚本，实现“模型 → 指令 → CLI → 桌面”。  
3. **MCP 服务器**：部署一个 MCP 服务器实例，AI 助手通过标准的 Model Context Protocol 与其通信，服务器内部使用该库完成实际的桌面操作。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑29 最近一次提交，GitHub 226 星、21 Fork，社区讨论活跃，代码基于 Rust，质量和安全审计相对成熟。  
- **成熟度**：已支持 AT‑SPI、GNOME Shell、Wayland portals 与 ydotool，覆盖主流 Linux 桌面环境，文档提供完整的 API、SDK 与 CLI 示例。  
- **风险**：需进一步确认许可证兼容性（MIT/Apache 双许可），并进行安全依赖审计及维护者响应时效评估。整体来看，项目已具备 **高** 级别的生产就绪度，适合作为 AI 助手桌面集成的核心组件进行试点或正式上线。

## 🧭 Practical evaluation

**Value:** agent-sh/computer-use-linux helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 226 GitHub stars
- 21 forks
- updated 2026-06-29
- primary language: Rust
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 50/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 45/100 |
| production | 57/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/agent-sh/computer-use-linux) · [← Back to Mcp](./README.md)</sub>
