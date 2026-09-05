# fossology/fossology

[![Stars](https://img.shields.io/github/stars/fossology/fossology?style=flat-square&color=yellow)](https://github.com/fossology/fossology/stargazers) [![Forks](https://img.shields.io/github/forks/fossology/fossology?style=flat-square&color=blue)](https://github.com/fossology/fossology/network) [![Language](https://img.shields.io/badge/lang-HTML-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> FOSSology is an open source license compliance software system and toolkit.  As a toolkit you can run license, copyright and export control scans from the command line.  As a system, a database and web ui are provided to give you a compliance workflow. License, copyright and export scanners are tools used in the workflow.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 985 |
| 🍴 **Forks** | 616 |
| 💻 **Language** | HTML |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`compliance` `compliance-automation` `compliance-check` `fossology` `license` `license-checking` `license-management` `license-scan` `oss` `spdx` `spdx-licenses`

## 🎯 Categories

Automation · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
FOSSology is an open‑source license‑compliance platform that combines a command‑line toolkit for scanning licenses, copyrights and export controls with a full‑stack web UI and database to manage a compliance workflow. It automates repetitive manual checks, lets you schedule scans, and integrates the results into a traceable, repeatable process. With a large user community and active development, it is ready for production pilots.

**Value**  
- **Automation of tedious tasks** – Scans that normally require manual inspection of source files are performed automatically, reducing human error and freeing engineering time.  
- **End‑to‑end workflow** – The web UI and database provide issue tracking, review, and reporting, turning raw scan data into actionable compliance decisions.  
- **Extensibility** – The CLI tools can be chained with CI/CD pipelines or other security/quality tools, enabling a repeatable, auditable compliance pipeline.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, follow the README to spin up the Docker‑compose stack, and run a few sample scans on a small codebase.  
2. **Pilot Integration** – Connect the CLI to your CI system (e.g., Jenkins, GitHub Actions) to schedule nightly scans of critical repositories.  
3. **Workflow Customization** – Use the web UI to define review gates, assign reviewers, and generate compliance reports that feed into release approvals.  
4. **Scale‑out** – Deploy the production‑grade PostgreSQL backend, enable LDAP/SSO for access control, and integrate with your artifact repository for continuous compliance enforcement.

**Production Readiness**  
- **Activity & Community** – 985 stars, 616 forks, frequent commits (last update 2026‑05‑14) and a broad ecosystem of topics indicate a healthy, maintained project.  
- **Maturity** – The combination of a stable web UI, database persistence, and command‑line tools has been used in large‑scale deployments, suggesting a high level of reliability.  
- **Risks** – Integration documentation is sparse; initial setup may require troubleshooting and validation of infrastructure costs (e.g., database sizing, storage for scan artifacts). Starting with a small PoC mitigates these risks before full production rollout.

### Русский

FOSSology — это открытая система и набор инструментов для автоматизации проверки лицензий, авторских прав и экспортного контроля: сканеры запускаются из командной строки, а веб‑интерфейс с базой данных обеспечивает полноценный workflow‑менеджмент. Типичное внедрение начинается с небольшого proof‑of‑concept, где сканеры подключаются к существующей CI/CD‑цепочке для регулярного анализа артефактов и последующего формирования отчётов в веб‑консоли. По уровню готовности к продакшну проект считается «high»: активные обновления, широкое принятие (985 ★, 616 forks) и надёжная экосистема позволяют использовать его в серьёзных пилотных проектах.

### 中文

**项目简介**  
FOSSology 是一套开源的许可证合规系统和工具集，既提供命令行的许可证、版权与出口管制扫描器，也提供基于数据库和 Web UI 的完整合规工作流，帮助组织在代码审计和发布前自动化完成合规检查。

**价值**  
- **降低重复人工**：把手工的许可证、版权和出口管制检查全部交给可编排的扫描工具，显著减少审计人员的工作量。  
- **可编排的流水线**：扫描器可以通过脚本或 CI/CD 任务调用，便于把合规检查嵌入现有的构建、发布或安全流水线，实现“一键合规”。  
- **统一管理与追溯**：Web UI 与后端数据库记录每次扫描结果，提供历史查询、报告导出和审批流，方便审计和合规追溯。

**典型接入方式**  
1. **小规模概念验证**：在本地或 CI 环境中克隆仓库，使用 `fossology` 提供的 CLI（如 `fossology-cli`）执行 `fossology scan`，检查输出的 SPDX/JSON 报告是否符合预期。  
2. **CI/CD 集成**：在 Jenkins、GitHub Actions、GitLab CI 等流水线中添加步骤，调用 `fossology-cli` 或直接使用 REST API 将代码提交到 FOSSology 服务器进行扫描，并根据返回的合规状态决定是否继续构建。  
3. **全流程部署**：在内部服务器或容器平台（Docker/K8s）部署 FOSSology 的 Web UI 与数据库，配置 LDAP/SSO 进行身份管理，然后通过 UI 创建项目、定义扫描策略、安排定时任务，实现企业级的合规管理平台。

**生产可用性**  
- **成熟度高**：项目活跃，最近一次提交在 2026‑05‑14，拥有 985+ stars、616+ forks，社区活跃度和第三方采用情况良好。  
- **功能完整**：提供许可证、版权、出口管制三大扫描器，支持多种输出格式（SPDX、CycloneDX、JSON），并具备任务调度与结果可视化。  
- **部署准备度**：官方提供 Docker 镜像和 Helm Chart，支持快速上手；但元数据中未明确标注完整的 CI 集成示例，建议先在小范围 PoC 中验证安装脚本、网络访问和权限配置后，再推广至生产环境。  

总体来看，FOSSology 已具备在企业生产环境中作为许可证合规核心组件的条件，只要做好前期的部署验证和集成脚本编写，即可实现高效、可重复的合规自动化。

## 🧭 Practical evaluation

**Value:** fossology/fossology helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 985 GitHub stars
- 616 forks
- updated 2026-05-14
- primary language: HTML
- 11 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 70/100 |
| stars | 64/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 79/100 |
| recency | 80/100 |
| adoption | 65/100 |
| production | 69/100 |
| usefulness | 90/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/fossology/fossology) · [← Back to Automation](./README.md)</sub>
