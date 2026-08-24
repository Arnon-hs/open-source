# bugsink/bugsink

[![Stars](https://img.shields.io/github/stars/bugsink/bugsink?style=flat-square&color=yellow)](https://github.com/bugsink/bugsink/stargazers) [![Forks](https://img.shields.io/github/forks/bugsink/bugsink?style=flat-square&color=blue)](https://github.com/bugsink/bugsink/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Self-hosted Error Tracking

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.9k |
| 🍴 **Forks** | 109 |
| 💻 **Language** | Python |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

Here's a brief summary and explanation of the project:

**Summary:** bugsink/bugsink is a self-hosted error tracking open-source project that allows users to monitor and track errors in their applications. It's a useful tool for prototypes or internal workflows, requiring manual inspection before adoption due to sparse integration signals.

**Value:** The value proposition of bugsink/bugsink lies in its ability to provide a concrete workflow for error tracking, which can be useful for teams that require a high degree of customization and control over their error monitoring solution. However, its value is dependent on its README and activity aligning with the specific needs of the user.

**Practical Adoption Path:** Before adopting bugsink/bugsink, users should manually inspect the project's integration signals, which are sparse in the discovered metadata. This requires careful evaluation of the project's compatibility with the user's existing infrastructure and workflows. Additionally, users should perform dependency and maintenance checks before production to ensure the project is suitable for their needs.

**Production Readiness:** bugsink/bugsink is considered production-ready with a medium level of readiness. While it has a large number of GitHub stars and forks, and is actively maintained, it still requires a final review of its license, security posture, and active maintainers before being used in

### Русский

**Bugsink** — это self‑hosted система отслеживания ошибок, написанная на Python, с более чем 1900 звёздами на GitHub и активным обновлением. Она подходит для прототипов и внутренних сервисов, где требуется быстро собрать и проанализировать ошибки без отправки данных в сторонние SaaS‑решения; типичный сценарий — интеграция в CI/CD пайплайн и отправка стек‑трейсов из приложений через простой HTTP‑интерфейс. Готовность к production — средняя: проект достаточно зрелый, но перед развёртыванием стоит проверить лицензию, актуальность зависимостей и наличие активных мейнтейнеров.

### 中文

**简短介绍**  
Bugsink 是一款基于 Python 的自托管错误追踪系统，适合在内部网络或私有云中部署，用于捕获、聚合和分析应用异常。它拥有近 2 k 星、百余次 fork，最近一次提交在 2026‑06‑30，社区活跃度尚可。

**价值**  
- **数据自主可控**：所有异常信息都保存在自己的服务器上，符合合规和隐私要求。  
- **轻量易部署**：仅依赖 Python 环境和常见数据库（如 SQLite / PostgreSQL），可通过 Docker 镜像快速启动。  
- **可定制**：提供 webhook 与 API，方便与 CI/CD、告警平台或内部仪表盘集成，满足特定工作流需求。

**典型接入方式**  
1. **服务端部署**  
   - 拉取源码或官方 Docker 镜像，配置 `config.yaml`（数据库、日志级别、通知渠道等），启动 `bugsink` 服务。  
2. **客户端上报**  
   - 在 Python 项目中安装 `bugsink-client`（或使用通用的 HTTP/JSON 上报接口），在捕获异常的地方调用 `bugsink.report(exception)`，或通过 `logging` Handler 自动发送日志。  
3. **集成**  
   - 使用提供的 Webhook 将异常推送到 Slack、Microsoft Teams、PagerDuty 等；或通过 REST API 拉取异常列表进行自定义报表。  

**生产可用性**  
- **成熟度**：中等（Medium）。项目已具备基本功能并在多个内部项目中验证，可用于原型或内部业务。  
- **准备工作**：在正式上线前需检查以下几点：  
  - **依赖安全**：审计 `requirements.txt` 中的第三方库，确保无已知漏洞。  
  - **维护状态**：确认核心维护者仍活跃，或准备好自行处理 PR 与安全补丁。  
  - **运维监控**：为 Bugsink 本身配置健康检查、日志轮转和备份策略。  
- **适用场景**：内部研发团队、对数据隐私有严格要求的企业、以及需要高度可定制错误追踪的项目。若对 SLA、弹性伸缩有更高要求，建议结合容器编排（K8s）或商业错误监控服务进行补充。

## 🧭 Practical evaluation

**Value:** bugsink/bugsink may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1905 GitHub stars
- 109 forks
- updated 2026-06-30
- primary language: Python

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 70/100 |
| topics | 0/100 |
| outlook | 52/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 65/100 |
| production | 53/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/bugsink/bugsink) · [← Back to Misc](./README.md)</sub>
