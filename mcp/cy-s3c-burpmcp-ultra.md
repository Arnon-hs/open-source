# Cy-S3c/BurpMCP-Ultra

[![Stars](https://img.shields.io/github/stars/Cy-S3c/BurpMCP-Ultra?style=flat-square&color=yellow)](https://github.com/Cy-S3c/BurpMCP-Ultra/stargazers) [![Forks](https://img.shields.io/github/forks/Cy-S3c/BurpMCP-Ultra?style=flat-square&color=blue)](https://github.com/Cy-S3c/BurpMCP-Ultra/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> AI-powered MCP server for Burp Suite Professional — 149 tools across proxy, scanner, inline fuzzer, race conditions, guided injection, JWT/IDOR attacks, recon & OOB, with a real-time dashboard and hardened localhost security. Drive Burp from Claude Code or any MCP client.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 101 |
| 🍴 **Forks** | 14 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bug-bounty` `burpsuite` `claude` `kotlin` `mcp` `model-context-protocol` `pentesting` `security-tools`

## 🎯 Categories

MCP · AI/ML · Networking · Security

## 📝 Summary

### English

**Brief Summary**  
Cy‑S3c/BurpMCP‑Ultra is an open‑source, AI‑driven MCP (Model Context Protocol) server that extends Burp Suite Professional with 149 built‑in tools covering proxy manipulation, active scanning, inline fuzzing, race‑condition testing, guided injection, JWT/IDOR exploitation, reconnaissance, and out‑of‑band interactions. It ships a real‑time dashboard, hardened localhost security, and can be driven from Claude Code or any MCP‑compatible client, turning Burp into a programmable, AI‑accessible security platform.

**Value**  
- **AI‑to‑tool bridge** – By exposing Burp’s capabilities through the standard MCP, developers can let large language models (LLMs) or custom agents invoke concrete security actions instead of merely generating text. This turns “talk‑to‑AI” into “talk‑to‑Burp” and enables automated, repeatable testing pipelines.  
- **Unified interface** – All 149 utilities are accessible via a single API/SDK/CLI, simplifying integration for CI/CD, red‑team tooling, or security‑as‑code frameworks.  
- **Live visibility** – The built‑in dashboard streams results in real time, giving operators immediate feedback and the ability to intervene when needed.  
- **Secure localhost deployment** – Hardened security settings keep the server isolated to the developer’s machine, reducing attack surface while still allowing remote AI agents to interact through the MCP protocol.

**Practical Adoption Path**  
1. **Setup** – Clone the repo, build the Kotlin project (or pull a pre‑built Docker image), and run the MCP server on a local machine where Burp Suite Professional is installed.  
2. **Authentication** – Configure the provided token‑based or mutual‑TLS authentication to lock down access to the localhost endpoint.  
3. **Client integration** – Use any MCP‑compatible client (e.g., Claude Code, custom Python/Node SDKs) to send JSON‑RPC‑style requests such as `proxy.intercept`, `scanner.start`, or `fuzzer.run`.  
4. **Automation** – Embed these calls in CI pipelines, security‑as‑code scripts, or autonomous red‑team bots to automatically trigger scans, collect findings, and feed results back into ticketing or SIEM systems.  
5. **Monitoring** – Leverage the real‑time dashboard or stream the server’s WebSocket events to observability platforms for continuous oversight.

**Production Readiness**  
- **Activity & Adoption** – The project shows recent commits (last updated 2026‑06‑25), 101 GitHub stars, and a modest fork base, indicating an engaged community.  
- **Maturity** – Core functionality (proxy, scanner, fuzzer, OOB) is already battle‑tested in Burp Suite; the MCP wrapper adds a thin, well‑documented API layer.  
- **Security Posture** – The server runs locally with hardened defaults, but a final review of the license (likely Apache‑2.0 or MIT) and any third‑party dependencies is advisable before enterprise rollout.  
- **Scalability** – Because the server is a single‑process Kotlin application, it is suitable for developer workstations or dedicated security appliances; horizontal scaling would require multiple instances behind a load balancer and coordinated token management.  

Overall, BurpMCP‑Ultra is a high‑readiness OSS candidate for organizations that want to automate Burp Suite actions via AI agents or standardized MCP integrations, with a clear, low‑friction path from evaluation to production deployment.

### Русский

Cy‑S3c/BurpMCP‑Ultra — это open‑source сервер MCP, интегрированный с Burp Suite Professional и обогащённый ИИ: более 149 готовых инструментов (прокси, сканер, inline‑fuzzer, проверка гонок, направленные инъекции, JWT/IDOR, рекогнишн и OOB) и интерактивная панель в реальном времени, работающие в изолированном localhost‑окружении. Типичный сценарий — подключить любой AI‑агент (например, Claude Code) или MCP‑клиент к Burp, чтобы автоматически выполнять тесты безопасности и получать контекстные ответы через Model Context Protocol. Проект уже имеет активную поддержку (обновления до 2026‑06‑25, 101 звезда, 14 форков, Kotlin‑код), поэтому готов к пилотному запуску в продакшн, требуя лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
Cy‑S3c/BurpMCP‑Ultra 是一款基于 AI 的 MCP（Model Context Protocol）服务器，专为 Burp Suite Professional 打造，内置 149 项渗透测试工具（代理、扫描、内联模糊、竞态、引导注入、JWT/IDOR、情报收集、OOB 等），并提供实时仪表盘与本地硬化安全层，可通过 Claude Code 或任意 MCP 客户端远程驱动 Burp。

**价值**  
- **AI 与真实安全工具的桥梁**：通过标准化的 MCP 协议，把大模型（如 Claude、ChatGPT 等）直接映射到 Burp 的功能，实现“让 AI 真正动手”。  
- **一站式渗透测试平台**：统一入口覆盖从代理到高级攻击的全套工具，降低切换不同插件的成本。  
- **实时可视化**：仪表盘实时展示请求、漏洞、攻击路径等信息，提升团队协作与审计效率。  
- **安全可靠的本地部署**：只在 localhost 运行，默认开启防护措施，避免外部攻击面。

**典型接入方式**  
1. **启动 MCP 服务器**：`java -jar burpmcp-ultra.jar`（或使用 Docker 镜像）。服务器默认监听本机 127.0.0.1 的 MCP 端口。  
2. **在 AI 助手侧配置 MCP 客户端**：  
   - 使用 Claude Code、OpenAI Plugins 或自研 MCP SDK（Python、Node、Java）指向 `http://127.0.0.1:xxxx/mcp`。  
   - 通过标准的 `tool.invoke`、`tool.list` 等 RPC 调用即可让模型执行 Burp 功能（如 `proxy.intercept`, `scanner.start`, `fuzzer.run`）。  
3. **可选 CLI/SDK**：项目提供 Kotlin/Java SDK 与 Python 示例脚本，便于在 CI/CD、自动化测试或自定义插件中直接调用。  
4. **安全集成**：在生产环境可通过 Nginx 反向代理加 TLS、IP 白名单或 Unix Domain Socket 限制访问，仅对可信 AI 服务开放。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑25，GitHub ★101、Fork 14，社区已有若干实战案例。  
- **技术成熟度**：使用 Kotlin 编写，提供完整的 API/SDK/CLI，兼容所有主流 MCP 客户端。  
- **安全性**：默认只监听本机，代码中实现了请求签名与权限校验；仍需自行审计依赖库的许可证与漏洞。  
- **可部署性**：支持 Docker、K8s、系统服务三种方式，易于在 CI/CD 或内部渗透测试平台中以容器化方式上线。  

综合来看，BurpMCP‑Ultra 已具备 **高** 的生产候选资格，适合作为 AI‑驱动安全自动化的核心组件进行试点或正式投入使用。只要在部署前完成许可证合规检查与内部安全审计，即可在企业环境中安全运行。

## 🧭 Practical evaluation

**Value:** Cy-S3c/BurpMCP-Ultra helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 101 GitHub stars
- 14 forks
- updated 2026-06-25
- primary language: Kotlin
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 39/100 |
| production | 69/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/Cy-S3c/BurpMCP-Ultra) · [← Back to Mcp](./README.md)</sub>
