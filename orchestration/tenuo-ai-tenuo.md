# tenuo-ai/tenuo

[![Stars](https://img.shields.io/github/stars/tenuo-ai/tenuo?style=flat-square&color=yellow)](https://github.com/tenuo-ai/tenuo/stargazers) [![Forks](https://img.shields.io/github/forks/tenuo-ai/tenuo?style=flat-square&color=blue)](https://github.com/tenuo-ai/tenuo/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> High-performance capability authorization engine for AI agents. Cryptographically attenuated warrants, task-scoped authority, verifiable offline. Rust core.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 76 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | Rust |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`a2a` `agents` `ai-agents` `capabilities` `cryptography` `langchain` `langgraph` `llm` `mcp` `rust` `security`

## 🎯 Categories

Orchestration · MCP · AI/ML · Security

## 📝 Summary

### English

**Brief Summary**  
Teneo is a high‑performance, Rust‑based capability‑authorization engine designed for AI agents. It issues cryptographically attenuated warrants that grant task‑scoped authority, can be verified offline, and integrates via an API/SDK/CLI for Web3 and DeFi prototyping.  

**Value**  
By turning permissions into verifiable, cryptographic tokens, Teneo lets developers prototype and audit blockchain‑driven workflows without exposing sensitive keys or relying on a live network. The engine’s offline verification and fine‑grained, task‑scoped warrants make it ideal for building wallet interfaces, DeFi primitives, or any AI‑agent that must act under provable authority constraints.  

**Practical Adoption Path**  
1. **Explore the SDK/CLI** – clone the repo, run the provided examples, and use the Rust crate (or generated bindings) to issue and validate warrants in a sandbox.  
2. **Integrate with your stack** – wrap the API in your service layer (e.g., a microservice that issues warrants for AI agents) and connect it to your existing blockchain node or RPC endpoint.  
3. **Test end‑to‑end** – simulate typical Web3 flows (wallet creation, token transfer, DeFi contract interaction) and verify that the warrants are correctly attenuated and that offline verification succeeds.  
4. **Hardening** – perform a security audit of the crate, pin dependencies, and add monitoring for any future upstream changes.  

**Production Readiness**  
Teneo sits at a **medium** readiness level: it is actively maintained (last commit 2026‑07‑02), has modest adoption (76 ★, 5 forks) and a clean Rust codebase, making it suitable for prototypes and internal tooling. Before production deployment, teams should:  

- Conduct a formal security review of the cryptographic primitives and licensing.  
- Verify that the dependency chain is stable and that no critical CVEs affect the crate.  
- Establish a maintenance plan (e.g., subscribe to release notifications or fork for custom patches).  

With those checks in place, Teneo can be safely promoted from sandbox experimentation to a core component of Web3/AI orchestration pipelines.

### Русский

Резюме проекта tenuo-ai/tenuo:

tenuo-ai/tenuo - это высокопроизводительное движок авторизации возможностей для агентов AI, позволяющий создавать криптографически защищенные гарантии, скопированные по задачам и проверяемые в офлайн-режиме. Этот проект предназначен для прототипирования или инспектирования блокчейн-работфлоу с открытыми подробностями реализации. tenuo-ai/tenuo подходит для прототипирования или внутренних рабочих процессов, но требует проверки зависимостей и обслуживания перед выпуском в производство.

### 中文

**项目简介（2‑3 句话）**  
tenuo‑ai/tenuo 是基于 Rust 实现的高性能能力授权引擎，专为 AI 代理提供加密可验证的授权凭证（warrant），支持任务级别的权限范围并可离线校验。它通过密码学衰减（cryptographically attenuated）技术，将授权信息安全地绑定到区块链工作流中，帮助开发者快速原型化或审计 Web3/DeFi 场景。

**价值**  
- **安全可验证**：授权凭证在链下即可通过密码学方式验证，避免了对中心化服务的依赖。  
- **任务粒度**：可为每一次 AI 任务生成独立的、受限的权限，降低权限滥用风险。  
- **快速原型**：开放的 API/SDK/CLI 让开发者能够在几行代码内构建完整的区块链工作流或钱包/DeFi 功能。  

**典型接入方式**  
1. **API/SDK**：通过 Rust crate（`tenuo`）或生成的语言绑定（如 Python、JS）直接在业务代码中调用 `create_warrant`、`verify_warrant` 等函数。  
2. **CLI**：使用 `tenuo-cli` 在本地或 CI 环境中生成、签名、验证 warrant，适合脚本化的 DevOps 流程。  
3. **REST/GRPC 网关**（可选）：项目提供的轻量网关可将内部库包装为 HTTP/GRPC 接口，方便非 Rust 项目集成。  

**生产可用性**  
- **成熟度**：当前评分 66/100，GitHub 76 星、5 个分支，最近一次更新为 2026‑07‑02，代码活跃度尚可。  
- **适用场景**：非常适合作为原型、内部工具或安全审计平台的授权层；在正式生产环境使用前，需要完成以下检查：  
  - 依赖审计（确保所有第三方 crate 已更新且无已知 CVE）。  
  - 许可证合规（确认项目使用的开源许可证与公司政策匹配）。  
  - 维护者沟通（确认核心维护者的响应速度和后续计划）。  
- **风险**：暂无重大元数据风险，但安全姿态和长期维护仍需进一步评估。  

综上，tenuo 为 AI‑Agent 与区块链交互提供了轻量且可验证的授权机制，接入门槛低，适合作为原型或内部服务的安全基石，经过充分审查后亦可逐步推广至生产环境。

## 🧭 Practical evaluation

**Value:** tenuo-ai/tenuo helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 76 GitHub stars
- 5 forks
- updated 2026-07-02
- primary language: Rust
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 40/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 55/100 |
| recency | 40/100 |
| adoption | 34/100 |
| production | 53/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/tenuo-ai/tenuo) · [← Back to Orchestration](./README.md)</sub>
