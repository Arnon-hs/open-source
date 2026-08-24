# DMOJ/online-judge

[![Stars](https://img.shields.io/github/stars/DMOJ/online-judge?style=flat-square&color=yellow)](https://github.com/DMOJ/online-judge/stargazers) [![Forks](https://img.shields.io/github/forks/DMOJ/online-judge?style=flat-square&color=blue)](https://github.com/DMOJ/online-judge/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> A modern open-source online judge and contest platform system.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 447 |
| 💻 **Language** | Python |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`coding-competitions` `coding-interviews` `dmoj` `dmoj-judge` `online-judge` `programming-challenge` `programming-contests` `python`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
DMOJ/online‑judge is a modern, open‑source platform for running programming contests and automated code evaluation. Built in Python, it provides a full‑stack judge system with problem management, submission handling, and a web UI, making it a ready‑to‑use alternative to proprietary contest platforms.

**Value**  
The system streamlines daily development and review cycles by letting teams embed automated code‑checking into pull‑request pipelines, CI jobs, or local testing environments. It reduces manual review effort, accelerates feedback loops, and offers a consistent, reproducible way to validate code quality across projects.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Fork the repo, run the Docker‑compose setup, and verify basic judge functionality with a small set of internal problems.  
2. **README & CI Integration** – Follow the existing README to configure a minimal CI job (e.g., GitHub Actions) that submits code to a local DMOJ instance and checks results.  
3. **Pilot Deployment** – Deploy a shared instance in a staging environment, import a curated problem set, and invite a pilot team to use it for code reviews and contest‑style assessments.  
4. **Scale & Customize** – Add custom problem types, integrate with internal authentication (LDAP/OIDC), and expose APIs for broader tooling.

**Production Readiness**  
The project shows strong OSS maturity: 1.1 k stars, 447 forks, recent commits (as of 2026‑05‑14), and active community support. Its Python‑centric stack and clear documentation make deployment straightforward, and the existing Docker images simplify environment replication. While the license, security posture, and maintainer activity still require a final audit, the overall signals indicate the system is ready for a serious pilot in production environments.

### Русский

DMOJ/online-judge — современная open‑source платформа для онлайн‑соревнований и автоматической проверки кода, позволяющая ускорить циклы разработки и ревью за счёт быстрой локальной валидации решений и интеграции с CI. Обычно её внедряют в виде небольшого proof‑of‑concept: добавляют репозиторий в проект, настраивают базовый набор задач в README и проверяют работу через тестовые контейнеры, после чего расширяют конфигурацию под свои контесты. По оценке готовности к продакшну проект находится на высоком уровне: активные коммиты, более 1100 звёзд, широкое использование в сообществе и стабильный стек на Python делают его надёжным кандидатом для пилотного запуска.

### 中文

**价值**  
DMOJ/online-judge 是一套现代化的开源在线评测与竞赛平台，能够帮助工程团队在日常开发、代码评审以及 CI 流程中实现自动化判题、批量测试和即时反馈，从而大幅缩短开发与回归验证的时间，提高整体工作效率。

**典型接入方式**  
1. **快速 PoC**：先在本地或测试环境克隆仓库，按照 README 完成依赖安装（Python 3 + PostgreSQL），运行 `docker-compose up` 启动完整的 Judge、Web 与数据库服务。  
2. **CI 集成**：在 CI（GitHub Actions、GitLab CI 等）中调用提供的 CLI 或 REST API，将提交的代码推送到 DMOJ，获取判题结果并将评分/错误信息回写到构建日志或 PR 评论。  
3. **业务嵌入**：通过平台的 GraphQL/REST 接口，将题目、提交、评测报告等数据与自有系统（如内部学习平台、代码托管平台）进行同步，实现统一的题库管理和评测视图。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑14，项目仍在持续更新，拥有 1 173+ 星、447+ Fork，社区贡献活跃。  
- **技术成熟**：核心使用 Python 编写，配套 PostgreSQL 与 Docker 部署方案，易于在容器化环境中弹性扩容。  
- **风险可控**：暂无重大元数据风险，但仍建议在正式上线前完成许可证合规审查、依赖安全扫描以及维护者响应能力的二次确认。  
- **适合试点**：基于上述信号，可视为高准备度的 OSS 候选，适合先在小范围内部项目或研发团队进行试点验证，验证后再推广至全公司或公开使用。

## 🧭 Practical evaluation

**Value:** DMOJ/online-judge helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1173 GitHub stars
- 447 forks
- updated 2026-05-14
- primary language: Python
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 66/100 |
| stars | 65/100 |
| topics | 100/100 |
| outlook | 52/100 |
| quality | 65/100 |
| recency | 20/100 |
| adoption | 66/100 |
| production | 52/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/DMOJ/online-judge) · [← Back to Misc](./README.md)</sub>
