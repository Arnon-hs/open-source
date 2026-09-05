# umihico/docker-selenium-lambda

[![Stars](https://img.shields.io/github/stars/umihico/docker-selenium-lambda?style=flat-square&color=yellow)](https://github.com/umihico/docker-selenium-lambda/stargazers) [![Forks](https://img.shields.io/github/forks/umihico/docker-selenium-lambda?style=flat-square&color=blue)](https://github.com/umihico/docker-selenium-lambda/network) [![Language](https://img.shields.io/badge/lang-Dockerfile-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> The simplest demo of chrome automation by python and selenium in AWS Lambda

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 621 |
| 🍴 **Forks** | 141 |
| 💻 **Language** | Dockerfile |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`aws-lambda` `chromedriver` `chromium` `docker` `lambda` `python` `scraping` `selenium` `serverless`

## 🎯 Categories

Automation · Cloud & Storage · DevOps/Infra

## 📝 Summary

### English

**Project Summary:**
Umihico's Docker-Selenium-Lambda project is an open-source, high-readiness solution for automating repetitive tasks using Python and Selenium in AWS Lambda. This project helps streamline workflows by removing manual operations, connecting tools into repeatable flows, and scheduling operational tasks. With its recent activity, strong adoption, and robust ecosystem, it is suitable for serious pilots.

**Value:**
The main value proposition of this project lies in its ability to automate repetitive tasks, reducing manual labor and increasing efficiency. By leveraging Docker and Selenium, developers can create repeatable flows and schedule operational tasks, making it easier to manage workflows.

**Practical Adoption Path:**
To adopt this project, developers can follow these steps:

1. Evaluate the project's implementation signals, such as API/SDK/CLI, language metadata, and focused topics.
2. Review the project's GitHub repository, including the Dockerfile, to understand its architecture and dependencies.
3. Assess the project's production readiness, considering its recent activity, adoption, and ecosystem signals.
4. Evaluate the project's risks, including license, security posture, and active maintainers.
5. Integrate the project into your existing workflow by scheduling operational tasks and connecting tools into repeatable flows.

**Production Readiness:**
The

### Русский

Резюме проекта umihico/docker-selenium-lambda:

Проект umihico/docker-selenium-lambda представляет собой простой демонстрационный пример автоматизации браузера Chrome с помощью Python и Selenium в AWS Lambda. Он помогает избавиться от повторяющихся ручных операций в рабочем процессе, обеспечивая возможность автоматизации мониторинга и выполнения задач.

Проект подходит для следующего типового сценария внедрения: удаление ручной работы, подключение инструментов к повторяемым потокам, планирование операционных задач. Проект имеет высокий уровень готовности к production, что означает, что он уже имеет достаточно активных разработчиков, адоптации и сигналов экосистемы, что позволяет использовать его в серьезных пилотных проектах.

### 中文

**项目简介**  
umihico/docker-selenium-lambda 是一个极简示例，展示了如何在 AWS Lambda 中使用 Python + Selenium + Chrome（通过 Docker）完成浏览器自动化。它把本地的 Selenium 脚本封装成 Lambda 可直接调用的容器镜像，帮助开发者快速把 UI 自动化迁移到无服务器环境。

**价值**  
- **消除重复手工操作**：把浏览器交互、数据抓取、表单提交等繁琐步骤自动化，节省人力成本。  
- **可编排的可重复流程**：可与 Step Functions、EventBridge、Airflow 等编排工具结合，实现定时或事件驱动的业务任务。  
- **无服务器即开即用**：无需维护 EC2 实例或 Selenium Grid，使用 Lambda 即可弹性伸缩，成本低。

**典型接入方式**  
1. **拉取并自定义镜像**：`docker pull ghcr.io/umihico/docker-selenium-lambda:latest`，根据业务需求在 Dockerfile 中加入额外的 Python 包或脚本。  
2. **部署到 Lambda**：在 AWS 控制台或使用 SAM/Serverless Framework，将镜像作为容器函数上传，配置合适的内存（推荐 2 GB）和超时（最多 15 min）。  
3. **调用方式**：  
   - **API Gateway**：暴露 HTTP 接口，前端或其他服务通过 REST 调用。  
   - **SDK/CLI**：使用 AWS SDK（boto3）或 `aws lambda invoke` 直接触发函数并传入 JSON 参数（如目标 URL、操作指令）。  
   - **事件驱动**：通过 EventBridge 定时触发或响应 S3、SNS 等事件实现自动化工作流。  

**生产可用性**  
- **活跃度**：最近一次更新在 2026‑07‑01，拥有 621 ★、141 Fork，社区活跃。  
- **成熟度**：项目已完成 Docker 化、Lambda 打包、示例代码，具备完整的 CI/CD 流程，适合作为正式业务的**试点**或**生产**使用。  
- **风险点**：仍需进一步审查许可证兼容性、容器安全基线以及维护者响应速度，但整体安全和可靠性已达到 OSS 级别的高可用标准。  

综上，umihico/docker-selenium-lambda 能帮助团队快速将 Selenium 脚本迁移到无服务器环境，实现可编排、低成本的浏览器自动化，是值得在生产环境中进行试点的成熟开源方案。

## 🧭 Practical evaluation

**Value:** umihico/docker-selenium-lambda helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 621 GitHub stars
- 141 forks
- updated 2026-07-01
- primary language: Dockerfile
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 59/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 58/100 |
| production | 75/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/umihico/docker-selenium-lambda) · [← Back to Automation](./README.md)</sub>
