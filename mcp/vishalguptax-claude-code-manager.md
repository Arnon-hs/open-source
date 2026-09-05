# vishalguptax/claude-code-manager

[![Stars](https://img.shields.io/github/stars/vishalguptax/claude-code-manager?style=flat-square&color=yellow)](https://github.com/vishalguptax/claude-code-manager/stargazers) [![Forks](https://img.shields.io/github/forks/vishalguptax/claude-code-manager?style=flat-square&color=blue)](https://github.com/vishalguptax/claude-code-manager/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Claude Code Manager - sessions, MCP, skills, usage & accounts in your VS Code sidebar. 100% local.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 21 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`account-switcher` `ai-coding` `ai-tools` `anthropic` `antigravity` `claude` `claude-ai` `claude-code` `claude-code-manager` `claude-manager` `claude-session` `claude-session-manager`

## 🎯 Categories

MCP · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Claude Code Manager is a VS Code extension that brings Claude‑based AI assistants directly into the editor sidebar, letting you manage sessions, Model‑Context‑Protocol (MCP) servers, skills, usage statistics, and accounts—all locally, without any cloud calls. Written in TypeScript, the project offers a clean API/SDK/CLI surface for plugging AI agents into real tools and data, making it a handy scaffold for prototyping AI‑enhanced development workflows.  

**Value Proposition**  
- **Local‑first AI integration** – All interactions stay on the developer’s machine, preserving privacy and eliminating latency or cost associated with external services.  
- **Standardised MCP support** – By implementing the Model‑Context‑Protocol, the extension provides a common language for AI agents to discover and invoke tools, reducing the friction of building custom connectors.  
- **Unified management UI** – Sessions, skill libraries, usage quotas, and multiple Claude accounts are visible and controllable from a single sidebar pane, streamlining day‑to‑day AI‑assisted coding.  

**Practical Adoption Path**  
1. **Evaluate the API/CLI** – Clone the repo, run the provided npm scripts, and explore the exported TypeScript SDK to see how MCP servers are started and how skills are registered.  
2. **Prototype a skill** – Write a simple skill (e.g., a file‑search or git‑status tool) using the documented skill‑definition schema and load it through the extension’s “Skills” panel.  
3. **Integrate with existing pipelines** – Replace or augment current scripts/CLI tools by exposing them as MCP endpoints; the extension can invoke them automatically from within VS Code.  
4. **Iterate & test** – Use the built‑in usage dashboard to monitor token consumption and performance, adjusting prompts or skill definitions as needed.  
5. **Scale to internal teams** – Package the extension as a VS Code marketplace item (or internal VS IX feed) and distribute it across the organization, optionally pairing it with a centrally hosted MCP server for shared resources.  

**Production Readiness Assessment**  
- **Maturity**: Medium. The codebase is recent (last commit 2026‑07‑03), has modest community interest (21 ★, 5 forks), and follows a clear TypeScript architecture, making it suitable for internal prototypes and early‑stage deployments.  
- **Dependencies & Maintenance**: The project relies on standard VS Code extension APIs and a few npm packages; however, it lacks a long‑term maintainer badge and formal CI/CD pipelines, so a review of transitive dependencies and a plan for security updates are advisable.  
- **Risk Factors**: No obvious licensing or metadata issues, but the security posture (e.g., handling of API keys for Claude accounts) and long‑term support need validation before a production rollout.  
- **Recommendation**: Deploy in a controlled environment (e.g., a dev sandbox or a pilot team) to validate stability and security, then harden the setup (pin dependencies, add automated tests, establish a maintainer) before scaling to mission‑critical workflows.

### Русский

**Claude Code Manager** (vishalguptax/claude-code-manager) — это расширение для VS Code, которое полностью локально интегрирует Claude‑подобные AI‑ассистенты с вашими сессиями, MCP‑сервером, навыками, учётными записями и статистикой использования прямо в боковой панели. Типичный сценарий: разработчик подключает к локальному Model Context Protocol (MCP) серверу свои инструменты и данные, после чего AI‑агент может вызывать их через единый протокол, что упрощает прототипирование и внутренние рабочие процессы. Готовность к production — средняя: проект уже стабилен и обновлён (21 звезда, 5 форков, TypeScript), но перед развертыванием в продакшн требуется проверка лицензии, безопасности и поддержки зависимостей.

### 中文

**简短介绍**
名称：vishalguptax/claude-code-manager
描述：Claude Code Manager 是一个开源项目，用于在 VS Code sidebar 中管理会话、MCP、技能、使用情况和账户。它完全本地化。

**价值**
vishalguptax/claude-code-manager 帮助连接 AI 助手到实际工具和数据通过一个标准协议。它可以连接 AI 代理到工具，部署 Model Context Protocol 服务器，标准化集成。

**典型接入方式**
该项目通过 API/SDK/CLI 等接口提供实现信号。开发者可以通过这些接口来连接 AI 助手到实际工具和数据。

**生产可用性**
该项目的生产可用性为中等。它适合用于原型或内部工作流，需要在生产环境中进行依赖和维护检查。

## 🧭 Practical evaluation

**Value:** vishalguptax/claude-code-manager helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 21 GitHub stars
- 5 forks
- updated 2026-07-03
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 69/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 26/100 |
| production | 67/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/vishalguptax/claude-code-manager) · [← Back to Mcp](./README.md)</sub>
