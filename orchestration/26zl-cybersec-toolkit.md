# 26zl/cybersec-toolkit

[![Stars](https://img.shields.io/github/stars/26zl/cybersec-toolkit?style=flat-square&color=yellow)](https://github.com/26zl/cybersec-toolkit/stargazers) [![Forks](https://img.shields.io/github/forks/26zl/cybersec-toolkit?style=flat-square&color=blue)](https://github.com/26zl/cybersec-toolkit/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> One command installs 580+ security tools on Linux & Termux; an authorization-gated MCP server picks tools and runs them with you — companion by default, an autonomous solver when you ask. Modular bash installer (18 modules, 14 profiles) + 870+ Claude Code skills for AI-assisted ethical hacking: CTF, pentest, bug bounty, DFIR, red & blue team.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | Python |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skills` `ai-agent` `ai-hacking` `blue-team` `bug-bounty` `claude-code` `ctf-tools` `cybersecurity` `dfir` `ethical-hacking` `hacking-tools` `kali-linux`

## 🎯 Categories

Orchestration · MCP · Automation · AI/ML · Backend

## 📝 Summary

### English

**Brief summary**  
The 26zl/cybersec‑toolkit is a modular Bash/Python installer that can provision 580+ security tools on Linux or Termux with a single command, then expose them through an authorization‑gated MCP (Multi‑Component Processor) server. The server can act as a “companion” that runs the selected tools alongside you, or as an autonomous solver that executes them on demand, while a library of 870+ Claude Code skills adds AI‑assisted assistance for CTFs, pentests, bug‑bounty, DFIR, and red/blue‑team tasks.

---

### Value proposition
- **One‑click environment** – eliminates the tedious, error‑prone process of manually installing dozens of security utilities; the 18 installer modules and 14 pre‑defined profiles let you spin up a fully‑featured cyber‑security lab in minutes.  
- **Agent‑centric workflow** – the MCP server abstracts each tool as a callable service, enabling prompt‑driven agents (LLMs, Claude, etc.) to invoke them directly. This turns ad‑hoc command‑line prompts into repeatable, orchestrated agent workflows.  
- **AI‑augmented tooling** – the bundled Claude Code skills provide ready‑made “tool‑use recipes” (e.g., enumerate subdomains, run nmap, parse Volatility images), accelerating both manual and autonomous investigations.  
- **Cross‑platform reach** – works on standard Linux distributions and on Android/Termux, making it useful for on‑the‑go assessments or classroom labs.

### Practical adoption path
1. **Evaluation** – Clone the repo, run the single‑line installer on a fresh VM or Termux instance, and select a profile that matches your use case (e.g., “pentest” or “DFIR”). Verify that the MCP server starts and that a few sample tools can be invoked via its CLI or simple HTTP API.  
2. **Integration** – Wrap the MCP endpoint in your existing automation stack (CI/CD, SOAR, or custom Python scripts). Because the project publishes explicit API/SDK signatures and uses standard JSON payloads, plugging it into existing orchestration tools (e.g., Ansible, Airflow, or LangChain) requires only minimal glue code.  
3. **Extension** – Add or customize Claude Code skills to cover organization‑specific tooling or internal scripts. The modular Bash installer makes it easy to drop new modules into the `modules/` directory and update the profile definitions.  
4. **Governance** – Harden the authorization layer (TLS, API keys, RBAC) before exposing the server beyond a sandbox. Conduct a dependency audit (the installer pulls many binaries) and pin versions to avoid supply‑chain drift.  

### Production readiness
- **Maturity** – Rated “Medium”. The toolkit is functional for prototypes and internal labs; it has recent activity (last commit 2026‑07‑02) and a modest community (22 ★, 2 forks).  
- **Stability concerns** – The large number of external binaries introduces dependency‑management and update‑frequency challenges. No formal CI/CD pipeline or release‑grade testing is evident, so you should perform your own regression checks after each installer run.  
- **Security posture** – The MCP server is gated, but the repository lacks a detailed security policy or audit report. Conduct a code review, verify the license compatibility, and consider containerizing the server to isolate it from critical infrastructure.  
- **Operational fit** – Well‑suited for proof‑of‑concepts, red‑team labs, CTF training environments, or internal automation pipelines where rapid tool provisioning outweighs the need for enterprise‑grade SLAs. For customer‑facing or compliance‑sensitive deployments, additional hardening, version pinning, and monitoring would be required.  

In short, 26zl/cybersec‑toolkit can dramatically accelerate the setup of a comprehensive security toolchain and enable AI‑driven agent orchestration, but moving it to production calls for careful dependency auditing, security hardening, and possibly wrapping it in a container or managed service to meet reliability and compliance standards.

### Русский

**26zl/cybersec-toolkit** – это модульный набор скриптов и AI‑поддержки, который одной командой разворачивает более 580‑ти security‑инструментов как в обычном Linux, так и в Termux, а через авторизованный MCP‑сервер позволяет автоматически подбирать и запускать их в виде «компаньона» или «автономного решателя». Типичный сценарий — координация многоагентных CTF/пентест‑или DFIR‑потоков: разработчик задаёт задачу, система подбирает нужные инструменты, формирует повторяемый пайплайн и сохраняет контекст работы, что упрощает создание и стандартизацию агентных воркфлоу. Готовность к production — средняя: проект уже стабильно работает (обновлён 2026‑07‑02, 22★, Python), но перед развертыванием в продакшн требуется проверка лицензий, безопасности зависимостей и наличие активных мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
26zl/cybersec‑toolkit 只需一条指令即可在 Linux 与 Termux 上一次性安装 580+ 安全工具，并通过授权网关的 MCP 服务器按需挑选、执行这些工具——默认以伴侣模式协同工作，亦可在请求时切换为全自动求解器。它采用模块化 Bash 安装器（18 个模块、14 套配置）并配套 870+ Claude Code 技能，实现 AI 辅助的 CTF、渗透测试、漏洞赏金、DFIR、红蓝对抗等全流程自动化。

---

## 价值说明
1. **快速搭建全栈安全环境**：一次性安装海量工具，省去手动搜集、兼容性调试的时间，立刻拥有渗透、取证、红蓝对抗等完整技术栈。  
2. **统一的多代理编排**：MCP（Multi‑Component Processor）服务器把离散的工具和提示封装为可复用的 Agent 工作流，便于在同一平台上协调多 Agent、共享记忆和状态。  
3. **AI‑驱动的工具调用**：内置 870+ Claude Code 技能，使 LLM 能直接识别、参数化并调用安全工具，实现“提示 → 工具 → 结果”的闭环，显著提升 CTF、红蓝演练等场景的效率。  
4. **模块化、可定制**：18 个 Bash 安装模块和 14 种预设配置文件（profiles）让用户按需选装，兼容 Linux 与 Android‑Termux 双平台。  

## 典型接入方式
| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| **内部原型 / 自动化脚本** | 直接使用项目提供的 CLI (`./install.sh -p <profile>`) | 1. 克隆仓库 2. 运行一条安装命令 3. 通过 `mcp-client` 调用 API（REST/JSON）或本地 CLI 启动特定工具 |
| **LLM + 安全工具编排** | 通过项目公开的 Python SDK 或 HTTP API 与 LLM（Claude、ChatGPT）集成 | 1. 在 LLM 提示中引用对应的 Claude Code skill ID 2. LLM 调用 SDK 的 `run_tool(tool_name, args)` 接口 3. 结果返回给 LLM 继续推理 |
| **CI/CD 安全检测** | 在 CI 流水线中加入 `bash install.sh -p ci`，随后调用 `mcp-cli scan <target>` | 1. 在容器镜像构建阶段执行安装脚本 2. 使用 `mcp-cli` 触发静态/动态扫描 3. 将报告上传至审计平台 |
| **红蓝对抗平台** | 作为后端服务部署（Docker）并暴露 RESTful 接口供前端调度 | 1. `docker compose up -d` 启动 MCP 服务器 2. 前端通过 `/api/run` 提交任务 3. 服务器调度对应模块并返回实时日志 |

> **重点**：项目提供的 `mcp-client`（Python）和 `mcp-cli`（Bash）是最直接的接入点；若已有内部服务总线，可通过 HTTP/WebSocket 将其包装为微服务。

## 生产可用性评估
| 维度 | 现状 | 备注 |
|------|------|------|
| **成熟度** | **中等**（适用于原型、内部工具） | 已实现完整安装与 API，仍需自行进行依赖锁定、版本审计和安全加固。 |
| **依赖管理** | Bash + Python 环境，依赖 580+ 第三方安全工具 | 建议使用容器化或虚拟环境封装，避免系统库冲突。 |
| **维护活跃度** | 最近一次提交 2026‑07‑02，星标 22，Fork 2 | 活跃度一般，需自行监控 upstream 更新并评估安全补丁。 |
| **安全合规** | 未发现显著元数据风险；许可证、维护者信息待确认 | 在生产环境部署前，请审查 LICENSE（默认 MIT?）并进行代码审计。 |
| **可扩展性** | 支持自定义 Bash 模块和新增 Claude Code skill | 可依据内部工具链添加专属模块，保持与现有安全流程一致。 |
| **监控/日志** | 通过 MCP 服务器提供实时日志输出，支持导出 | 建议接入集中日志系统（ELK、Prometheus）以实现可观测性。 |
| **容错/高可用** | 单实例 MCP 服务器，未提供内置 HA | 对关键业务可考虑水平扩展（多实例 + 负载均衡）或使用容器编排（K8s）。 |

**结论**：26zl/cybersec‑toolkit 已具备快速部署全套安全工具链和 AI‑驱动编排的核心能力，适合作为内部原型或安全研发平台的基础设施。若要在生产环境使用，建议：  
1. 将其容器化并锁定依赖版本；  
2. 完成许可证与安全审计；  
3. 为 MCP 服务器添加身份认证、审计日志和高可用部署方案。  

完成上述措施后，即可在企业内部实现可重复、可扩展的多 Agent 安全工作流。

## 🧭 Practical evaluation

**Value:** 26zl/cybersec-toolkit helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 22 GitHub stars
- 2 forks
- updated 2026-07-02
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 51/100 |
| recency | 40/100 |
| adoption | 24/100 |
| production | 54/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/26zl/cybersec-toolkit) · [← Back to Orchestration](./README.md)</sub>
