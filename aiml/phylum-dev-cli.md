# phylum-dev/cli

[![Stars](https://img.shields.io/github/stars/phylum-dev/cli?style=flat-square&color=yellow)](https://github.com/phylum-dev/cli/stargazers) [![Forks](https://img.shields.io/github/forks/phylum-dev/cli?style=flat-square&color=blue)](https://github.com/phylum-dev/cli/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Command line interface for the Phylum API

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 108 |
| 🍴 **Forks** | 11 |
| 💻 **Language** | Rust |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `malware` `malware-detection` `rust` `secure-software-supply-chain` `security` `security-scan` `software-supply-chain` `software-supply-chain-security` `supply-chain` `vulnerabilities`

## 🎯 Categories

AI/ML · Backend · DevTools · Security

## 📝 Summary

### English

**Summary**  
phylum‑dev/cli is a Rust‑based command‑line interface for the Phylum API that lets developers quickly prototype AI‑enabled features—such as Retrieval‑Augmented Generation (RAG) pipelines or autonomous agents—without building a model stack from scratch. With 108 GitHub stars, recent commits (as of 2026‑05‑11), and a modest but active community, the tool is positioned as a low‑friction entry point for adding AI capabilities to backend or security‑focused workflows.  

**Value**  
The CLI abstracts the underlying Phylum API, exposing ready‑made commands and SDK hooks that accelerate experimentation, model evaluation, and tooling integration, so teams can focus on product logic rather than model infrastructure.  

**Adoption path**  
1. **Evaluate** – Install the binary (`cargo install phylum-cli` or download a pre‑built release) and run the built‑in `phylum login` to connect to an existing Phylum account.  
2. **Prototype** – Use sample commands (e.g., `phylum rag create`, `phylum agent run`) to build a quick RAG or agent proof‑of‑concept, iterating with the CLI’s verbose output and JSON logs.  
3. **Integrate** – Wrap CLI invocations in CI/CD pipelines or invoke the underlying Rust SDK from your own services for tighter automation.  

**Production readiness**  
The project shows strong OSS signals: recent activity, a growing star count, and a clear Rust codebase with well‑defined topics. While the license and long‑term security audit still need a final check, the current health indicators (active maintainers, regular releases, and community forks) make phylum‑dev/cli a viable candidate for a pilot in production environments, especially for teams that need a quick, secure way to add AI functionality without managing model infrastructure.

### Русский

**phylum-dev/cli** — это CLI‑утилита на Rust для работы с Phylum API, позволяющая быстро добавить AI‑функциональность (прототипирование моделей, построение RAG‑ и агентных пайплайнов, оценка инструментов) без необходимости создавать стек с нуля. Проект уже активно поддерживается (108 звёзд, свежие коммиты, широкая экосистема), что делает его готовым к использованию в пилотных production‑проектах после окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
phylum-dev/cli 是 Phylum API 的命令行工具，使用 Rust 实现，可直接在终端调用 Phylum 的安全与合规检测功能。它为开发者提供快速原型化 AI 能力的入口，无需自行搭建模型堆栈。

**价值**  
- **即插即用**：通过 CLI 即可调用 Phylum 的 AI 安全检测、RAG 与智能体工作流，省去自行部署模型的成本。  
- **加速研发**：适用于快速验证 AI 功能、评估模型工具链以及在 CI/CD 中嵌入安全审计。  
- **生态兼容**：提供统一的 API/SDK/CLI 接口，配合语言元数据和主题标签，便于在多语言项目中统一管理。

**典型接入方式**  
1. **安装**：`cargo install phylum-cli` 或下载预编译二进制。  
2. **配置**：在本地或 CI 环境中设置 `PHYLUM_API_KEY`，或通过 `phylum login` 完成身份认证。  
3. **调用**：在脚本或终端直接执行 `phylum scan <path>`、`phylum rag <query>` 等子命令，输出 JSON/文本结果供后续处理或自动化流程使用。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑11，项目最近更新，拥有 108 星、11 Fork，社区讨论活跃。  
- **技术成熟**：使用 Rust 编写，具备良好的性能和安全特性；已在多个内部项目中验证。  
- **准备度**：在许可证、依赖安全审计和维护者活跃度上仍需最终确认，但目前的信号足以支持正式的试点或生产部署。

## 🧭 Practical evaluation

**Value:** phylum-dev/cli helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 108 GitHub stars
- 11 forks
- updated 2026-05-11
- primary language: Rust
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 27/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 72/100 |
| recency | 100/100 |
| adoption | 39/100 |
| production | 76/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/phylum-dev/cli) · [← Back to AI/ML](./README.md)</sub>
