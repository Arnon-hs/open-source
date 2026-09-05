# Regsorm/code-index-mcp

[![Stars](https://img.shields.io/github/stars/Regsorm/code-index-mcp?style=flat-square&color=yellow)](https://github.com/Regsorm/code-index-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/Regsorm/code-index-mcp?style=flat-square&color=blue)](https://github.com/Regsorm/code-index-mcp/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> Rust-native code index MCP server with first-class 1C:Enterprise (BSL) support. Static binary, no runtime. 31 tools — 20 universal + 11 BSL-specific. Tree-sitter AST for 10 languages. Federation across multiple repos. Built for production-scale monorepos.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 77 |
| 🍴 **Forks** | 10 |
| 💻 **Language** | Rust |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`1c-enterprise` `ast` `bsl` `code-index` `code-search` `developer-tools` `mcp` `model-context-protocol` `onescript` `rust` `tree-sitter`

## 🎯 Categories

MCP · DevTools

## 📝 Summary

### English

**Project Summary:**
Regsorm/code-index-mcp is an open-source, Rust-native code index server that supports 1C:Enterprise (BSL) and provides a standard protocol for connecting AI assistants to real tools and data. It offers 31 tools, including 20 universal and 11 BSL-specific, with a tree-sitter AST for 10 languages. The project enables federation across multiple repos and is built for production-scale monorepos.

**Value Proposition:**
The main value of Regsorm/code-index-mcp lies in its ability to standardize integrations between AI assistants and real tools and data. By providing a standard protocol, developers can easily connect their AI agents to tools, making it a crucial component for building intelligent systems.

**Practical Adoption Path:**
To adopt Regsorm/code-index-mcp, developers can follow these steps:

1. Evaluate the project's implementation signals, such as API/SDK/CLI, language metadata, or focused topics.
2. Review the project's documentation and example use cases to understand its capabilities and limitations.
3. Integrate the project into their existing workflow, starting with a prototype or internal project.
4. Monitor the project's dependency and maintenance checks to ensure production readiness.

**Production Readiness:**
Regsorm/code

### Русский

Regsorm/code-index-mcp — это высокопроизводительный сервер индекса кода на Rust с нативной поддержкой 1C:Enterprise (BSL) и статическим бинарником без внешних зависимостей. Он позволяет быстро подключать AI‑ассистентов к реальным инструментам и данным через стандартный Model Context Protocol, предоставляя 31 инструмент (20 универсальных + 11 BSL‑специфичных) и Tree‑sitter AST для 10 языков, а также федерацию индексов в нескольких репозиториях, что удобно для монорепозиториев production‑уровня. Проект находится на среднем уровне готовности: подходит для прототипов и внутренних workflow, но перед выводом в продакшн требуется проверка лицензии, безопасности и активности мейнтейнеров.

### 中文

**项目简介**  
Regsorm/code-index-mcp 是一款基于 Rust 的代码索引 MCP（Model Context Protocol）服务器，原生支持 1C:Enterprise（BSL）语言。它以单文件静态二进制交付，无需运行时依赖，内置 31 套工具（20 套通用工具 + 11 套 BSL 专用），并提供 10 种语言的 Tree‑sitter AST，支持跨仓库联邦查询，专为大规模单体仓库设计。

**价值**  
- **AI‑工具桥梁**：通过标准化的 MCP 接口，AI 助手可以直接查询、分析和操作真实代码库和元数据，实现“代码即上下文”。  
- **统一化集成**：一次部署即可为多语言、多仓库提供统一的代码索引与查询服务，减少各类语言的碎片化实现。  
- **高性能、零运行时**：Rust 编译的静态二进制体积小、启动快，适合作为内部服务或边缘节点运行。

**典型接入方式**  
1. **API/SDK**：启动服务器后，使用 HTTP/JSON 或 gRPC 接口（符合 MCP 规范）进行查询；项目提供了 Rust、Python、Node.js 等语言的 SDK 示例。  
2. **CLI**：通过自带的命令行工具直接在终端执行索引、搜索、AST 导出等操作，适合脚本化集成。  
3. **模型上下文协议**：将服务器地址配置到支持 MCP 的大模型（如 OpenAI、Claude）或自研的 AI Agent，即可让模型在对话中实时获取代码上下文。

**生产可用性**  
- **成熟度**：当前评分 66/100，GitHub 77 星、10 Fork，最近一次提交为 2026‑07‑01，代码基于 Rust，具备较好的性能和安全基线。  
- **适用场景**：非常适合内部原型、研发工具链、或在受控环境下的生产级单体仓库；在正式生产环境使用前建议完成以下检查：  
  - 许可证合规（确认与公司政策兼容）  
  - 安全审计（审查依赖的第三方 crate）  
  - 维护者活跃度（确保后续 bug 修复和功能迭代）  
- **部署成本**：只需下载单一二进制文件，配置好仓库路径和网络端口即可运行，几乎没有运行时依赖，运维成本低。

综上，Regsorm/code-index-mcp 为 AI 与真实代码资产的交互提供了高效、统一的桥接层，接入方式灵活，适合作为内部研发平台的代码索引后端，在完成必要的合规与安全审查后即可投入生产使用。

## 🧭 Practical evaluation

**Value:** Regsorm/code-index-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 77 GitHub stars
- 10 forks
- updated 2026-07-01
- primary language: Rust
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 26/100 |
| stars | 40/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 66/100 |
| recency | 80/100 |
| adoption | 36/100 |
| production | 67/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/Regsorm/code-index-mcp) · [← Back to Mcp](./README.md)</sub>
