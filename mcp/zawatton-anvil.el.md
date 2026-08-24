# zawatton/anvil.el

[![Stars](https://img.shields.io/github/stars/zawatton/anvil.el?style=flat-square&color=yellow)](https://github.com/zawatton/anvil.el/stargazers) [![Forks](https://img.shields.io/github/forks/zawatton/anvil.el?style=flat-square&color=blue)](https://github.com/zawatton/anvil.el/network) [![Language](https://img.shields.io/badge/lang-Emacs%20Lisp-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> An MCP server written in Elisp — a token-efficient workbench for AI agents. Drives files, org-mode, Elisp & SQLite from any MCP client   (Claude, GPT, local LLMs) through Emacs primitives instead of sed/grep round-trips.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 73 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | Emacs Lisp |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

MCP · Database

## 📝 Summary

### English

**Summary**  
*zawatton/anvil.el* is an Emacs‑Lisp implementation of an MCP (Model Context Protocol) server that lets AI agents interact directly with files, Org‑mode documents, SQLite databases, and other Emacs primitives, avoiding costly sed/grep round‑trips. It provides a token‑efficient workbench for connecting Claude, GPT, or local LLMs to real‑world tooling through a standard protocol.  

**Value**  
By exposing Emacs’s rich editing and data‑access capabilities as MCP endpoints, Anvil eliminates the “prompt‑only” limitation of most LLM integrations and lets agents read, write, and query native data structures (e.g., Org trees, SQLite tables) with far fewer tokens. This dramatically reduces latency and cost while enabling more precise, context‑aware tool use—ideal for prototyping AI‑augmented workflows, building custom assistants, or exposing internal knowledge bases to external models.  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run `M-x anvil-start-server` inside Emacs, and point a local MCP client (e.g., Claude’s MCP client or a self‑hosted LLM) at `localhost:PORT`. Verify basic commands like reading a file or querying an Org agenda.  
2. **Read the README** – Follow the quick‑start instructions, configure the optional SQLite connector, and test with a minimal Emacs init to ensure no conflicting packages.  
3. **Integrate** – Wrap the server start‑up in your CI pipeline or Docker image, expose the MCP port, and replace ad‑hoc shell scripts with MCP calls from your AI agents.  
4. **Scale & Harden** – Add authentication (e.g., token‑based or TLS), monitor resource usage, and pin the Emacs version to avoid breaking changes.  

**Production readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑06‑26) and has modest community traction (≈70 ★, 9 forks). It is stable enough for internal prototypes and low‑risk production use.  
- **Dependencies**: Pure Emacs‑Lisp plus optional SQLite bindings; no heavyweight external services, which simplifies deployment.  
- **Risks**: The license and security posture need a final check, and long‑term maintainer commitment is unclear. Before production, conduct a security audit, lock dependency versions, and establish a fallback plan (e.g., self‑hosted MCP server).  

Overall, Anvil.el offers a compelling, token‑efficient bridge between LLMs and real tools, with a straightforward integration path and sufficient stability for internal workflows, provided the usual due‑diligence steps are taken before full production rollout.

### Русский

**zawatton/anvil.el** — это open‑source MCP‑сервер, написанный на Emacs Lisp, который позволяет AI‑агентам (Claude, GPT, локальные LLM) управлять файлами, org‑mode, Elisp‑кодом и SQLite через единый протокол Model Context Protocol, обходя громоздкие вызовы sed/grep. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept сервера в Emacs, подключение к нему нужного AI‑клиента и построение прототипов интеграций «AI ↔ инструменты/данные». Готовность к production — средняя: проект уже стабилен для прототипов и внутренних воркфлоу (73 ★, активные коммиты), но перед запуском в продакшн требуется проверка лицензии, безопасности и наличие обслуживающего мейнтейнера.

### 中文

**项目简介**  
zawatton/anvil.el 是用 Emacs Lisp 编写的 MCP（Model Context Protocol）服务器。它在 Emacs 环境中提供了一个高效的工作台，能够让 Claude、GPT、国产 LLM 等任意 MCP 客户端直接操作文件、org‑mode、Elisp 代码以及 SQLite 数据库，而无需通过 sed/grep 等外部工具的往返。

**价值**  
- **标准化桥接**：通过 MCP 将 AI 助手与真实的开发工具和数据源统一对接，避免了各类“自研 API”导致的碎片化。  
- **低开销**：所有操作均基于 Emacs 原生 primitive，省去中间层的序列化/反序列化和子进程开销，尤其适合 token‑敏感的 LLM 场景。  
- **即插即用**：只要在 Emacs 中加载 anvil.el，即可把本地文件系统、org‑mode 知识库、Elisp 代码执行环境以及 SQLite 视作统一的“工具集合”，让 AI 能够像人类一样直接使用。

**典型接入方式**  
1. **准备环境**：在目标机器上安装 Emacs（≥ 27）并克隆仓库。  
2. **启动服务器**：在 Emacs 中 `M-x anvil-start-server`（或在 init.el 中调用 `(anvil-start-server :port 12345)`），服务器会监听指定的 MCP 端口。  
3. **配置客户端**：在 Claude、OpenAI‑compatible SDK、或本地 LLM 的 MCP 客户端中指向 `localhost:1234`（端口可自定义），并声明需要的工具集合（如 `file`, `org`, `sqlite`）。  
4. **验证**：发送一个简单的 MCP 请求（如读取 `README.org`），确认返回的内容即为 Emacs 读取的结果。  
5. **迭代**：根据业务需求在 `anvil-config.el` 中添加自定义 Elisp 命令或 SQLite 表，随后在 MCP 请求中直接调用。

**生产可用性**  
- **成熟度**：GitHub 目前 73 星、9 叉，最近一次提交为 2026‑06‑26，代码质量基本稳定，适合作为原型或内部工具。  
- **依赖**：唯一依赖是 Emacs 本身及其内置的 SQLite 库，部署成本低。  
- **风险点**  
  - **维护者活跃度**：项目维护者不多，长期维护需要自行跟进 PR 或 fork。  
  - **安全审计**：由于服务器会执行任意 Elisp 代码，建议在受信网络或沙箱环境中运行，并对外部 MCP 客户端进行身份验证（可自行在 `anvil-auth.el` 中实现）。  
  - **许可证**：请确认仓库的 LICENSE（默认 GPL‑3.0）是否符合贵公司合规要求。  
- **上线建议**：先在开发/测试环境做一个“小型 PoC”，验证 AI 与文件/数据库交互的正确性与安全边界；随后在 CI 中加入自动化测试（启动 anvil、发送标准 MCP 请求、检查返回），再逐步推广到生产环境。

综上，zawatton/anvil.el 为把 AI 助手接入真实开发工具提供了一个轻量且统一的方案，适合原型开发和内部工作流的快速落地；在生产环境使用时，需要自行加强安全防护并做好维护计划。

## 🧭 Practical evaluation

**Value:** zawatton/anvil.el helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 73 GitHub stars
- 9 forks
- updated 2026-06-26
- primary language: Emacs Lisp

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 40/100 |
| topics | 0/100 |
| outlook | 51/100 |
| quality | 41/100 |
| recency | 40/100 |
| adoption | 36/100 |
| production | 50/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/zawatton/anvil.el) · [← Back to Mcp](./README.md)</sub>
