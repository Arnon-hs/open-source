# softdaddy-o/soft-ue-cli

[![Stars](https://img.shields.io/github/stars/softdaddy-o/soft-ue-cli?style=flat-square&color=yellow)](https://github.com/softdaddy-o/soft-ue-cli/stargazers) [![Forks](https://img.shields.io/github/forks/softdaddy-o/soft-ue-cli?style=flat-square&color=blue)](https://github.com/softdaddy-o/soft-ue-cli/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> Python CLI + UE plugin that lets Claude Code (AI coding agent) control Unreal Engine in real time. Spawn actors, edit blueprints, call functions, capture screenshots, manage PIE sessions, and more -- all from the terminal. Works with UE5 editor and packaged builds via an in-process HTTP bridge.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 187 |
| 🍴 **Forks** | 41 |
| 💻 **Language** | C++ |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-assisted-development` `ai-tools` `anthropic` `blueprints` `claude-code` `cli` `devtools` `game-development` `python-cli` `ue5` `unreal-engine` `unreal-engine-5`

## 🎯 Categories

Automation · AI/ML · DevTools

## 📝 Summary

### English

**Project Summary:** 

softdaddy-o/soft-ue-cli is an open-source Python CLI and Unreal Engine plugin that enables real-time control of Unreal Engine using Claude Code, a coding AI agent. This tool automates repetitive tasks, allowing developers to streamline their workflow and focus on higher-level tasks. With its high production readiness and recent adoption, it's an attractive solution for those seeking to integrate AI-driven automation into their development processes.

**Value Proposition:**

The primary value of softdaddy-o/soft-ue-cli lies in its ability to remove repetitive manual operations from a workflow. This can significantly improve productivity and reduce the time spent on mundane tasks. By automating tasks such as spawning actors, editing blueprints, and managing PIE sessions, developers can focus on more complex and creative aspects of game development.

**Practical Adoption Path:**

To adopt softdaddy-o/soft-ue-cli, developers can follow these steps:

1. Evaluate the project's documentation and API to understand its capabilities and limitations.
2. Integrate the plugin with Unreal Engine, either through the editor or packaged builds.
3. Configure the CLI to connect with Claude Code, the AI coding agent.
4. Test the automation of repetitive tasks to ensure seamless integration.
5. Customize and extend the plugin to

### Русский

Резюме:

softdaddy-o/soft-ue-cli - это открытый-source проект, который позволяет использовать искусственный интеллект (AI) для автоматизации операций в Unreal Engine. Этот инструмент предоставляет возможность выполнять такие задачи, как создание актёров, редактирование б蓝принтов, вызов функций и захват экрана, прямо из командной строки. softdaddy-o/soft-ue-cli идеально подходит для удаления повторяющихся ручных операций из рабочего процесса, что делает его ценным инструментом для разработчиков и команд.

Типовой сценарий внедрения: softdaddy-o/soft-ue-cli может быть использован для автоматизации повторяющихся задач в Unreal Engine, такие как создание актёров, редактирование б蓝принтов и захват экрана. Это может помочь разработчикам сократить время, затрачиваемое на выполнение этих задач, и сосредоточиться на более сложных задачах.

Уровень готовности к production: softdaddy-o/soft-ue-cli готов к использованию в production. Проект имеет высокий уровень

### 中文

**项目简介**  
softdaddy‑o/soft-ue-cli 是一个基于 Python CLI 与 Unreal Engine 插件的工具，能够让 Claude Code（AI 编码代理）实时控制 UE5。通过终端即可生成 Actor、编辑 Blueprint、调用函数、截图、管理 PIE 会话等，内部通过进程内 HTTP 桥接实现对编辑器和打包运行时的统一操控。

**价值体现**  
- **自动化重复操作**：把手动的资源创建、蓝图编辑、调试截图等工作交给 AI，显著提升开发效率。  
- **可编排的工作流**：CLI 可以被脚本、CI/CD 或调度系统调用，轻松把 UE 操作嵌入到更大的自动化流水线。  
- **统一入口**：一次实现的 HTTP 接口即支持本地编辑器也支持已打包的游戏客户端，降低了多环境集成成本。

**典型接入方式**  
1. **安装 CLI**：`pip install soft-ue-cli`（或从源码安装）。  
2. **启动 UE 插件**：在 UE5 编辑器或打包版本中启用 SoftUE 插件，插件会在后台启动 HTTP 服务器。  
3. **调用命令**：在终端或脚本中使用 `softue <subcommand> [options]`，如 `softue spawn-actor --class MyActor --location 0,0,0`。  
4. **与 Claude Code 集成**：在 Claude 的提示或自定义插件中直接发送对应 CLI 命令，实现“对话即操控”闭环。

**生产可用性**  
- **活跃度**：截至 2026‑07‑06 最近一次提交，GitHub ★187、Fork 41，社区讨论活跃。  
- **技术成熟度**：核心功能已在 UE5 编辑器和打包构建中验证，提供稳定的 API/SDK 与 CLI 接口。  
- **风险点**：仍需确认许可证兼容性、潜在安全（HTTP 桥接）以及维护者的长期可用性。总体来看，项目已具备在内部或受控环境中进行正式试点的条件。

## 🧭 Practical evaluation

**Value:** softdaddy-o/soft-ue-cli helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 187 GitHub stars
- 41 forks
- updated 2026-07-06
- primary language: C++
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 48/100 |
| topics | 100/100 |
| outlook | 66/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 46/100 |
| production | 60/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/softdaddy-o/soft-ue-cli) · [← Back to Automation](./README.md)</sub>
