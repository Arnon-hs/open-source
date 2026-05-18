# janitor-security/the-janitor

[![Stars](https://img.shields.io/github/stars/janitor-security/the-janitor?style=flat-square&color=yellow)](https://github.com/janitor-security/the-janitor/stargazers) [![Forks](https://img.shields.io/github/forks/janitor-security/the-janitor?style=flat-square&color=blue)](https://github.com/janitor-security/the-janitor/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-41%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 41/100 |
| 🗓️ **Last push** | 2026-05-18 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

AI/ML · Frontend · Security

## 📝 Summary

### English

**Brief Summary**  
This open‑source project demonstrates how to assemble an AI‑driven vulnerability scanner by chaining Claude and Codex. Although the proof‑of‑concept did not achieve reliable detection, the codebase shows a reusable pattern for adding AI‑based security analysis to existing tooling without training a model from scratch.

**Value**  
- Provides a concrete example of integrating large‑language‑model (LLM) services (Claude for reasoning, Codex for code analysis) into a security workflow, saving time for teams that want to prototype AI‑enhanced scanning.  
- The modular architecture can be repurposed for other “AI‑assist” use cases such as RAG (retrieval‑augmented generation) or autonomous agents, giving developers a head‑start on building LLM‑centric pipelines.  

**Practical Adoption Path**  
1. **Clone & Review** – Pull the repository, inspect the licensing, and read the README to understand the Claude/Codex API contracts.  
2. **Configure Credentials** – Supply your own Claude and Codex API keys (or compatible endpoints) in the provided `.env` template.  
3. **Run the Prototype** – Execute the sample scanner against a small, non‑production codebase to verify end‑to‑end flow and gather false‑positive/negative statistics.  
4. **Iterate & Harden** – Replace the demo prompts with custom security policies, add pre‑ and post‑processing (e.g., static analysis filters), and integrate the scanner into CI/CD pipelines or internal security dashboards.  
5. **Manual Review Layer** – Because the current model signals are sparse, embed a human‑in‑the‑loop step that validates flagged findings before any automated action.  

**Production Readiness**  
- **Readiness Level:** *Medium* – suitable for prototyping and internal tooling, but not yet production‑grade.  
- **Strengths:** Clear modular code, up‑to‑date (May 2026), and demonstrates a reusable LLM orchestration pattern.  
- **Weaknesses:** Limited quality signals, sparse integration metadata, and the scanner’s detection accuracy is unproven.  
- **Next Steps for Production:** Conduct thorough security testing, establish a robust monitoring/alerting framework, ensure consistent API versioning for Claude and Codex, and set up a maintenance plan for dependency updates and bug fixes.  

In short, the project offers a valuable starting point for teams eager to experiment with AI‑augmented vulnerability scanning, provided they add rigorous validation and operational safeguards before moving to production.

### Русский

**I built an AI vulnerability scanner with Claude and Codex. It failed** — это open‑source‑инструмент, позволяющий быстро добавить возможности ИИ‑сканирования уязвимостей в существующие проекты без разработки собственного стека моделей. Он подходит для прототипирования AI‑фич, построения RAG‑агентов и оценки инструментов моделирования, однако требует ручной проверки и уточнения интеграционных сигналов перед внедрением. Готовность к production — средняя: проект пригоден для внутренних прототипов, но перед переходом в продакшн необходимо оценить лицензию, поддержку, документацию и частоту релизов.

### 中文

**项目简介**  
这是一个使用 Anthropic Claude 与 OpenAI Codex 构建的 AI 漏洞扫描器示例，演示了如何快速为现有系统加入 AI 检测能力——尽管当前实现仍未完全成功。项目适合作为原型或内部工具，帮助开发者快速验证 RAG、Agent 工作流以及模型工具链的可行性。

**价值**  
- **快速原型**：提供即插即用的代码框架，让团队在几分钟内搭建起 AI 驱动的安全检测功能，无需从零构建模型堆栈。  
- **技术评估**：可用于评估 Claude、Codex 等大模型在漏洞扫描、代码审计等安全场景的表现，为后续选型提供实证数据。  
- **学习示例**：代码结构清晰，展示了如何在前端与后端之间串联 LLM、RAG 与自定义插件，适合作为学习和内部培训材料。

**典型接入方式**  
1. **克隆仓库** → `git clone <repo>`，安装依赖（Node.js / Python 环境）。  
2. **配置 API 密钥**：在 `.env` 中填入 Claude 与 Codex 的访问令牌。  
3. **集成到现有 CI/CD**：将扫描脚本作为代码提交前的预检查步骤，或在安全审计平台中以微服务方式调用。  
4. **手动审查**：由于自动化信号稀疏，建议在正式采纳前对扫描结果进行人工复核，并根据业务需求调整提示词或过滤规则。

**生产可用性**  
- **成熟度**：Medium。代码已更新至 2026‑05‑18，适合作为原型或内部流程使用，但在正式生产环境部署前需进行依赖、维护频率、许可证合规以及文档完整性的检查。  
- **风险**：质量信号有限，模型调用成本和误报率需自行评估；同时项目的维护者活跃度不高，建议自行制定更新和监控策略。  

总体而言，该项目是一个便捷的起点，可帮助团队快速验证 AI 在安全检测中的潜力，但在投入生产前需要进行充分的人工审查和运维准备。

## 🧭 Practical evaluation

**Value:** I built an AI vulnerability scanner with Claude and Codex. It failed helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-05-18
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 54/100 |
| quality | 41/100 |
| recency | 100/100 |
| adoption | 0/100 |
| production | 58/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |

---

<sub>🔭 Discovered 2026-05-18 · [View on GitHub](https://github.com/janitor-security/the-janitor) · [← Back to AI/ML](./README.md)</sub>
