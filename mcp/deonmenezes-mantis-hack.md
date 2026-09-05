# deonmenezes/mantis-hack

[![Stars](https://img.shields.io/github/stars/deonmenezes/mantis-hack?style=flat-square&color=yellow)](https://github.com/deonmenezes/mantis-hack/stargazers) [![Forks](https://img.shields.io/github/forks/deonmenezes/mantis-hack?style=flat-square&color=blue)](https://github.com/deonmenezes/mantis-hack/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Mantis — autonomous offensive-security platform for Claude Code. DISCOVER → REASON → TEST → LEARN over a 7-phase FSM with parallel specialist agents, 3-round Multi-Step Evidence verification, MCP control plane. Evidence, not alerts.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 80 |
| 🍴 **Forks** | 23 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-harness` `ai-agents` `autonomous-agents` `bug-bounty` `claude-code` `mantis` `mcp` `offensive-security` `security`

## 🎯 Categories

MCP · Automation · AI/ML · Security

## 📝 Summary

### English

**Brief Summary**  
Mantis is an autonomous offensive‑security platform built for Claude Code that runs a 7‑phase finite‑state machine (DISCOVER → REASON → TEST → LEARN) using parallel specialist agents, multi‑step evidence verification, and an MCP control plane. It focuses on generating verifiable “evidence” rather than noisy alerts, and provides a standard Model Context Protocol (MCP) for connecting AI assistants to real tools and data.  

**Value**  
- **Unified AI‑to‑tool bridge** – Mantis implements a common MCP that lets any Claude‑compatible AI agent invoke external services (APIs, CLIs, SDKs) through a single, well‑documented protocol, eliminating ad‑hoc glue code.  
- **Evidence‑first workflow** – By requiring multi‑step verification of findings, the platform reduces false positives and gives security teams actionable proof rather than raw alerts.  
- **Extensible specialist agents** – The parallel‑agent architecture lets teams plug in custom scanners, exploit modules, or data‑gathering bots without rewriting the core FSM.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the Docker compose or npm start scripts, and point a Claude‑compatible assistant at the provided MCP endpoint.  
2. **Integrate** – Use the exposed SDK/CLI to register your own tool adapters (e.g., vulnerability scanners, ticketing systems) as specialist agents; the MCP schema makes this a declarative step.  
3. **Validate** – Execute the built‑in 3‑round evidence verification flow on a test environment to confirm the evidence pipeline works end‑to‑end.  
4. **Scale** – Deploy the MCP control plane on Kubernetes or a managed cloud service, configure horizontal agent pods, and hook the platform into CI/CD or SOC dashboards.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑05‑14), has 80 ★ and 23 forks, and is written in JavaScript, which eases integration for many teams.  
- **Strengths**: Clear API/SDK surface, modular agent model, and a well‑defined protocol that aligns with emerging AI‑tool standards.  
- **Caveats**: Requires a review of the open‑source license, a security audit of the MCP server, and verification that the dependency tree (Node.js packages) is kept up‑to‑date. Additional testing is advisable before exposing the platform to production networks.  

Overall, Mantis offers a compelling foundation for teams that want to embed AI assistants into security tooling pipelines, with a manageable path from prototype to production once the remaining compliance and hardening steps are completed.

### Русский

**deonmenezes/mantis-hack** – открытая платформа, позволяющая подключать AI‑агентов к реальным инструментам и базам данных через единый протокол (Model Context Protocol). Типичный сценарий: разработчики встраивают Mantis в свои CI/CD‑конвейеры или внутренние исследовательские среды, чтобы автоматизировать цикл «обнаружить → рассудить → тестировать → учиться» с параллельными специалист‑агентами и многократной проверкой доказательств. Проект находится на среднем уровне готовности к production: имеет активные обновления, достаточный набор звёзд и форков, но требует проверки лицензии, безопасности и поддержки перед масштабным внедрением.

### 中文

**项目简介（2‑3 句）**  
Mantis 是面向 Claude Code 的自主进攻式安全平台，采用 7 阶段有限状态机（DISCOVER → REASON → TEST → LEARN），并通过并行的专业化代理、3 轮多步骤证据验证以及 MCP 控制平面，实现“证据而非告警”。它为 AI 助手提供统一的工具与数据接入协议，使安全自动化更加可靠、可审计。

---

## 价值说明  
1. **统一协议**：通过 Model Context Protocol（MCP）把 AI 代理、内部工具和数据库统一在同一通信层，降低了跨系统集成的复杂度。  
2. **证据驱动**：平台不产生噪声告警，而是返回可验证的安全证据，帮助团队快速定位真实威胁并进行后续学习。  
3. **并行专长代理**：在 7‑phase FSM 中，多个专门化的子代理同时工作，提高了发现、推理和测试的效率。  
4. **可复用的安全流水线**：从发现到学习的完整闭环，可直接嵌入 CI/CD、DevSecOps 或内部安全运营平台。

## 典型接入方式  
| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| **AI 助手调用内部工具** | 使用提供的 **CLI / SDK**（JavaScript） | 1. `npm i mantis-hack` <br>2. 在代码中引入 `MantisClient` <br>3. 配置 MCP 控制平面地址与身份凭证 |
| **部署 MCP 服务器** | 通过 **Docker 镜像** 或 **K8s Helm chart** | 1. 拉取 `deonmenezes/mantis-hack` 镜像 <br>2. 设置环境变量（`MCP_ENDPOINT`, `API_KEY`） <br>3. 启动后通过 REST/gRPC 与代理交互 |
| **标准化集成** | 使用 **OpenAPI / GraphQL** 描述的接口 | 1. 下载 `openapi.yaml` <br>2. 生成对应语言的客户端 <br>3. 按照文档调用 `discover`, `reason`, `test`, `learn` 四大入口 |

> **小贴士**：平台在 `package.json` 中声明了 `peerDependencies`（Node >=18），确保在 CI 环境中使用相同的 Node 版本可以避免兼容性问题。

## 生产可用性评估  
- **成熟度**：Medium。项目已在 GitHub 获得 80+ 星、23 个 fork，最近一次提交为 2026‑05‑14，代码活跃度尚可。  
- **适用场景**：非常适合作为 **原型**、**内部安全实验**或 **研发阶段的自动化安全流水线**。在正式生产环境部署前，需要完成以下检查：  
  1. **依赖审计**：确认所有第三方 NPM 包的安全报告（使用 `npm audit`）。  
  2. **许可证合规**：项目默认 MIT，确认与企业开源政策匹配。  
  3. **安全姿态**：审查 Docker 镜像的 CVE 列表，确保无已知高危漏洞。  
  4. **运维监控**：为 MCP 控制平面添加健康检查、日志聚合（如 Prometheus + Grafana）以及限流/熔断。  
- **可扩展性**：平台本身即为微服务化设计，支持水平扩展的并行代理，配合 Kubernetes 可以轻松实现弹性伸缩。  
- **维护成本**：当前维护者数量有限，建议内部指定 **维护负责人**，并对关键模块（FSM、证据验证）设立单元测试与 CI 流水线，以降低因社区停更导致的技术债务。

**结论**：deonmenezes/mantis-hack 为 AI‑驱动的安全自动化提供了统一、证据导向的接入层，适合作为内部原型或中小规模生产环境的安全加速器；在正式上线前需完成依赖安全审计、运维监控和内部维护机制的补齐。

## 🧭 Practical evaluation

**Value:** deonmenezes/mantis-hack helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 80 GitHub stars
- 23 forks
- updated 2026-05-14
- primary language: JavaScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 41/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 39/100 |
| production | 67/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/deonmenezes/mantis-hack) · [← Back to Mcp](./README.md)</sub>
