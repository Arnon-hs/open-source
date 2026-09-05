# daaain/claude-code-log

[![Stars](https://img.shields.io/github/stars/daaain/claude-code-log?style=flat-square&color=yellow)](https://github.com/daaain/claude-code-log/stargazers) [![Forks](https://img.shields.io/github/forks/daaain/claude-code-log?style=flat-square&color=blue)](https://github.com/daaain/claude-code-log/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> A Python CLI tool that converts Claude Code transcript JSONL files into readable HTML / Markdown format.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 90 |
| 💻 **Language** | Python |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Documents

## 📝 Summary

### English

**Project Summary:**

daaain/claude-code-log is an open-source Python CLI tool that converts Claude Code transcript JSONL files into readable HTML/Markdown format, facilitating the integration of AI capabilities without starting from scratch. This tool is particularly useful for prototyping AI features, building RAG or agent workflows, and evaluating model tooling. With its medium production readiness score, it's suitable for internal workflows or proof-of-concepts, requiring careful dependency and maintenance checks before deployment.

**Value Proposition:**

The primary value proposition of daaain/claude-code-log lies in its ability to simplify the integration of AI capabilities, allowing developers to focus on building and evaluating AI features without the need to establish a comprehensive AI model stack from scratch. This makes it an attractive solution for developers looking to prototype AI features or build agent workflows, as well as for those seeking to evaluate model tooling.

**Practical Adoption Path:**

To adopt daaain/claude-code-log, follow these steps:

1. **Evaluate the tool**: Assess the tool's feasibility and potential impact on your project or workflow.
2. **Read the README**: Familiarize yourself with the tool's documentation, instructions, and best practices.
3. **Start with a small proof of concept**: Test the

### Русский

Резюме проекта daaain/claude-code-log:

Дааain/claude-code-log - это бесплатный инструмент командной строки на Python, который преобразует JSONL-файлы транскриптов Claude Code в читаемый HTML/Markdown-формат. Этот инструмент позволяет добавлять функции AI без создания собственного моделирующего стека. Он особенно полезен для прототипирования функций AI, построения RAG или агентных потоков, а также оценки инструментов моделирования.

### 中文

**项目简介**  
`daaain/claude-code-log` 是一个基于 Python 的命令行工具，能够把 Claude Code 生成的 transcript JSONL 文件快速转换为可阅读的 HTML 或 Markdown 文档，方便开发者对对话内容进行审阅、归档或进一步加工。

**价值**  
- **快速落地 AI 功能**：无需自行搭建模型栈，只需把 Claude 的对话记录转成结构化文档，即可用于原型验证、RAG（检索增强生成）或 Agent 工作流的调试与评审。  
- **提升可视化与可维护性**：HTML/Markdown 输出让对话历史在代码库、文档系统或内部 Wiki 中直观呈现，便于团队协作与审计。  
- **开箱即用的原型工具**：轻量级依赖（纯 Python）和简单的 CLI 接口，使其成为内部实验或 PoC 项目的理想配套工具。

**典型接入方式**  
1. **本地快速试用**  
   ```bash
   pip install claude-code-log
   claude-code-log input.jsonl --format html > transcript.html
   ```  
   直接在终端生成 HTML/Markdown，查看或提交到代码审查。  

2. **CI/CD 流程集成**  
   在 CI 脚本中加入转换步骤，将最新的 Claude transcript 自动转为 Markdown 并推送到文档仓库，实现对话记录的持续同步。  

3. **RAG/Agent 工作流**  
   将生成的 Markdown 作为知识库文档导入向量数据库（如 Pinecone、FAISS），配合检索模块实现基于历史对话的上下文增强。  

**生产可用性**  
- **成熟度**：项目已有 1125+ Stars、90+ Forks，活跃更新至 2026‑06‑30，代码质量和社区反馈良好，适合作为内部原型或业务中小规模的生产工具。  
- **依赖与维护**：仅依赖标准 Python 库和少量轻量级第三方包，易于审计。建议在正式上线前进行一次依赖安全扫描（如 pip-audit）并确认许可证兼容性。  
- **风险与准备**：目前缺乏完整的生产级监控与异常恢复机制，建议在关键业务中加入错误捕获、日志上报以及回滚方案；同时确保有内部维护者负责定期升级。  

总体而言，`daaain/claude-code-log` 在原型开发和内部工作流自动化场景下具备 **中等** 的生产就绪度，经过少量的安全与运维审查后即可投入到正式环境使用。

## 🧭 Practical evaluation

**Value:** daaain/claude-code-log helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1125 GitHub stars
- 90 forks
- updated 2026-06-30
- primary language: Python

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 49/100 |
| stars | 65/100 |
| topics | 0/100 |
| outlook | 68/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 60/100 |
| production | 67/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/daaain/claude-code-log) · [← Back to Documents](./README.md)</sub>
