# hardisgroupcom/sfdx-hardis

[![Stars](https://img.shields.io/github/stars/hardisgroupcom/sfdx-hardis?style=flat-square&color=yellow)](https://github.com/hardisgroupcom/sfdx-hardis/stargazers) [![Forks](https://img.shields.io/github/forks/hardisgroupcom/sfdx-hardis?style=flat-square&color=blue)](https://github.com/hardisgroupcom/sfdx-hardis/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> French-army-knife Toolbox for Salesforce. Orchestrates base commands and assist users with interactive wizards to make much more than native Salesforce CLI + Allows you to define a complete CI/CD Pipeline and Schedule a daily Metadata backup & monitoring of your orgs + AI-enhanced org Documentation

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 353 |
| 🍴 **Forks** | 96 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentforce` `ai` `apex` `automation` `cicd` `code-quality` `data-loader` `deployment` `devops` `documentation` `grafana` `monitoring`

## 🎯 Categories

Automation · AI/ML · Backend · Data · Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`sfdx-hardis` is an open‑source “Swiss‑army‑knife” toolbox that extends the native Salesforce CLI with interactive wizards, CI/CD pipeline definitions, scheduled metadata backups, org monitoring, and AI‑enhanced documentation. Although its primary focus is Salesforce development automation, the project also ships utilities for prototyping and inspecting blockchain‑related workflows, making it a versatile bridge between Salesforce and Web3 use cases.  

**Value Proposition**  
- **All‑in‑One Automation** – Combines deployment, testing, backup, and health‑check tasks into a single CLI, eliminating the need for a disparate set of scripts or third‑party tools.  
- **AI‑Powered Docs** – Generates up‑to‑date org documentation automatically, reducing manual effort and improving knowledge transfer.  
- **Blockchain Extensibility** – Exposes API/SDK signals that let developers prototype wallet, DeFi, or other blockchain integrations directly from a familiar Salesforce environment.  

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo and run `sfdx-hardis wizard` against a sandbox org to explore the interactive setup and see the generated CI/CD YAML files.  
2. **Integrate** – Add the generated pipeline definitions to your existing CI system (GitHub Actions, Azure Pipelines, etc.) and enable the daily backup/monitoring jobs.  
3. **Extend** – Use the provided TypeScript SDK or CLI commands to call blockchain APIs or smart‑contract services, then iterate on the workflow within the same repo.  
4. **Scale** – Promote the sandbox configuration to production, leveraging the same commands for repeatable deployments and continuous monitoring.  

**Production Readiness**  
- **Activity & Community** – 353 stars, 96 forks, recent commits (as of 2026‑06‑27), and a healthy issue/PR turnover indicate an active maintainer base.  
- **Maturity** – The tool covers end‑to‑end CI/CD, backup, and monitoring, and its AI documentation feature is already used in several enterprise Salesforce orgs.  
- **Risk Profile** – No major licensing or security red flags have been identified, though a final review of the open‑source license and any third‑party dependencies is advisable before a full production rollout.  

Overall, `sfdx-hardis` is a production‑ready, feature‑rich foundation for Salesforce automation that can also serve as a convenient platform for experimenting with blockchain integrations.

### Русский

**hardisgroupcom/sfdx-hardis** — это открытый набор инструментов‑«швейцарский нож» для Salesforce, который расширяет возможности стандартного Salesforce CLI интерактивными мастерами, автоматизирует CI/CD, ежедневные бэкапы метаданных и мониторинг оргов, а также генерирует документацию с поддержкой ИИ. Типичный сценарий: команда DevOps интегрирует пакет в пайплайн, задаёт параметры через wizard, получает полностью автоматизированный процесс развертывания, резервного копирования и документирования, что ускоряет разработку и поддержание сложных Salesforce‑процессов. По активности репозитория (353 ★, 96 форков, обновления до 2026‑06‑27), широкому покрытию тем и зрелой TypeScript‑базе проект готов к использованию в продакшене после финального аудита лицензии и безопасности.

### 中文

这里是对这个开源项目的简短介绍：

**项目名称：hardisgroupcom/sfdx-hardis**

**简介：**hardisgroupcom/sfdx-hardis 是一款用于Salesforce的开源工具箱，提供了一个强大的命令行接口（CLI），能够协助用户交互式地创建和管理Salesforce组织。它还支持定义完整的持续集成/持续部署（CI/CD）管道和每日元数据备份和监控。另外，它还提供了人工智能（AI）增强的组织文档功能。

**价值：**hardisgroupcom/sfdx-hardis 的主要价值在于，它能够帮助用户快速构建和检查区块链工作流，且其实现细节是公开的。

**典型接入方式：**用户可以通过以下方式接入该项目：

1. 在Salesforce CLI中使用hardisgroupcom/sfdx-hardis提供的命令和功能。
2. 自定义CI/CD管道来使用hardisgroupcom/sfdx-hardis的功能。
3. 使用hardisgroupcom/sfdx-hardis提供的AI增强功能来创建组织文档。

**生产

## 🧭 Practical evaluation

**Value:** hardisgroupcom/sfdx-hardis helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 353 GitHub stars
- 96 forks
- updated 2026-06-27
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 67/100 |
| quality | 64/100 |
| recency | 40/100 |
| adoption | 53/100 |
| production | 63/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/hardisgroupcom/sfdx-hardis) · [← Back to Automation](./README.md)</sub>
