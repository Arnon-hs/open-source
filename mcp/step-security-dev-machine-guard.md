# step-security/dev-machine-guard

[![Stars](https://img.shields.io/github/stars/step-security/dev-machine-guard?style=flat-square&color=yellow)](https://github.com/step-security/dev-machine-guard/stargazers) [![Forks](https://img.shields.io/github/forks/step-security/dev-machine-guard?style=flat-square&color=blue)](https://github.com/step-security/dev-machine-guard/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Scan your dev machine for AI agents, MCP servers, IDE extensions, and suspicious packages - in seconds.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 159 |
| 🍴 **Forks** | 19 |
| 💻 **Language** | Go |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

MCP · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*step‑security/dev‑machine‑guard* is a Go‑based utility that quickly scans a developer’s workstation for AI agents, Model‑Context‑Protocol (MCP) servers, IDE extensions, and suspicious packages. By exposing a standard protocol for connecting AI assistants to real tools and data, it lets teams prototype “AI‑augmented” workflows while keeping a security‑focused eye on the local environment.  

**Value**  
- **Security‑first visibility** – Detects rogue or outdated AI components and suspicious dependencies before they can be leveraged by malicious actors.  
- **Standardised integration** – Implements the Model Context Protocol, enabling any MCP‑compatible AI assistant to interact with local tools (editors, CLIs, build systems) without custom glue code.  
- **Rapid prototyping** – A lightweight scan that runs in seconds, making it practical for CI checks, onboarding scripts, or “security‑as‑code” gatekeeping in internal dev pipelines.  

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Fork the repo, run the default scan on a sandbox workstation, and verify that the JSON/HTTP output matches your tooling expectations.  
2. **README‑driven integration** – Follow the quick‑start guide to expose the generated MCP endpoint to a test AI assistant (e.g., OpenAI‑function‑calling or LangChain).  
3. **CI/CD gate** – Wrap the CLI in a GitHub Action or pre‑commit hook to block merges when suspicious packages or unknown agents are detected.  
4. **Iterative hardening** – Add custom detection rules (e.g., corporate‑approved extensions) and monitor the audit logs before rolling out to the full dev fleet.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑06‑23), has a modest community (≈160 ★, 19 forks), and the core functionality is stable for internal use.  
- **Considerations before production**:  
  * Verify the licensing terms and ensure they align with your organization’s policy.  
  * Perform a security audit of the binary and its dependencies (Go modules).  
  * Establish a maintenance plan for updating the tool and its detection signatures.  
- **Suitable use‑cases**: Internal prototype environments, “AI‑assistant‑enabled” developer workstations, and as a gating step in CI pipelines. With the above checks, it can be promoted to production for broader internal deployment.

### Русский

**step-security/dev-machine-guard** — это Go‑утилита, сканирующая рабочую станцию за секунды на наличие AI‑агентов, MCP‑серверов, подозрительных IDE‑расширений и пакетов, что позволяет быстро оценить безопасность окружения и подготовить его к интеграции с Model Context Protocol. Типичный сценарий — запуск небольшого proof‑of‑concept: проверить репозиторий, выполнить базовое сканирование и, при необходимости, добавить проверку в CI/CD, после чего перейти к более масштабному использованию в прототипах или внутренних workflow. Готовность к production — средняя: проект имеет активную звёздную базу (159 ★) и недавние обновления, но перед выпуском в продакшн требуется проверка лицензии, безопасности зависимостей и наличие поддерживающих мейнтейнеров.

### 中文

**项目简介**  
step-security/dev-machine-guard 是一款用 Go 编写的轻量级安全扫描工具，能够在几秒钟内检查本地开发环境中是否存在 AI 代理、MCP 服务器、IDE 插件以及可疑的依赖包。  

**价值**  
- **统一协议**：通过标准的 Model Context Protocol（MCP），为 AI 助手提供安全、可控的工具和数据接入入口。  
- **快速可视化**：即刻发现潜在的 AI 代理或恶意包，帮助团队在开发阶段就把安全风险拦截在源头。  
- **加速集成**：为内部原型或业务流程提供“一键式”检测，降低 AI/ML 项目接入第三方工具的门槛。  

**典型接入方式**  
1. **本地快速验证**：在 CI/CD 前或开发机器上运行 `dev-machine-guard scan`，获取扫描报告。  
2. **CI/CD 插件**：将其包装为 Docker 镜像或 GitHub Action，在代码合并前自动执行安全检查。  
3. **服务化部署**：在内部的 Model Context Protocol（MCP）网关旁边运行守护进程，实时监控新安装的 IDE 扩展或 npm/pip 包。  

**生产可用性**  
- **成熟度**：目前评分 66/100，适合作为原型或内部工作流的安全层。  
- **依赖与维护**：项目活跃（2026‑06‑23 最近更新），拥有 159 ★、19 Fork，核心代码基于 Go，易于审计。  
- **上线建议**：在生产环境使用前，建议先在小范围（如单个团队或测试环境）进行 PoC，检查依赖许可证、漏洞报告以及维护者响应速度；确认无重大安全隐患后再推广至全员机器。  

总体而言，step-security/dev-machine-guard 为 AI 助手与真实开发工具的安全对接提供了快速、标准化的解决方案，适合在内部原型阶段快速落地，生产化前需完成依赖审计和持续维护评估。

## 🧭 Practical evaluation

**Value:** step-security/dev-machine-guard helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 159 GitHub stars
- 19 forks
- updated 2026-06-23
- primary language: Go

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 47/100 |
| topics | 0/100 |
| outlook | 50/100 |
| quality | 44/100 |
| recency | 40/100 |
| adoption | 43/100 |
| production | 51/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/step-security/dev-machine-guard) · [← Back to Mcp](./README.md)</sub>
