# yeet-src/agent-lock

[![Stars](https://img.shields.io/github/stars/yeet-src/agent-lock?style=flat-square&color=yellow)](https://github.com/yeet-src/agent-lock/stargazers) [![Forks](https://img.shields.io/github/forks/yeet-src/agent-lock?style=flat-square&color=blue)](https://github.com/yeet-src/agent-lock/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> Confine an AI agent (Claude Code, Codex, oh-my-pi, ...) to one directory with a BPF-LSM program, and watch it live over eBPF.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 31 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-security` `ai-agents` `bpf-lsm` `ebpf` `linux` `llm-tools` `lsm` `oh-my-pi` `sandbox` `security` `yeet`

## 🎯 Categories

AI/ML · Security

## 📝 Summary

### English

Here's a brief summary of the yeet-src/agent-lock project:

**Summary:** yeet-src/agent-lock is an open-source project that allows developers to confine AI agents to a single directory using a BPF-LSM program, enabling live monitoring over eBPF. This project provides a convenient way to prototype AI features and build RAG or agent workflows without starting from scratch. It's particularly useful for evaluating model tooling and developing internal workflows.

**Value:** The project's value proposition lies in its ability to streamline the development of AI capabilities by leveraging existing models and tools. It helps developers build and test AI-powered applications quickly, making it an attractive option for prototyping and internal workflows.

**Practical Adoption Path:** To adopt yeet-src/agent-lock, developers should start by evaluating the project through a small proof of concept and carefully reviewing the README documentation. This will help them understand the integration path and potential setup costs. Once they're familiar with the project, they can begin integrating it into their workflows, starting with small-scale applications and gradually scaling up to more complex projects.

**Production Readiness:** The project is considered medium-production ready, meaning it's suitable for internal workflows and prototypes but may require additional dependencies and maintenance checks before being deployed in production environments. This

### Русский

Резюме проекта yeet-src/agent-lock:

Проект yeet-src/agent-lock позволяет добавить функциональность AI в существующие приложения без необходимости создавать новую модель. Он конфигурирует агента AI в одном каталоге с помощью BPF-LSM и позволяет наблюдать за его работой в режиме реального времени с помощью eBPF. Этот проект подойдет для прототипирования функций AI, построения рабочих процессов агента или оценки инструментов моделирования в среде разработки.

### 中文

**项目简介（2‑3 句）**  
yeet-src/agent‑lock 通过 BPF‑LSM 程序将 Claude Code、Codex、oh‑my‑pi 等 AI 代理限制在单一目录内运行，并利用 eBPF 实时监控其行为。它让开发者在已有模型之上快速加入安全沙箱，实现 AI 功能原型而无需从零搭建模型栈。

---

## 价值说明  

| 维度 | 价值点 |
|------|--------|
| **安全** | BPF‑LSM 在内核层面强制文件系统访问限制，防止 AI 代理读取/写入超出授权目录的敏感文件，降低泄露和破坏风险。 |
| **可观测** | eBPF 程序实时捕获系统调用、文件 I/O、网络请求等指标，帮助团队快速定位异常行为或性能瓶颈。 |
| **加速研发** | 直接在现有模型（Claude Code、Codex 等）上套用沙箱，无需重新训练或部署完整模型，适合快速验证 RAG、Agent 工作流等 AI 场景。 |
| **成本低** | 只需在 Linux 主机上加载 BPF 程序，无额外云算力或专有硬件，适合内部原型和小规模实验。 |

---

## 典型接入方式  

1. **准备环境**  
   - 确保运行主机内核 ≥ 5.10，已启用 `CONFIG_BPF_LSM` 与 `CONFIG_DEBUG_INFO_BTF`。  
   - 安装 `bpftool`、`clang`、`llvm`（用于编译 BPF 程序）。  

2. **克隆并构建**  
   ```bash
   git clone https://github.com/yeet-src/agent-lock.git
   cd agent-lock
   npm install            # 项目使用 JavaScript/Node 作为控制层
   make bpf                # 编译 BPF‑LSM 与 eBPF 监控程序
   ```

3. **配置沙箱目录**  
   在 `config.json` 中指定 AI 代理的工作根目录，例如：  
   ```json
   {
     "agentRoot": "/opt/ai/agent-workdir",
     "allowedPaths": ["/opt/ai/agent-workdir"]
   }
   ```

4. **启动守护进程**  
   ```bash
   sudo node src/daemon.js
   ```
   守护进程会把 BPF‑LSM 程序挂载到内核，随后启动目标 AI 代理（如 `codex-server`），并通过 eBPF 收集运行时事件。

5. **监控与调试**  
   - 使用自带的 Web UI（`http://localhost:8080`) 查看文件访问、系统调用、网络流量等实时统计。  
   - 通过 `bpftool prog show` 检查 BPF 程序状态，或使用 `bpftool map dump` 查看内部计数器。

> **小贴士**：在正式环境前，建议先在一个最小的目录（如 `/tmp/agent-test`）做 POC，确认 BPF 程序不会误拦截正常系统调用。

---

## 生产可用性评估  

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | 中等 | 项目已有 31 ⭐、5 forks，最近更新于 2026‑07‑06，代码以 JavaScript 为主，核心 BPF 部分相对独立。 |
| **依赖风险** | 中等 | 依赖 Linux 内核 BPF‑LSM 与 eBPF，需确保目标服务器满足内核版本与编译工具链要求；在非 Linux（如 Windows）上不可用。 |
| **运维成本** | 中等 | 需要维护 BPF 程序的兼容性（内核升级可能导致加载失败），以及守护进程的可靠性（建议使用 systemd 服务管理）。 |
| **安全审计** | 良好 | BPF‑LSM 在内核层面执行，理论上比用户态沙箱更安全，但仍需审计自定义 BPF 代码以防止潜在的内核崩溃或信息泄露。 |
| **适用场景** | 原型/内部工作流 | 非常适合研发团队快速验证 AI Agent 的文件/网络权限需求；在对安全合规要求极高的生产环境中，仍需进行完整的渗透测试与监控。 |

**结论**：`yeet-src/agent-lock` 已具备在内部研发或受控生产环境中使用的条件，关键在于做好内核兼容性检查、持续监控 BPF 程序运行状态，并在正式部署前完成安全评审。对需要在现有 AI 模型上快速加入安全沙箱的团队来说，它是一个成本低、实现快的实用选项。

## 🧭 Practical evaluation

**Value:** yeet-src/agent-lock helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 31 GitHub stars
- 5 forks
- updated 2026-07-06
- primary language: JavaScript
- 11 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 32/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 53/100 |
| recency | 40/100 |
| adoption | 29/100 |
| production | 50/100 |
| usefulness | 74/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/yeet-src/agent-lock) · [← Back to AI/ML](./README.md)</sub>
