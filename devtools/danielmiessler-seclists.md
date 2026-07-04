# danielmiessler/SecLists

[![Stars](https://img.shields.io/github/stars/danielmiessler/SecLists?style=flat-square&color=yellow)](https://github.com/danielmiessler/SecLists/stargazers) [![Forks](https://img.shields.io/github/forks/danielmiessler/SecLists?style=flat-square&color=blue)](https://github.com/danielmiessler/SecLists/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> SecLists is the security tester's companion. It's a collection of multiple types of lists used during security assessments, collected in one place. List types include usernames, passwords, URLs, sensitive data patterns, fuzzing payloads, web shells, and many more.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 71.9k |
| 🍴 **Forks** | 25k |
| 💻 **Language** | PHP |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-07-04 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

DevTools · Data · Security · Marketing

## 📝 Summary

### English

**Project Summary:**

SecLists is an open-source project that provides a comprehensive collection of security assessment lists, including usernames, passwords, URLs, and more. This project aims to help engineers save time in their daily development and review loops. With its strong adoption and recent activity, SecLists is a high-quality candidate for production use.

**Value:**

The primary value proposition of SecLists is to help engineers speed up their workflows, automate local engineering tasks, and improve Continuous Integration (CI) feedback. By providing a collection of pre-existing lists, developers can reduce the time spent on security assessments and focus on more critical tasks.

**Practical Adoption Path:**

To adopt SecLists, follow these steps:

1. **Evaluate and review the project**: Check the README file, documentation, and code quality to ensure it meets your project's requirements.
2. **Start with a small proof of concept**: Integrate SecLists into a small part of your project to test its feasibility and effectiveness.
3. **Assess the license and security posture**: Verify that the license and security posture align with your project's needs and standards.
4. **Monitor the project's activity and maintainers**: Keep an eye on the project's recent activity, maintainers, and community engagement to ensure its continued support and

### Русский

Резюме проекта danielmiessler/SecLists:

danielmiessler/SecLists - это открытое исходное ПО, которое помогает инженерам сократить время, затрачиваемое на ежедневные разработки и ревью. Этот проект представляет собой коллекцию различных типов списков, используемых во время безопасности оценок, собранных в одном месте. Внедрение проекта может включать ускорение разработки, автоматизацию локальных задач и улучшение обратной связи в CI.

Проект имеет высокий уровень готовности к production, подтверждаемый его активностью, приёмом и сигналами экосистемы. Для интеграции рекомендуется начать с небольшого proof of concept и проверки README.

### 中文

**项目简介**  
SecLists（danielmiessler/SecLists）是安全测试人员的必备资源库，汇集了用户名、密码、URL、敏感数据正则、模糊测试 payload、Web shell 等多种列表，帮助在渗透测试和安全评估时快速获取常用字典和样本。

**价值**  
- **节省时间**：提供即取即用的安全字典，避免团队自行搜集、维护列表。  
- **提升质量**：在代码审计、CI/CD 安全扫描、模糊测试等环节直接引用，提升检测覆盖率和准确性。  
- **统一标准**：统一的列表来源保证了团队内部使用的字典保持一致，降低误报/漏报风险。

**典型接入方式**  
1. **本地克隆**：在 CI 脚本或本地开发环境中 `git clone https://github.com/danielmiessler/SecLists.git`，直接读取所需子目录（如 `Passwords/`、`Fuzzing/`）。  
2. **子模块或包管理**：在项目的 `git submodule`、`npm`、`pip`（通过自定义脚本）或 `Dockerfile` 中引入，以保持与主仓库同步。  
3. **自动化脚本**：编写小工具在构建阶段下载最新的特定文件（例如 `curl -L https://raw.githubusercontent.com/danielmiessler/SecLists/master/Passwords/Common-Credentials.txt`），并喂给安全扫描工具或模糊测试框架。  

**生产可用性**  
- **活跃度**：2026‑07‑04 最近一次提交，71 k+ Stars、25 k+ Forks，社区活跃度高。  
- **成熟度**：作为 OSS 基础设施已被大量安全工具（Burp、nmap、ffuf 等）直接引用，具备高可靠性。  
- **集成风险**：暂无重大元数据风险，唯一需要关注的是许可证（MIT）兼容性以及后续维护者的响应速度。  
- **建议**：先在非关键环境做小范围 PoC（例如在 CI 中跑一次密码字典扫描），确认路径、更新频率与安全策略后即可在生产流水线中全面推广。  

综上，SecLists 具备 **高生产就绪度**，适合作为安全测试、代码审计和 CI 安全自动化的共享字典资源，快速提升开发与运维团队的安全检测效率。

## 🧭 Practical evaluation

**Value:** danielmiessler/SecLists helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 71907 GitHub stars
- 25047 forks
- updated 2026-07-04
- primary language: PHP

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 100/100 |
| stars | 100/100 |
| topics | 0/100 |
| outlook | 82/100 |
| quality | 85/100 |
| recency | 100/100 |
| adoption | 100/100 |
| production | 78/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/danielmiessler/SecLists) · [← Back to DevTools](./README.md)</sub>
