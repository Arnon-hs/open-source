# aeroxy/chrome-devtools-cli

[![Stars](https://img.shields.io/github/stars/aeroxy/chrome-devtools-cli?style=flat-square&color=yellow)](https://github.com/aeroxy/chrome-devtools-cli/stargazers) [![Forks](https://img.shields.io/github/forks/aeroxy/chrome-devtools-cli?style=flat-square&color=blue)](https://github.com/aeroxy/chrome-devtools-cli/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> A high-performance, developer and agent friendly CLI for interacting with Chrome via the DevTools Protocol (CDP).

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 225 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | Rust |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Summary**  
`aeroxy/chrome-devtools-cli` is a Rust‑based command‑line tool that lets developers and AI agents drive Chrome through the Chrome DevTools Protocol (CDP) with high performance and a simple interface. It is positioned as a shortcut for adding browser‑automation capabilities to AI/ML workflows—such as prototype RAG pipelines or agent‑driven browsing—without building a CDP stack from scratch.  

**Value**  
- **Fast, low‑overhead access to Chrome**: By wrapping CDP in a native CLI, the project eliminates the latency and complexity of HTTP‑based wrappers, making it suitable for real‑time AI agents that need to fetch or render web content.  
- **AI‑centric integration**: The tool can be invoked from scripts, LangChain agents, or other model orchestration frameworks, enabling quick prototyping of “browse‑the‑web” capabilities, data extraction, or UI testing without writing custom CDP code.  
- **Open‑source and language‑agnostic**: Although written in Rust, the CLI can be called from any language, lowering the barrier for teams that already use Python, Node, or other stacks.  

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided README examples, and verify that the CLI can launch Chrome, navigate pages, and capture screenshots or DOM data for a simple use case (e.g., fetching a page title).  
2. **Integration layer** – Wrap the CLI calls in a thin wrapper (Python subprocess, Bash script, or Docker entrypoint) that your AI agent or workflow engine can invoke.  
3. **Iterative feature addition** – Extend the wrapper with the specific CDP commands you need (network interception, JS evaluation, etc.) and test against your target URLs.  
4. **Security & compliance check** – Review the MIT/Apache license (as listed in the repo), scan the binary for known vulnerabilities (e.g., using `cargo audit`), and lock the dependency versions.  

**Production Readiness**  
- **Maturity**: Medium. The project has 225 stars and recent activity (last commit 2026‑06‑27), indicating an active codebase, but the contributor count is low (8 forks) and long‑term maintainers are not clearly identified.  
- **Reliability**: Suitable for internal tools, prototypes, or bounded production workloads where occasional updates can be vetted.  
- **Risks**: Requires a final review of licensing, security posture of the Rust dependencies, and a plan for handling breaking changes in Chrome’s CDP. With those checks and a small‑scale rollout, the CLI can be promoted to production for non‑critical browser‑automation tasks.

### Русский

**Краткое резюме:**  
`aeroxy/chrome-devtools-cli` — это быстрый и удобный CLI‑инструмент на Rust для работы с Chrome через DevTools Protocol, позволяющий легко добавить AI‑функциональность (например, RAG‑подсказки или агентные сценарии) без построения собственного стека. Типичный путь внедрения — запуск небольшого proof‑of‑concept, проверка README и базовых команд, после чего можно интегрировать в прототипы или внутренние пайплайны. Проект находится на среднем уровне готовности к production: имеет 225 звёзд, активные обновления и простую зависимостную структуру, но требует окончательной проверки лицензии, безопасности и поддержки перед масштабным использованием.

### 中文

**项目简介**  
aeroxy/chrome‑devtools‑cli 是一款基于 Rust 实现的高性能命令行工具，能够直接通过 Chrome DevTools Protocol（CDP）与 Chrome 浏览器交互。它面向开发者和 AI/Agent 场景，提供快速、脚本化的浏览器控制能力。

**价值**  
- **即插即用的 AI 能力**：无需自行搭建 CDP 客户端或维护复杂的浏览器自动化框架，直接在 CLI 中调用即可为 AI 模型提供网页抓取、渲染快照、交互等底层数据。  
- **高效原型开发**：在 RAG、Agent 工作流或模型评估中，能够快速获取最新的网页内容或执行 JavaScript，帮助模型获取实时上下文。  
- **跨语言友好**：作为独立的可执行文件，可在任何支持系统调用的语言（Python、Node、Bash 等）中轻松调用，降低集成成本。

**典型接入方式**  
1. **安装**：`cargo install chrome-devtools-cli` 或下载预编译二进制。  
2. **启动 Chrome（或 Chrome‑Headless）** 并打开远程调试端口，例如 `chrome --headless --remote-debugging-port=9222`。  
3. **在脚本中调用**：  
   ```bash
   # 获取页面 DOM
   chrome-devtools-cli --port 9222 --url https://example.com --cmd "DOM.getDocument"
   
   # 截图
   chrome-devtools-cli --port 9222 --url https://example.com --cmd "Page.captureScreenshot"
   ```  
   在 Python 中可以使用 `subprocess.run([...])` 捕获输出并喂给模型。  
4. **与 AI 框架结合**：将 CLI 输出（JSON、Base64 图片等）作为提示或检索文档，构建 RAG/Agent 流程。

**生产可用性**  
- **成熟度**：已有 225+ ⭐、8+ forks，最近一次更新在 2026‑06‑27，表明项目仍在活跃维护。  
- **适用场景**：非常适合作为原型或内部工具，用于快速获取网页信息、自动化交互或生成训练数据。  
- **上线注意事项**：  
  - **依赖审计**：检查 Rust 依赖的许可证（MIT/Apache）以及是否存在已知安全漏洞。  
  - **稳定性**：在生产环境建议使用固定的二进制版本或 Docker 镜像，避免因上游更新导致行为变化。  
  - **监控与容错**：对 Chrome 启动、端口占用以及 CLI 调用的返回码进行监控，必要时实现重试或回退机制。  
- **总体评估**：在做好依赖安全审查和容错设计后，可在内部服务或受控的生产环境中使用；对外部高可用服务仍需进一步评估其长线维护和社区支持情况。

## 🧭 Practical evaluation

**Value:** aeroxy/chrome-devtools-cli helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 225 GitHub stars
- 8 forks
- updated 2026-06-27
- primary language: Rust

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 50/100 |
| topics | 0/100 |
| outlook | 67/100 |
| quality | 54/100 |
| recency | 80/100 |
| adoption | 43/100 |
| production | 62/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/aeroxy/chrome-devtools-cli) · [← Back to DevTools](./README.md)</sub>
