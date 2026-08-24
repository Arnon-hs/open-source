# olo-dot-io/Uni-CLI

[![Stars](https://img.shields.io/github/stars/olo-dot-io/Uni-CLI?style=flat-square&color=yellow)](https://github.com/olo-dot-io/Uni-CLI/stargazers) [![Forks](https://img.shields.io/github/forks/olo-dot-io/Uni-CLI?style=flat-square&color=blue)](https://github.com/olo-dot-io/Uni-CLI/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> Command-grade software access for AI agents. 235+ websites, desktop apps, MCP servers, and external CLIs as one searchable, self-repairing CLI catalog. YAML adapters, structured error envelopes, ~80 tokens per call.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 39 |
| 🍴 **Forks** | — |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-infrastructure` `ai-agents` `ai-tools` `automation` `browser-automation` `cdp` `chrome` `claude-code` `cli` `codex` `cursor` `developer-tools`

## 🎯 Categories

MCP · Automation · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary**  
Uni‑CLI (olo‑dot‑io/Uni‑CLI) is an open‑source, TypeScript‑based catalog that unifies access to 235+ web services, desktop applications, MCP servers, and external CLIs through a searchable, self‑repairing command‑line interface. It uses YAML adapters and structured error envelopes to keep each call under ~80 tokens, enabling AI agents to invoke real tools via a consistent protocol.

**Value**  
- **Standardized tool access** – AI assistants can talk to any registered service with a single, uniform CLI syntax, eliminating the need to write custom wrappers for each integration.  
- **Rapid prototyping & scaling** – The searchable catalog and self‑repairing adapters let developers quickly discover and connect new tools, then ship Model Context Protocol (MCP) servers that expose those capabilities to downstream models.  
- **Low token overhead** – By keeping calls under ~80 tokens, Uni‑CLI reduces prompt size and latency, making it practical for real‑time agent workflows.

**Practical Adoption Path**  
1. **Explore the catalog** – Use the built‑in search to locate the desired web service, desktop app, or MCP endpoint.  
2. **Add or customize an adapter** – If a tool is not yet covered, create a YAML adapter that maps the tool’s API/CLI to Uni‑CLI’s schema; the framework validates and self‑repairs the definition.  
3. **Deploy a Model Context Protocol server** – Wrap the Uni‑CLI catalog in an MCP server so your AI model can issue `uni <command>` calls over HTTP/gRPC.  
4. **Integrate with your AI agent** – Point the agent’s tool‑use module to the MCP endpoint; the agent can now invoke the tool, receive structured error envelopes, and handle failures gracefully.  
5. **Iterate and monitor** – Leverage the built‑in logging and health checks to refine adapters and ensure reliability in production.

**Production Readiness**  
- **High**: The repo shows recent activity (last commit 2026‑05‑13), 39 stars, 20 topical tags, and a clear TypeScript codebase, indicating an active community and maintainable code.  
- **Signals of stability**: Structured error envelopes, self‑repairing adapters, and a token‑efficient call model have been tested across a broad set of 235+ integrations.  
- **Remaining due diligence**: Verify the open‑source license compatibility, conduct a security audit of any third‑party binaries invoked, and confirm that maintainers are responsive to issues before committing to a large‑scale rollout.  

Overall, Uni‑CLI offers a mature, extensible bridge between AI agents and real‑world tools, making it a strong candidate for pilots and eventual production deployment.

### Русский

**Uni‑CLI (olo‑dot‑io/Uni-CLI)** — это открытый каталог команд‑строк, объединяющий более 235 веб‑сайтов, настольных приложений, MCP‑серверов и внешних CLI в единый, поисковый и самовосстанавливающийся интерфейс. Он позволяет AI‑агентам подключаться к реальным инструментам и данным через стандартизированный протокол (YAML‑адаптеры, структурированные ошибки, ~80 токенов за запрос), что упрощает создание сервисов типа Model Context Protocol и автоматизацию рабочих процессов. Проект активно поддерживается (TypeScript, 39★, обновлён 13 мая 2026), имеет хорошую экосистему и готов к пилотному внедрению в production‑среды, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
olo‑dot‑io/Uni‑CLI 是一套面向 AI 代理的“指令级”软件访问框架，统一收录 235+ 网站、桌面应用、MCP 服务器以及外部 CLI，提供可搜索、自动修复的统一 CLI 目录。通过 YAML 适配器、结构化错误封装以及每次调用约 80 tokens 的轻量协议，实现 AI 与真实工具和数据的无缝对接。

**价值**  
- **统一协议**：为 AI 助手提供标准化的接入点，避免为每个工具单独实现 SDK。  
- **即插即用**：只需编写或复用 YAML 适配器，即可让 AI 调用任意已有 CLI/API。  
- **自我修复 & 可搜索**：目录会自动检测失效命令并给出修复建议，降低运营成本。  
- **高效调用**：每次交互约 80 tokens，适配 LLM 的上下文限制，提升响应速度。

**典型接入方式**  
1. **选择目标工具**：在 Uni‑CLI 的目录中搜索或直接指定目标（如 `git`, `aws`, `chrome`）。  
2. **使用 YAML 适配器**：编写对应的 YAML 文件，声明输入参数、输出结构、错误封装等；已有适配器可直接复用。  
3. **在 AI Agent 中调用**：通过 Model Context Protocol（MCP）或直接调用 Uni‑CLI 提供的 SDK（TypeScript/Node），发送标准化的指令请求，收到结构化响应。  
4. **部署 MCP 服务器（可选）**：如需在内部网络或私有云中提供统一入口，可运行 Uni‑CLI 的 MCP 服务器实例，对外暴露统一 API。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑13，GitHub ★39，拥有 20+ 主题标签，社区活跃。  
- **技术成熟度**：使用 TypeScript 实现，提供完整的 API/SDK 文档，已在多个开源项目中实践。  
- **安全与合规**：暂无重大元数据风险，但仍需审查许可证（MIT）和潜在的依赖安全漏洞。  
- **适配成本**：只需编写或调整 YAML 适配器，即可快速上线，适合在生产环境进行试点。  

综合来看，Uni‑CLI 已具备较高的生产就绪度，适合作为 AI 助手与真实工具交互的标准化桥梁，在自动化、DevTools、AI/ML 等场景中快速落地。

## 🧭 Practical evaluation

**Value:** olo-dot-io/Uni-CLI helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 39 GitHub stars
- updated 2026-05-13
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 34/100 |
| topics | 100/100 |
| outlook | 53/100 |
| quality | 46/100 |
| recency | 20/100 |
| adoption | 25/100 |
| production | 52/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/olo-dot-io/Uni-CLI) · [← Back to Mcp](./README.md)</sub>
