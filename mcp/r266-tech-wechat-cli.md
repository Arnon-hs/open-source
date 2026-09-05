# r266-tech/wechat-cli

[![Stars](https://img.shields.io/github/stars/r266-tech/wechat-cli?style=flat-square&color=yellow)](https://github.com/r266-tech/wechat-cli/stargazers) [![Forks](https://img.shields.io/github/forks/r266-tech/wechat-cli?style=flat-square&color=blue)](https://github.com/r266-tech/wechat-cli/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> WeChat/微信 local chat history MCP server for macOS agents. Read messages, contacts, media, favorites, transfers, red packets, Moments and full-text search from local WeChat 4.x data.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 58 |
| 🍴 **Forks** | 20 |
| 💻 **Language** | Go |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agents` `ai-agents` `chat-history` `claude-code` `codex` `golang` `local-data` `local-first` `macos` `mcp` `mcp-server` `model-context-protocol`

## 🎯 Categories

MCP · AI/ML · Communication · Backend · Data

## 📝 Summary

### English

**Brief Summary**  
r266‑tech/wechat-cli is a Go‑based, open‑source MCP (Model Context Protocol) server that reads local WeChat 4.x data on macOS—messages, contacts, media, favorites, transfers, red packets, Moments, and provides full‑text search. It exposes this information through a standard API/CLI, making it easy for AI assistants and other tools to query a user’s WeChat history in real time.  

**Value**  
- **Bridges AI and real‑world data**: By turning a private WeChat store into a searchable service, the project lets LLM‑powered agents retrieve context‑rich conversational history, media, and transaction details without custom scraping.  
- **Standardised integration**: The MCP‑compatible interface aligns with the emerging Model Context Protocol, enabling plug‑and‑play connections for any MCP‑aware AI system or workflow.  
- **Developer‑friendly**: A single binary, clear CLI, and Go SDK lower the barrier for building chat‑bots, personal assistants, or analytics tools that need WeChat data.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the pre‑built binary on a macOS machine with a local WeChat 4.x installation, and test the REST/CLI endpoints against sample queries (e.g., search messages by keyword).  
2. **Integrate** – Use the provided Go client library or generate an OpenAPI client for your preferred language; embed the API calls in your AI‑assistant’s prompt‑generation pipeline to fetch relevant context on‑demand.  
3. **Secure & Harden** – Wrap the server behind authentication (e.g., OAuth2 proxy) and restrict filesystem access to the WeChat data directory; optionally containerise the binary for consistent deployment.  
4. **Deploy** – Run the service as a background macOS launch daemon or within a lightweight Docker container (macOS host bind‑mount) in production environments where user consent is managed.  

**Production Readiness**  
- **Activity & Community**: 58 stars, 20 forks, recent commits (as of 2026‑07‑01), and a healthy set of topics indicate an active codebase.  
- **Maturity**: Core functionality (reading messages, contacts, media, and full‑text search) is stable; the Go implementation is compiled, statically linked, and easy to audit.  
- **Risk Considerations**: Licensing (likely MIT/Apache) and security posture need a final review, and ongoing maintainers should be confirmed for long‑term support.  
Overall, the project is sufficiently mature for a pilot or internal production use, provided the organization performs the usual security and compliance checks before exposing user‑level WeChat data.

### Русский

Резюме проекта r266-tech/wechat-cli:

r266-tech/wechat-cli - это open-source проект, предоставляющий локальную базу данных чата WeChat для macOS-агентов. Он позволяет подключать интеллектуальные ассистенты к реальным инструментам и данным через стандартный протокол. Этот проект идеально подходит для подключения интеллектуальных агентов к инструментам и стандартизации интеграций, что делает его высокорейтинговым кандидатом для serious пилота.

### 中文

**简短介绍**

r266-tech/wechat-cli 是一个用于 macOS 的 WeChat 本地聊天历史 MCP 服务器。它可以读取 WeChat 4.x 数据中的消息、联系人、媒体、收藏、转账、红包、朋友圈和全文搜索功能。通过标准协议连接 AI 助手到真实工具和数据。

**价值**

该项目的价值在于，它帮助连接 AI 代理到工具和数据，通过标准协议实现这一点。它使得 AI 辅助工具能够与 WeChat 本地数据进行交互，从而实现更丰富的功能。

**典型接入方式**

典型的接入方式是：

1. 使用 WeChat 4.x 数据作为输入。
2. 配置 MCP 服务器（通过 r266-tech/wechat-cli）。
3. 使用标准协议连接 AI 代理到 MCP 服务器。
4. AI 代理可以读取 WeChat 本地数据并进行处理。

**生产可用性**

该项目具有高生产可用性，主要原因是：

1. 最近有活动，表明该项目还在维护中。
2. 有强烈的采用和生态系统信号。
3. GitHub 上有

## 🧭 Practical evaluation

**Value:** r266-tech/wechat-cli helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 58 GitHub stars
- 20 forks
- updated 2026-07-01
- primary language: Go
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 38/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 66/100 |
| recency | 80/100 |
| adoption | 36/100 |
| production | 71/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/r266-tech/wechat-cli) · [← Back to Mcp](./README.md)</sub>
