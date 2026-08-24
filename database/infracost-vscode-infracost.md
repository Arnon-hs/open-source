# infracost/vscode-infracost

[![Stars](https://img.shields.io/github/stars/infracost/vscode-infracost?style=flat-square&color=yellow)](https://github.com/infracost/vscode-infracost/stargazers) [![Forks](https://img.shields.io/github/forks/infracost/vscode-infracost?style=flat-square&color=blue)](https://github.com/infracost/vscode-infracost/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> See cost estimates for Terraform right in your editor💰📉

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.8k |
| 🍴 **Forks** | 55 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-07-06 |
| 🔍 **Source** | github |

## 🏷️ Topics

`aws` `azure` `cloud-cost-estimates` `cost-estimation` `cost-management` `cost-optimization` `finops` `gcp` `google` `infrastructure-as-code` `shift-left` `terraform`

## 🎯 Categories

Database · DevOps/Infra

## 📝 Summary

### English

Here's a brief summary of the project:

**Project Summary:** infracost/vscode-infracost is an open-source project that provides cost estimates for Terraform directly within the Visual Studio Code editor, enabling teams to manage infrastructure costs more efficiently. This project offers a practical adoption path for teams looking to speed up data access and prototype database-backed applications with reduced custom plumbing. With high production readiness and strong ecosystem signals, it's suitable for serious pilots.

**Value:** The project helps teams persist, query, and move data with less custom plumbing, making it an attractive solution for managing persistence, speeding up data access, and prototyping database-backed applications.

**Adoption Path:** The practical adoption path involves evaluating the project through a small proof of concept and reviewing the README documentation. This approach allows teams to assess the project's feasibility and potential benefits before committing to a larger implementation.

**Production Readiness:** The project has high production readiness, with recent activity, adoption, and ecosystem signals indicating a strong and viable solution. However, it's essential to conduct a final review of the license, security posture, and active maintainers to ensure the project meets the team's requirements.

### Русский

Резюме проекта infracost/vscode-infracost:

Этот проект позволяет командам получать стоимостные оценки для Terraform прямо в своем редакторе, что помогает сократить необходимость в ручном проектировании и тестировании инфраструктуры. Типовой сценарий внедрения включает в себя управление сохранением данных, ускорение доступа к ним и прототипирование приложений с базами данных. Проект готов к внедрению в производстивную среду, имея сильные показатели активности, приёма и сигналы экосистемы, что делает его подходящей кандидатурой для серьезного пилота.

### 中文

**项目简介**  
`infracost/vscode-infracost` 是一款 VS Code 插件，能够在编辑 Terraform 文件时直接显示资源的成本估算，让开发者在编写基础设施代码的同时即刻了解费用影响，帮助团队在设计阶段就实现成本控制。  

**价值体现**  
- **成本可视化**：实时展示每个 Terraform 资源的预计费用，避免因资源选型不当导致的预算超支。  
- **提升效率**：无需切换到浏览器或 CLI，成本信息即嵌入编辑器，缩短审查和调优的反馈回路。  
- **促进协作**：团队成员可以在代码审查时直接看到成本变化，促进成本意识的统一。  

**典型接入方式**  
1. **安装插件**：在 VS Code Marketplace 搜索 “Infracost” 或使用命令 `code --install-extension infracost.infracost`。  
2. **配置 API Token**：在 Infracost 官网获取个人 API Token，写入项目根目录的 `.infracost/config.yml` 或在 VS Code 设置中填写。  
3. **初始化项目**：在终端执行 `infracost breakdown --path .` 生成 `infracost.json`，插件会自动读取并在编辑器侧栏或悬浮提示中展示费用。  
4. **CI 集成（可选）**：将 `infracost` CLI 加入 CI 流程，生成的成本报告可与 PR 评论同步，进一步实现自动化成本审查。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑06，项目最近一次提交，拥有 1,842 ⭐、55 🍴，主要语言 TypeScript，社区活跃。  
- **成熟度**：插件已在多个公开项目中使用，具备完整的文档和示例，支持最新的 Terraform 版本。  
- **风险评估**：暂无重大元数据风险；仍需对许可证（MIT）和安全依赖进行最终审查。总体而言，项目具备 **高** 的生产就绪度，适合作为正式环境的成本可视化工具进行试点或直接上线。

## 🧭 Practical evaluation

**Value:** infracost/vscode-infracost helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1842 GitHub stars
- 55 forks
- updated 2026-07-06
- primary language: TypeScript
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 69/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 83/100 |
| recency | 100/100 |
| adoption | 62/100 |
| production | 80/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/infracost/vscode-infracost) · [← Back to Database](./README.md)</sub>
