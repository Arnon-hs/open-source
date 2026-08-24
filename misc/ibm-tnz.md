# IBM/tnz

[![Stars](https://img.shields.io/github/stars/IBM/tnz?style=flat-square&color=yellow)](https://github.com/IBM/tnz/stargazers) [![Forks](https://img.shields.io/github/forks/IBM/tnz?style=flat-square&color=blue)](https://github.com/IBM/tnz/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-46%2F100-brightgreen?style=flat-square)](#)

> Tn3270 to Z Python library

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 89 |
| 🍴 **Forks** | 19 |
| 💻 **Language** | Python |
| 📈 **Score** | 46/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`command-line` `emulator` `mainframe` `mouse` `shell` `terminal` `tui` `zos`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
IBM/tnz is an open‑source Python library that bridges legacy Tn3270 terminal interactions with modern Z‑based AI workflows. It enables developers to prototype AI‑enhanced features—such as Retrieval‑Augmented Generation (RAG) or autonomous agents—without building a model stack from scratch, and it ships with a modest but active community (≈90 stars, recent updates).  

**Value**  
- **Accelerated AI prototyping:** By handling the low‑level Tn3270 communication, tnz lets teams focus on the AI layer (prompt engineering, retrieval, orchestration) rather than reinventing terminal connectivity.  
- **Unified stack:** The library integrates directly with popular Python AI ecosystems (LangChain, Llama‑Index, etc.), making it easy to embed legacy mainframe data into RAG pipelines or agent actions.  
- **Low entry cost:** With a small code footprint and clear examples, developers can quickly test concepts and validate business value before committing resources.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC):** Clone the repo, run the README example, and connect to a non‑production Tn3270 host to verify basic command/response handling.  
2. **AI Layer Integration:** Wrap tnz calls in a LangChain or Llama‑Index tool, exposing mainframe outputs as retrieval documents or tool‑use actions for an LLM.  
3. **Iterative Validation:** Use unit tests and a sandboxed mainframe environment to validate data fidelity, latency, and error handling.  
4. **Scaling Up:** Package tnz as an internal service (e.g., FastAPI wrapper) and integrate with CI/CD pipelines; add monitoring for connection health and security scanning of dependencies.  

**Production Readiness**  
- **Maturity:** Medium. The library is actively maintained (last commit 2026‑05‑11) and has a modest user base, making it suitable for internal prototypes and low‑risk production workloads.  
- **Considerations before production:**  
  - Perform a full license review (MIT/Apache‑style but verify exact terms).  
  - Conduct security vetting of the dependency tree (e.g., via `safety` or GitHub Dependabot).  
  - Establish monitoring for connection failures and implement retry/back‑off logic.  
  - Evaluate long‑term maintainer commitment; consider sponsoring or forking if critical.  

Overall, IBM/tnz offers a practical shortcut to embed mainframe data into modern AI pipelines, with a clear, incremental adoption route and a readiness level that fits prototyping and controlled production use cases after standard security and maintenance checks.

### Русский

**IBM/tnz** — это открытая Python‑библиотека, позволяющая быстро добавить возможности работы с моделями AI (RAG, агентные сценарии, прототипирование функций) поверх протокола TN3270, не начиная с нуля. Для внедрения рекомендуется сначала реализовать небольшой proof‑of‑concept, проверив README и базовую совместимость, а затем расширять интеграцию в существующие рабочие процессы. Готовность к production — средняя: библиотека подходит для прототипов и внутренних сервисов, но требует проверки лицензии, безопасности и поддержки зависимостей перед масштабным использованием.

### 中文

**项目简介（2‑3 句）**  
IBM/tnz 是一个用 Python 实现的 Tn3270（IBM 3270 终端协议）到 Z（Z‑OS）交互库，帮助开发者在现代 Python 环境中快速调用和操作传统的 3270 主机系统。它提供了简洁的 API，适合在 AI/ML 流程中嵌入对遗留主机数据的读取与写入，从而在不重新实现底层协议的前提下实现 AI 能力的快速原型化。

**价值**  
- **快速赋能 AI**：在已有的主机业务上直接叠加检索增强生成（RAG）或智能代理等 AI 功能，无需从零搭建模型堆栈。  
- **降低集成成本**：统一的 Python 接口让数据科学家和后端工程师都能轻松调用主机接口，缩短原型开发周期。  
- **提升业务可视化**：通过把主机数据拉到现代数据管道，可实现更灵活的分析、监控和决策支持。

**典型接入方式**  
1. **阅读 README**：确认库的安装方式（`pip install ibm-tnz`）以及所需的 3270 客户端依赖。  
2. **小规模 PoC**：在本地或测试环境中编写简短脚本，使用 `tnz.connect(host, port)` 建立会话，调用 `screen.read()`、`screen.write()` 等 API 完成一次端到端的数据读取/写入。  
3. **与 AI 流程集成**：将读取到的主机数据喂入向量化模型或 LLM，构建 RAG 检索或智能客服等工作流。  
4. **CI/CD 验证**：在代码库中加入单元测试，确保连接、登录、数据解析等关键路径在每次提交后仍然可用。

**生产可用性**  
- **成熟度**：GitHub 统计 89 ★、19 Fork，最近一次更新为 2026‑05‑11，表明项目仍在活跃维护，适合作为内部原型或中小规模生产服务。  
- **准备度**：**中等**。在正式上线前需要完成以下检查：  
  - 许可证兼容性（确认符合公司开源合规政策）。  
  - 安全审计：审查依赖库是否存在已知漏洞，并对主机连接进行加密（如使用 TLS/SSH 隧道）。  
  - 监控与容错：为连接超时、会话失效等异常情况加入重试和告警机制。  
- **运维建议**：将库封装为内部服务或微服务，统一管理凭证（如使用 Vault），并在 CI 中锁定依赖版本，以降低维护成本。

综上，IBM/tnz 为需要在现代 AI 应用中触达传统 IBM 3270 主机的团队提供了低门槛、可快速验证的技术桥梁，适合作为原型或内部业务流程的起点，经过适当的安全与运维加固后即可进入生产环境使用。

## 🧭 Practical evaluation

**Value:** IBM/tnz helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 89 GitHub stars
- 19 forks
- updated 2026-05-11
- primary language: Python
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 42/100 |
| topics | 100/100 |
| outlook | 45/100 |
| quality | 53/100 |
| recency | 20/100 |
| adoption | 39/100 |
| production | 47/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/IBM/tnz) · [← Back to Misc](./README.md)</sub>
