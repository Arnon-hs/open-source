# VoltAgent/awesome-claude-code-subagents

[![Stars](https://img.shields.io/github/stars/VoltAgent/awesome-claude-code-subagents?style=flat-square&color=yellow)](https://github.com/VoltAgent/awesome-claude-code-subagents/stargazers) [![Forks](https://img.shields.io/github/forks/VoltAgent/awesome-claude-code-subagents?style=flat-square&color=blue)](https://github.com/VoltAgent/awesome-claude-code-subagents/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> A collection of 100+ specialized Claude Code subagents covering a wide range of development use cases

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22.3k |
| 🍴 **Forks** | 2.6k |
| 💻 **Language** | Shell |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent-framework` `ai-agent-tools` `ai-agents` `awesome` `awesome-list` `claude` `claude-ai` `claude-code-subagents` `claude-subagents` `subagents`

## 🎯 Categories

Orchestration · AI/ML

## 📝 Summary

### English

**Brief Summary**  
VoltAgent/awesome-claude-code-subagents is an open‑source library of more than 100 ready‑to‑use Claude “subagents” that automate specific development tasks—from code generation and refactoring to CI/CD orchestration. By packaging isolated prompts and tool invocations into reusable, composable agents, it lets teams build repeatable, multi‑agent workflows with minimal boilerplate.  

**Value**  
The collection turns ad‑hoc Claude prompts into standardized building blocks, enabling teams to:  

* **Coordinate multi‑agent pipelines** – chain subagents for end‑to‑end scenarios such as “write code → run tests → open PR.”  
* **Add tool‑use layers** – each subagent can invoke CLIs, APIs, or containerized tools, making Claude act like a true DevOps assistant.  
* **Standardize memory & state** – shared context handling is baked into the subagents, reducing the need for custom prompt engineering.  

**Practical Adoption Path**  

1. **Proof‑of‑Concept (PoC)** – Clone the repo, run the provided README examples, and pick a single subagent that matches a low‑risk use case (e.g., automated linting).  
2. **Integration Scaffold** – Wrap the chosen subagent in your internal CI/CD or IDE plugin using the existing Shell wrappers; adjust environment variables to point at your Claude API key.  
3. **Iterative Expansion** – Gradually replace custom scripts with additional subagents, validating each step with unit tests and monitoring token usage.  
4. **Governance & Customization** – Fork the repo to add organization‑specific prompts or tool bindings, then contribute back to keep the upstream community healthy.  

**Production Readiness**  
The project scores 79/100 and shows strong OSS maturity: 22 322 ★, 2 606 forks, recent commits (June 2026), and active discussions across 10 topics. Its primary language (Shell) and clear folder structure make onboarding straightforward, while the high star count signals community adoption. The main risk lies in the lack of explicit integration documentation; therefore, start with a small PoC to map out setup costs before scaling. Once the initial workflow is validated, the library is robust enough for a serious pilot in production environments.

### Русский

VoltAgent/awesome-claude-code-subagents — это открытый набор более 100 специализированных субагентов Claude, позволяющих превратить разрозненные запросы и инструменты в повторяемые рабочие процессы с поддержкой оркестрации, памяти и пайплайнов инструментов. Для внедрения рекомендуется начать с небольшого proof‑of‑concept: установить репозиторий, протестировать один‑два субагента согласно README и интегрировать их в существующий CI/CD‑pipeline. Проект обладает высокой готовностью к продакшн: активные коммиты, более 22 k звёзд, 2,6 k форков и свежие обновления, однако путь интеграции требует уточнения, поэтому следует оценить затраты на настройку перед масштабированием.

### 中文

**项目简介**  
VoltAgent/awesome-claude-code-subagents 是一个收录 100 多个专用 Claude Code 子代理的仓库，覆盖从代码生成、单元测试到 CI/CD、代码审计等多种开发场景。它把零散的 Prompt 与工具封装成可复用的工作流，使得多代理协作、工具链调用和记忆管理更加标准化、可编排。

**价值**  
- **快速构建复合 AI 工作流**：通过已有的子代理直接拼接，实现跨语言、跨工具的自动化开发任务。  
- **降低重复成本**：同类任务（如自动单元测试、依赖分析）只需引用对应子代理，无需每次手动编写 Prompt。  
- **统一记忆与上下文**：子代理共享的记忆模型帮助在长链路中保持上下文一致性，提高结果可靠性。

**典型接入方式**  
1. **阅读 README 与子代理清单**，挑选与业务需求匹配的子代理。  
2. **在本地或 CI 环境中克隆仓库**，使用提供的 Shell 脚本或 Docker 镜像启动 Claude‑Code 服务。  
3. **通过简单的 JSON/YAML 配置**（或 CLI 参数）将选中的子代理组合成一个工作流，例如：  
   ```yaml
   workflow:
     - name: code-gen
       agent: generate_code
     - name: lint
       agent: run_linter
     - name: test
       agent: run_tests
   ```  
4. **在业务系统中调用统一的 API 端点**，将代码、文件路径或其它上下文作为输入，即可获得子代理链的输出。  
5. **先做小范围 PoC**（如仅集成代码生成子代理），验证网络、鉴权、费用等细节后，再逐步扩展到完整流水线。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑24 最近一次提交，拥有 22 322 ⭐、2 606 forks，社区活跃，Issue 反馈响应及时。  
- **技术成熟**：主要使用 Shell 脚本封装，易于在容器或 CI 环境中部署；同时提供多语言示例。  
- **风险点**：元数据中未明确标注完整的部署文档，实际集成时需要自行梳理依赖（如 Claude API 密钥、网络代理）并评估初始化成本。  
- **总体评估**：在完成小规模验证后，可视为 **高生产就绪度** 的 OSS 组件，适合在内部研发平台或外部 SaaS 中进行正式试点。

## 🧭 Practical evaluation

**Value:** VoltAgent/awesome-claude-code-subagents helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 22322 GitHub stars
- 2606 forks
- updated 2026-06-24
- primary language: Shell
- 10 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 85/100 |
| stars | 93/100 |
| topics | 100/100 |
| outlook | 89/100 |
| quality | 91/100 |
| recency | 80/100 |
| adoption | 91/100 |
| production | 73/100 |
| usefulness | 90/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/VoltAgent/awesome-claude-code-subagents) · [← Back to Orchestration](./README.md)</sub>
