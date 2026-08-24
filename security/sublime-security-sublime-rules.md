# sublime-security/sublime-rules

[![Stars](https://img.shields.io/github/stars/sublime-security/sublime-rules?style=flat-square&color=yellow)](https://github.com/sublime-security/sublime-rules/stargazers) [![Forks](https://img.shields.io/github/forks/sublime-security/sublime-rules?style=flat-square&color=blue)](https://github.com/sublime-security/sublime-rules/network) [![Language](https://img.shields.io/badge/lang-YAML-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-46%2F100-brightgreen?style=flat-square)](#)

> Sublime rules for email attack detection, prevention, and threat hunting.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 367 |
| 🍴 **Forks** | 100 |
| 💻 **Language** | YAML |
| 📈 **Score** | 46/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`email-security` `phishing` `threat-hunting`

## 🎯 Categories

Security

## 📝 Summary

### English

**Project Summary:** 
The sublime-security/sublime-rules project provides open-source, AI-driven email attack detection, prevention, and threat hunting capabilities for Sublime. This project offers a value proposition by enabling users to add AI capabilities without starting from scratch, making it ideal for prototyping AI features or building workflows. However, its production readiness is medium due to potential integration complexities and maintenance requirements.

**Value Proposition:** 
The project's value lies in its ability to quickly add AI-driven security capabilities to users' existing workflows, saving time and resources. This is particularly useful for organizations looking to prototype AI features or build internal workflows without investing in a comprehensive AI model stack.

**Practical Adoption Path:** 
To adopt this project, users should start by manually inspecting the integration process to ensure a smooth setup. This may involve validating the setup cost and potential dependencies before committing to production use. Once the integration path is clear, users can leverage the project's AI capabilities to enhance their email security posture.

**Production Readiness:** 
The project's production readiness is rated as medium, indicating that while it is useful for prototyping or internal workflows, it may require additional validation and maintenance checks before being deployed in a production environment. This is due to the potential complexity of integration and the need to ensure that

### Русский

Резюме:

Sublime-security/sublime-rules - это открытый проект, предназначенный для обнаружения, предотвращения и поиска угроз в электронной почте, используя правила, которые можно интегрировать с помощью машинного обучения. Этот проект идеально подходит для прототипирования функций AI, создания рабочих процессов RAG или агентов, а также оценки инструментов моделирования. Проект готов к использованию в прототипах или внутренних рабочих процессах, но требует тщательного проверки и поддержки перед внедрением в производство.

### 中文

**项目简介**  
`sublime-security/sublime-rules` 是一套基于 YAML 编写的 Sublime 规则库，专注于电子邮件攻击的检测、拦截和威胁狩猎。它提供了可直接复用的检测逻辑，帮助安全团队在已有的邮件安全平台上快速加入 AI‑辅助的威胁识别能力，而无需从零构建模型堆栈。

**价值**  
- **快速原型**：通过现成的规则集合，即可在几分钟内部署基础的 AI 检测功能，适合安全团队进行概念验证或内部演示。  
- **支持 RAG/Agent 工作流**：规则可作为检索增强生成（RAG）或安全智能体（Agent）的“知识源”，为后续的上下文推理提供结构化信号。  
- **降低模型门槛**：不必自行训练或调优模型，直接利用社区维护的规则即可获得初步的 AI 辅助检测效果。  

**典型接入方式**  
1. **规则导入**：将仓库中的 `*.yaml` 文件复制或通过 Git 子模块引入到现有的邮件安全平台（如 Proofpoint、Microsoft Defender for Office 365、或自建的 SIEM）中。  
2. **适配适配器**：编写一个轻量的适配器脚本（Python/Go），读取 YAML 规则并转换为平台支持的过滤表达式或检测策略。  
3. **手动审查**：在正式启用前，安全分析师需对每条规则进行业务审查，确认其匹配条件、误报率以及与现有策略的冲突情况。  
4. **监控与调优**：上线后通过日志/报警平台监控规则触发频率，依据实际误报/漏报情况迭代规则或加入自定义阈值。  

**生产可用性**  
- **成熟度**：评分 55/100，属于“中等”成熟度。规则库已获得 367 颗星、100 次 fork，且最近一次更新在 2026‑07‑02，活跃度尚可。  
- **适用场景**：非常适合作为 **原型**、内部 **威胁狩猎** 或 **实验性 AI 功能** 的起点；在生产环境使用前，需要完成以下检查：  
  - **依赖审计**：确认 YAML 解析库、适配器脚本的版本兼容性。  
  - **维护计划**：制定规则更新的同步机制（如定期 `git pull`），防止因社区停更导致规则过时。  
  - **误报评估**：通过小规模流量或历史邮件样本进行回测，确保误报率在可接受范围。  
- **风险**：元数据中集成信号稀疏，缺乏直接的插件或 API，接入成本主要体现在手动审查和适配代码的编写上。  

**结论**  
`sublime-security/sublime-rules` 是一套高质量的邮件安全规则集合，能够帮助安全团队快速实现 AI 辅助的检测原型。若在生产环境使用，建议先在受控环境进行充分验证，并建立规则同步与维护流程后再推广至全量部署。

## 🧭 Practical evaluation

**Value:** sublime-security/sublime-rules helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 367 GitHub stars
- 100 forks
- updated 2026-07-02
- primary language: YAML
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 55/100 |
| topics | 38/100 |
| outlook | 49/100 |
| quality | 55/100 |
| recency | 40/100 |
| adoption | 53/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/sublime-security/sublime-rules) · [← Back to Security](./README.md)</sub>
