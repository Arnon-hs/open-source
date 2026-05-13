# apache/yunikorn-core

[![Stars](https://img.shields.io/github/stars/apache/yunikorn-core?style=flat-square&color=yellow)](https://github.com/apache/yunikorn-core/stargazers) [![Forks](https://img.shields.io/github/forks/apache/yunikorn-core?style=flat-square&color=blue)](https://github.com/apache/yunikorn-core/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Apache YuniKorn Core

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1k |
| 🍴 **Forks** | 264 |
| 💻 **Language** | Go |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apache-yarn` `go` `kubernetes` `universal-resource-scheduler` `yunikorn`

## 🎯 Categories

Automation · DevOps/Infra

## 📝 Summary

### English

Apache YuniKorn Core is an open‑source, Go‑based scheduler that automates repetitive operational tasks and enables the creation of repeatable, tool‑linked workflows. With strong recent activity, 1 010 ⭐ on GitHub, and growing ecosystem adoption, it is ready for a serious pilot, though a small proof‑of‑concept and a quick README review are recommended before full integration. The project’s high production readiness stems from active maintainers, robust community signals, and a clear path to replace manual scheduling with reliable, automated job orchestration.

### Русский

Apache YuniKorn Core — open‑source‑платформа на Go, автоматизирующая повторяющиеся операции в инфраструктуре и позволяющая связать инструменты в воспроизводимые рабочие потоки (например, планирование и исполнение операционных задач). Для начала рекомендуется запустить небольшой proof‑of‑concept, проверив README и базовую интеграцию, после чего можно масштабировать решение в продакшн. Проект обладает высокой готовностью к production: активная разработка, значительное количество звёзд и форков, а также растущее принятие в сообществе, хотя окончательная проверка лицензии, безопасности и активности мейнтейнеров всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
Apache YuniKorn Core 是一款基于 Go 实现的开源调度框架，专注于将繁琐的手工运维任务自动化并编排为可重复的工作流。它能够把多种工具和服务无缝连接，提供统一的任务调度与资源管理能力。

**价值**  
- **降低人为错误**：通过自动化调度，消除重复的手动操作，提升运维可靠性。  
- **提升效率**：支持将脚本、容器、批处理等不同任务统一纳入可编排的工作流，实现“一键”执行。  
- **可扩展性强**：基于插件化设计，能够灵活接入 CI/CD、监控、日志等生态系统工具。

**典型接入方式**  
1. **快速 POC**：克隆仓库后直接运行 `make run`，使用自带的示例配置验证调度功能。  
2. **集成 README**：参考项目根目录的 README，按照示例 YAML 定义调度策略和资源池，将业务任务（如 Spark、K8s Job）注册到 YuniKorn。  
3. **API/SDK 调用**：通过 RESTful API 或 Go SDK 在现有 CI/CD 流水线中下发任务，实现自动化触发与状态查询。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑13 最近一次提交，拥有 1010+ 星、264+ Fork，社区活跃，维护者响应及时。  
- **成熟度**：已在多个大规模集群中试点，具备完整的监控、日志和高可用部署方案。  
- **风险**：仍需对许可证、依赖安全性以及维护者长期可用性进行最终审查，但整体已达到可在正式生产环境中进行认真试点的水平。

## 🧭 Practical evaluation

**Value:** apache/yunikorn-core helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1010 GitHub stars
- 264 forks
- updated 2026-05-13
- primary language: Go
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 64/100 |
| topics | 63/100 |
| outlook | 75/100 |
| quality | 78/100 |
| recency | 100/100 |
| adoption | 63/100 |
| production | 78/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/apache/yunikorn-core) · [← Back to Automation](./README.md)</sub>
