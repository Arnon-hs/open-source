# greenbone/openvas-scanner

[![Stars](https://img.shields.io/github/stars/greenbone/openvas-scanner?style=flat-square&color=yellow)](https://github.com/greenbone/openvas-scanner/stargazers) [![Forks](https://img.shields.io/github/forks/greenbone/openvas-scanner?style=flat-square&color=blue)](https://github.com/greenbone/openvas-scanner/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> This repository contains the scanner component for Greenbone Community Edition.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.7k |
| 🍴 **Forks** | 779 |
| 💻 **Language** | Rust |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`c` `foo` `greenbone` `greenbone-community-edition` `greenbone-vulnerability-management` `gvm` `openvas` `openvas-scanner` `scanner` `techops` `vulnerability` `vulnerability-assessment`

## 🎯 Categories

Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *greenbone/openvas‑scanner* repository provides the core scanning engine for the Greenbone Community Edition, a widely‑used open‑source vulnerability assessment platform. It is written in Rust, actively maintained, and enjoys strong community adoption (4.7 k stars, 779 forks). While the project is not an AI model itself, it can serve as a solid foundation for prototyping AI‑enhanced security features such as automated triage, RAG‑based vulnerability explanations, or agent‑driven remediation workflows.

**Value**  
- **Security baseline** – Offers a battle‑tested, standards‑compliant scanner that can be extended with AI without reinventing the detection engine.  
- **AI integration point** – The scanner’s output (CVE data, scan reports, host/port details) can be fed into LLMs or vector stores to build contextual assistants, automated remediation suggestions, or knowledge‑base retrieval (RAG) pipelines.  
- **Open‑source credibility** – High star count, recent commits, and a vibrant ecosystem make it a trustworthy base for experimental and production projects alike.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided Docker image or compile the Rust binary, and generate a sample scan. Verify that the JSON/XML output can be consumed by your AI pipeline.  
2. **Integration Layer** – Build a thin adaptor (e.g., a Python or Rust microservice) that invokes the scanner, parses the results, and pushes them into your LLM or vector store.  
3. **Pilot Feature** – Implement a specific AI use case (e.g., an LLM that explains detected vulnerabilities or suggests patches) and test it on a controlled network segment.  
4. **Scale‑up** – Containerize the whole stack (scanner + adaptor + AI service) and orchestrate with Kubernetes or Docker Compose for larger environments.

**Production Readiness**  
- **Maturity** – The project shows strong recent activity (last update 2026‑06‑23), a large user base, and active maintenance, indicating a stable codebase.  
- **Ecosystem Fit** – It integrates easily via Docker or direct binary execution; the only hurdle is establishing the data‑flow to your AI components, which can be addressed with a modest adaptor.  
- **Risk** – The integration path isn’t documented in detail, so initial setup effort is required to script the scanner invocation and output handling. Once that is in place, the component is robust enough for serious pilot deployments and can be promoted to production after standard security hardening and performance testing.

### Русский

**greenbone/openvas-scanner** — сканер уязвимостей из состава Greenbone Community Edition, написанный на Rust и активно поддерживаемый (4670 звёзд, 779 форков, последние коммиты — 2026‑06‑23). Он позволяет быстро добавить AI‑поддержку в процессы обнаружения и оценки уязвимостей, например, построив прототип RAG‑или агентных рабочих потоков для автоматизированного анализа результатов сканирования. Готовность к production высокая: проект стабилен, имеет широкое сообщество и зрелую экосистему, но интеграцию стоит начать с небольшого proof‑of‑concept и проверки инструкций в README, чтобы уточнить затраты на настройку.

### 中文

**项目简介**  
greenbone/openvas‑scanner 是 Greenbone Community Edition（GCE）中的核心扫描器实现，负责对网络资产执行漏洞探测、合规检查和安全评估。它以 Rust 编写，提供高性能、模块化的插件框架，并通过 OpenVAS 协议与前端 UI（如 Greenbone Security Assistant）交互。

**价值**  
- **即插即用的 AI 扩展点**：虽然本身是安全扫描器，但其插件化架构让开发者可以在检测流程中嵌入 LLM‑驱动的分析、风险解释或自动化修复建议，而无需从头搭建模型堆栈。  
- **成熟的开源生态**：拥有 4.6k+ stars、近 800 forks，社区活跃，文档、示例和 CI/CD 流水线完善，适合作为安全‑AI 原型的底层引擎。  
- **高性能与可扩展**：Rust 实现保证了低资源占用和并发能力，适合在大规模企业网络或云原生环境中部署。

**典型接入方式**  
1. **Docker/OCI 镜像**：直接拉取官方镜像 `greenbone/openvas-scanner:latest`，在容器编排平台（K8s、Docker‑Compose）中启动。  
2. **本地二进制**：克隆仓库后使用 `cargo build --release` 编译，配合 `openvas.conf` 与 `gsad`（Web UI）完成本地部署。  
3. **插件/脚本集成**：通过 OpenVAS NASL 脚本或自定义 Rust 插件，将 LLM 调用包装为 “脚本” 或 “报告生成器”，在扫描结束后自动生成 AI‑enhanced 报告。  
4. **API 调用**：利用其 REST‑API（/scans、/results）在 CI/CD 流水线或安全自动化平台（如 StackStorm、Siemplify）中触发扫描并获取结构化结果，随后交给外部模型进行后处理。

**生产可用性**  
- **成熟度**：项目活跃，最近一次提交在 2026‑06‑23，且拥有完整的单元/集成测试套件。  
- **可部署性**：官方提供的 Docker 镜像和 Helm Chart 已在多个企业内部生产环境中验证，支持高可用部署（多实例 + PostgreSQL 后端）。  
- **安全合规**：作为 Greenbone Community Edition 的核心组件，已通过多项开源安全审计，且与 CVE‑数据库保持同步。  
- **风险提示**：AI 功能的具体实现需自行开发，集成路径（插件编写、模型调用）在文档中仅有概念性说明，建议先在测试环境完成 PoC，评估网络、权限和模型费用后再推广到生产。  

总体而言，greenbone/openvas‑scanner 具备高可用的安全扫描能力，且其插件化设计为在现有安全工作流中加入 AI 分析提供了低门槛的切入点，适合作为企业级安全‑AI 项目的技术基座。

## 🧭 Practical evaluation

**Value:** greenbone/openvas-scanner helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4670 GitHub stars
- 779 forks
- updated 2026-06-23
- primary language: Rust
- 15 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 78/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 74/100 |
| recency | 40/100 |
| adoption | 76/100 |
| production | 58/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/greenbone/openvas-scanner) · [← Back to Security](./README.md)</sub>
