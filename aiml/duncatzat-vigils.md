# duncatzat/vigils

[![Stars](https://img.shields.io/github/stars/duncatzat/vigils?style=flat-square&color=yellow)](https://github.com/duncatzat/vigils/stargazers) [![Forks](https://img.shields.io/github/forks/duncatzat/vigils?style=flat-square&color=blue)](https://github.com/duncatzat/vigils/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> A local control plane for AI agents — see what they do, approve what matters, keep secrets out. Rust + Tauri + Chrome MV3.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 332 |
| 🍴 **Forks** | 20 |
| 💻 **Language** | Rust |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-security` `ai-agents` `audit-log` `desktop` `llm` `local-first` `pii` `rust` `sandbox` `tauri`

## 🎯 Categories

AI/ML · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Vigils is an open‑source, Rust‑based local control plane for AI agents that lets you observe agent actions, approve critical steps, and keep sensitive data out of the loop. Built with Tauri and a Chrome MV3 extension, it provides a lightweight UI for monitoring, gating, and managing agent workflows without needing to assemble a full model stack from scratch.  

**Value**  
- **Safety & Governance** – By surfacing every agent decision and requiring explicit approval for high‑impact actions, Vigils reduces the risk of unintended behavior and data leakage.  
- **Speed to Prototype** – Developers can plug in existing models or APIs and immediately gain a managed execution environment, accelerating the creation of RAG pipelines, autonomous agents, or other AI‑augmented features.  
- **Low Overhead** – Because it runs locally and leverages Rust’s performance and Tauri’s cross‑platform UI, the solution adds minimal latency and operational complexity compared with cloud‑only control planes.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided `cargo build` and Tauri launch scripts, and follow the README to connect a single model endpoint (e.g., OpenAI, Ollama).  
2. **Define Guardrails** – Use the UI or configuration files to specify which actions require approval (e.g., external API calls, file writes).  
3. **Iterate on Agent Logic** – Integrate your existing agent code via the simple Rust/HTTP interface, test end‑to‑end flows, and adjust the gating rules as needed.  
4. **Scale Internally** – Once the PoC is stable, package the binary for internal distribution, add CI checks for the Rust dependencies, and optionally extend the Chrome MV3 extension for broader user access.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑06‑25) and has a modest community (≈332 ★, 20 forks), indicating usable code but limited large‑scale validation.  
- **Suitability**: Ideal for internal prototypes, sandboxed RAG/agent workflows, or as a safety layer during early‑stage AI feature development.  
- **Considerations Before Production**:  
  * Verify the integration steps for your specific model stack (the docs are sparse).  
  * Perform dependency audits and lockfile reviews to mitigate Rust crate supply‑chain risks.  
  * Conduct load testing to ensure the local control plane can handle the expected concurrency.  
  * Plan for monitoring and fallback mechanisms if the control plane itself becomes a bottleneck.  

In short, Vigils offers a practical, safety‑first way to experiment with AI agents locally; it can be adopted quickly for proof‑of‑concepts, but production deployment should include thorough integration testing, dependency vetting, and performance validation.

### Русский

**vigils** — это локальная контрольная плоскость для AI‑агентов, позволяющая наблюдать их действия, одобрять только нужные операции и изолировать конфиденциальные данные; проект реализован на Rust с UI‑слоем Tauri и поддержкой Chrome MV3. Он отлично подходит для быстрого прототипирования AI‑фич, построения RAG‑ или агентных пайплайнов и оценки новых моделей, при этом требует небольшого proof‑of‑concept и проверки README перед более широким внедрением. Готовность к продакшну — средняя: проект стабилен для внутренних прототипов, но требует дополнительного аудита зависимостей и уточнения интеграционного пути перед использованием в критически важных системах.

### 中文

**项目简介（2‑3 句）**  
Vigils（duncatzat/vigils）是基于 Rust、Tauri 与 Chrome MV3 实现的本地 AI 代理控制平面，能够实时监控、批准或拦截代理的行为，并在运行时对敏感信息进行过滤。它让开发者无需从零搭建模型堆栈，就能快速为产品或内部工具加入可审计的 AI 能力。

**价值**  
- **安全审计**：所有 AI 代理的请求与响应都在本地拦截、展示，关键操作需要人工批准，防止模型泄露或产生不当输出。  
- **快速原型**：提供即插即用的本地控制面板，配合 RAG、工具调用等工作流即可实现可视化调试，显著缩短 AI 功能的研发周期。  
- **降低依赖**：不必自行部署完整的模型服务，直接在本地环境中使用已有模型或云端 API，即可获得完整的审计与治理能力。

**典型接入方式**  
1. **阅读 README**，确认系统需求（Rust ≥ 1.70、Node.js、Tauri CLI）。  
2. **克隆仓库** → `cargo build --release` 编译后生成本地可执行文件。  
3. **配置模型后端**：在 `config.yaml` 中填写 OpenAI、Claude、Gemini 等 API 密钥或本地模型路径。  
4. **启动控制平面**：运行生成的二进制或通过 `tauri dev` 启动 UI，随后在业务代码中把对模型的 HTTP/JSON 调用指向 `http://localhost:PORT/v1/…`（Vigils 会代理转发并在 UI 中展示）。  
5. **验证**：在 UI 中观察请求、批准或拒绝，确保业务流程符合安全策略后，再将代理调用迁入生产环境。

**生产可用性**  
- **成熟度**：GitHub ★332、20 fork，最近一次提交在 2026‑06‑25，代码活跃度中等。  
- **适用场景**：非常适合作为内部原型、RAG/Agent 工作流的安全审计层或在受控环境下的 AI 功能验证。  
- **上线注意**：  
  - 依赖 Rust 与 Tauri，需评估团队对这些技术栈的熟悉度。  
  - 生产环境应对其本地代理服务做高可用包装（如使用 systemd 服务或容器化），并在防火墙/网络策略上限制对外 API 的直接访问。  
  - 通过 CI 检查更新频率，锁定依赖版本，防止突发的 breaking change。  

综上，Vigils 在 **安全审计 + 快速原型** 方面提供了显著价值，适合作为内部或受限环境的 AI 控制层；在生产环境使用时，需要完成小规模 POC、完整的依赖审计以及高可用包装后方可投入正式业务。

## 🧭 Practical evaluation

**Value:** duncatzat/vigils helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 332 GitHub stars
- 20 forks
- updated 2026-06-25
- primary language: Rust
- 10 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 48/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/duncatzat/vigils) · [← Back to AI/ML](./README.md)</sub>
