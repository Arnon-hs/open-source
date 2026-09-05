# open-delivery-spec/cli

[![Stars](https://img.shields.io/github/stars/open-delivery-spec/cli?style=flat-square&color=yellow)](https://github.com/open-delivery-spec/cli/stargazers) [![Forks](https://img.shields.io/github/forks/open-delivery-spec/cli?style=flat-square&color=blue)](https://github.com/open-delivery-spec/cli/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-39%2F100-brightgreen?style=flat-square)](#)

> Mentioned in dev.to article (tag github): Your Git History Already Knows Which Code Is AI-Written. Your CI Should Too.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 39/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | devto |

## 🏷️ Topics

`devto` `github` `ai` `devops` `opensource`

## 🎯 Categories

AI/ML · DevOps/Infra

## 📝 Summary

### English

**Project Summary:**
Your Git History Already Knows Which Code Is AI-Written. Your CI Should Too. is an open-source project that leverages existing Git history to identify AI-written code, enabling teams to integrate AI capabilities into their workflows without starting from scratch.

**Value Proposition:**
This project offers a unique value proposition by allowing teams to prototype AI features, build robust agent workflows, and evaluate model tooling without requiring a blank model stack. By tapping into the metadata stored in Git history, teams can gain insights into AI-written code, streamlining their development processes and improving collaboration.

**Practical Adoption Path:**
The adoption path for this project involves a manual inspection of the integration signals, as they can be sparse in the discovered metadata. This requires careful evaluation before adoption to ensure the project meets the team's needs. Once integrated, teams can leverage the project's capabilities to build and refine their AI workflows, starting with prototypes and internal workflows before scaling to production.

**Production Readiness:**
The project has a medium production readiness score, indicating that it is suitable for use in prototypes or internal workflows, but requires dependency and maintenance checks before deployment in production environments. This is due to the limited quality signals and the need for careful evaluation of the project's license, maintenance, documentation,

### Русский

**Your Git History Already Knows Which Code Is AI‑Written. Your CI Should Too** — это open‑source‑инструмент, который автоматически извлекает метаданные из истории Git, определяя, какой код был сгенерирован ИИ, и предоставляет эти сигналы CI‑pipeline для быстрой проверки и контроля. Типичный сценарий: команда подключает библиотеку к своему CI, получает отчёты о «AI‑written» фрагментах, использует их для прототипирования RAG‑агентов, оценки новых моделей и построения воркфлоу с минимальной потребностью в обучении собственных моделей. Готовность к production — средняя: решение подходит для прототипов и внутренних процессов, но требует ручной проверки качества метаданных и оценки лицензии, поддержки и частоты релизов перед масштабным внедрением.

### 中文

**项目简介**  
Your Git History Already Knows Which Code Is AI‑Written. Your CI Should Too. 是一个开源工具，能够在 CI 流水线中自动识别代码是否由 AI 生成，并在此基础上提供原型化的 RAG、Agent 等 AI 功能，帮助团队在已有 Git 元数据的情况下快速加入 AI 能力，而无需从零训练模型。

**价值**  
- **利用已有 Git 历史**：直接读取 commit、author、diff 等元信息，判断 AI 生成代码，省去额外的检测模型训练成本。  
- **快速原型**：提供即插即用的 RAG/Agent 工作流模板，适合内部实验、概念验证或评估新模型工具。  
- **降低风险**：在 CI 中提前捕获 AI 代码，可配合审计、合规和代码质量检查，防止未经审查的 AI 代码进入主分支。

**典型接入方式**  
1. **在 CI 配置文件中引入**（如 GitHub Actions、GitLab CI、Jenkins）：  
   ```yaml
   steps:
     - uses: actions/checkout@v3
     - name: Run AI‑code detector
       uses: your-org/ai-code-detector@v1
       with:
         repo_path: ${{ github.workspace }}
         output: detection_report.json
   ```  
2. **读取检测报告**，在后续步骤中根据 `confidence`、`file_path` 等元数据决定是否阻止合并、触发审查或启动 RAG/Agent 流程。  
3. **可选扩展**：将检测结果写入 GitHub Checks API、Slack 通知或自定义审计系统，实现全链路可视化。

**生产可用性**  
- **成熟度**：目前评分 42/100，属于 **Medium** 级别。适合内部原型、研发实验或对 AI 代码合规性有基本需求的团队。  
- **使用前检查**：项目维护频率较低，元数据提取信号稀疏，建议在正式环境前进行手动审查和充分的单元/集成测试。  
- **依赖与运维**：仅依赖标准 Git 命令和 Python 环境，部署成本低；但需关注许可证兼容性、社区活跃度以及后续的 bug 修复和安全更新。  

综上，该工具在 **快速评估 AI 代码风险** 与 **在现有 CI 中嵌入 AI 功能** 方面具备显著价值，适合作为内部实验平台或合规审计的第一层防护；在生产环境使用时，请做好额外的质量和安全审查。

## 🧭 Practical evaluation

**Value:** Your Git History Already Knows Which Code Is AI-Written. Your CI Should Too. helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-07-02
- 5 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 63/100 |
| outlook | 50/100 |
| quality | 40/100 |
| recency | 80/100 |
| adoption | 0/100 |
| production | 52/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 70/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/open-delivery-spec/cli) · [← Back to AI/ML](./README.md)</sub>
