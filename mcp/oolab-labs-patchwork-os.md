# Oolab-labs/patchwork-os

[![Stars](https://img.shields.io/github/stars/Oolab-labs/patchwork-os?style=flat-square&color=yellow)](https://github.com/Oolab-labs/patchwork-os/stargazers) [![Forks](https://img.shields.io/github/forks/Oolab-labs/patchwork-os?style=flat-square&color=blue)](https://github.com/Oolab-labs/patchwork-os/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> personal AI runtime, local-first. MCP bridge giving Claude Code 170+ tools (LSP, debugger, terminal, git) inside VS Code, Cursor, Windsurf, or JetBrains. Optional Patchwork layer adds YAML recipes, an approval queue, and an oversight dashboard. Your models, your machine, your policy. (Mac & Windows)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 26 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `anthropic` `approval-queue` `automation` `claude` `claude-code` `ide` `local-first` `lsp` `mcp` `mcp-server` `ollama`

## 🎯 Categories

MCP · Automation · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Patchwork‑OS is an open‑source, local‑first AI runtime that bridges Claude Code (and other LLMs) to over 170 development tools—including LSP servers, debuggers, terminals, and Git—via a standardized Model Context Protocol (MCP). An optional “Patchwork” layer adds YAML‑based recipes, an approval queue, and an oversight dashboard, letting teams enforce custom policies while keeping all models and data on‑premise (macOS & Windows).

**Value Proposition**  
- **Tool‑centric AI** – By exposing a uniform MCP interface, Patchwork‑OS lets any AI assistant invoke real development tools instead of relying on hallucinated code, dramatically improving correctness and traceability.  
- **Policy & Governance** – The YAML recipe system and approval queue give organizations fine‑grained control over which actions an AI can perform, satisfying security and compliance requirements for on‑premise deployments.  
- **Cross‑IDE Compatibility** – The same bridge works inside VS Code, Cursor, Windsurf, or JetBrains, reducing integration effort across heterogeneous developer stacks.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Prototype** – Clone the repo, run the provided Docker/CLI starter, and point Claude Code (or another MCP‑compatible model) at the local MCP server. Verify basic tool calls (e.g., `git status`, `npm install`). | Quick win to confirm the protocol works in your environment. |
| 2️⃣  | **Define YAML Recipes** – Encode the most common workflows (code generation, linting, CI checks) as recipes. Use the built‑in approval queue to require human sign‑off for risky actions. | Turns ad‑hoc calls into repeatable, auditable processes. |
| 3️⃣  | **Integrate with IDE** – Install the Patchwork extension for your preferred IDE (VS Code, JetBrains, etc.) and configure it to point at your local MCP endpoint. Test end‑to‑end scenarios like “AI‑debugger” or “AI‑git‑commit”. | Gives developers a seamless experience and validates cross‑IDE stability. |
| 4️⃣  | **Policy Hardening** – Enable the oversight dashboard, set role‑based permissions, and hook the approval queue into existing ticketing or SSO systems. | Aligns the runtime with corporate security and compliance policies. |
| 5️⃣  | **Scale to Production** – Containerize the MCP server, add health checks, and monitor resource usage. Perform a security audit of the TypeScript codebase and verify the license (MIT‑style) matches your organization’s policy. | Ensures reliability, observability, and legal clearance before broader rollout. |

**Production Readiness Assessment**  

- **Maturity**: Medium. The project is actively maintained (last update 2026‑06‑23) and has a modest but growing community (26 ★, 4 forks). The core MCP bridge is functional, but the optional Patchwork layer still needs thorough testing in large‑scale environments.  
- **Strengths**: Clear API/SDK/CLI surface, language‑agnostic protocol, and strong focus on on‑premise security. Works on both macOS and Windows, covering the majority of developer workstations.  
- **Risks**:  
  1. **Maintenance** – Small contributor base; you may need to allocate internal resources for bug fixes and feature extensions.  
  2. **Security** – No formal security audit yet; review the TypeScript dependencies and consider hardening the MCP server (TLS, auth tokens).  
  3. **License** – Verify the repository’s license (likely MIT/Apache) aligns with your organization’s policy.  

**Bottom Line**  
Patchwork‑OS offers a compelling way to tether AI assistants to real development tools while keeping data and policy control in‑house. For teams looking to prototype AI‑augmented workflows, it’s ready for internal pilots with modest integration effort. Moving to production will require a focused security review, possible contributor support, and the implementation of governance controls via the YAML recipes and approval queue.

### Русский

**Patchwork‑OS** — это open‑source runtime для локального ИИ, который через MCP‑мост соединяет Claude Code (и другие модели) с более чем 170 реальными инструментами (LSP, отладчик, терминал, git) внутри VS Code, Cursor, Windsurf или JetBrains; дополнительный слой Patchwork добавляет YAML‑рецепты, очередь согласования и панель контроля. Типичный сценарий — быстрое прототипирование или внутренние рабочие процессы, где требуется подключить AI‑агента к существующим инструментам и данным, а также развернуть собственный Model Context Protocol‑сервер. Готовность к production — средняя: проект стабилен для прототипов, но перед выпуском в продакшн требуется проверка зависимостей, лицензий и безопасности.

### 中文

**项目简介（2‑3 句）**  
Patchwork‑OS 是一个本地优先的个人 AI 运行时，提供 MCP（Model Context Protocol）桥接层，让 Claude‑Code 通过 170+ 工具（LSP、调试器、终端、Git 等）直接在 VS Code、Cursor、Windsurf 或 JetBrains 中工作。可选的 Patchwork 层进一步加入 YAML 配方、审批队列和监管仪表盘，实现模型、机器和策略的全链路可控。

**价值主张**  
- **标准化 AI‑Tool 接入**：通过统一的 MCP 协议，把 AI 助手安全地连接到本地开发工具、终端和版本控制系统，避免每个项目各自实现繁琐的集成。  
- **本地化与隐私**：所有模型和数据均运行在用户机器上，遵循自定义的安全策略，适合对数据合规性要求严格的企业或个人。  
- **可扩展的治理层**：Patchwork 提供 YAML 配方、审批队列和可视化监管面板，帮助团队在使用 AI 自动化时实现审计、批准和回滚。

**典型接入方式**  
1. **作为本地服务运行**：克隆仓库后 `npm install && npm run start` 启动 MCP 服务器。  
2. **IDE 插件/扩展**：在 VS Code、Cursor、Windsurf 或 JetBrains 中安装对应的插件，插件会自动发现本地 MCP 端点并注册所有工具。  
3. **CLI/SDK 调用**：项目提供 TypeScript/JavaScript SDK 与 CLI，开发者可在自定义脚本或 CI 流程中通过 `patchwork-client` 调用模型、执行命令或触发 YAML 配方。  
4. **模型部署**：将自己的模型（OpenAI、Claude、Llama 等）通过 MCP 适配器注册，即可在同一桥接层内统一使用。

**生产可用性评估**  
- **成熟度**：Medium。代码已更新至 2026‑06‑23，拥有 26 星、4 个 fork，适合原型和内部工作流。  
- **依赖与维护**：基于 TypeScript，依赖相对轻量；但仍需自行审查第三方库的安全状态并确认维护者的活跃度。  
- **部署门槛**：在 macOS/Windows 上直接 `npm` 安装即可，配置简单；若在企业环境使用，建议进行安全审计并制定内部升级策略。  
- **可扩展性**：支持自定义 MCP 实现和 Patchwork YAML 配方，能够满足从小团队到中大型组织的不同治理需求。  

综上，Patchwork‑OS 为将 AI 助手与真实开发工具深度集成提供了统一、可审计的桥接方案，适合作为原型验证平台或在对数据隐私有严格要求的内部生产环境中使用。

## 🧭 Practical evaluation

**Value:** Oolab-labs/patchwork-os helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 26 GitHub stars
- 4 forks
- updated 2026-06-23
- primary language: TypeScript
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 30/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 52/100 |
| recency | 40/100 |
| adoption | 27/100 |
| production | 54/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/Oolab-labs/patchwork-os) · [← Back to Mcp](./README.md)</sub>
