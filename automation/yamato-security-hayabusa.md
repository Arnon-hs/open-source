# Yamato-Security/hayabusa

[![Stars](https://img.shields.io/github/stars/Yamato-Security/hayabusa?style=flat-square&color=yellow)](https://github.com/Yamato-Security/hayabusa/stargazers) [![Forks](https://img.shields.io/github/forks/Yamato-Security/hayabusa?style=flat-square&color=blue)](https://github.com/Yamato-Security/hayabusa/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> Hayabusa (隼) is a sigma-based threat hunting and fast forensics timeline generator for Windows event logs.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.2k |
| 🍴 **Forks** | 276 |
| 💻 **Language** | Rust |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`attack` `cybersecurity` `detection` `dfir` `event` `forensics` `hayabusa` `hunting` `incident` `incident-response` `logs` `response`

## 🎯 Categories

Automation · Observability · Security

## 📝 Summary

### English

**Summary**  
Hayabusa (隼) is an open‑source, sigma‑based threat‑hunting and fast‑forensics timeline generator that parses Windows event logs to produce structured, query‑ready timelines. Written in Rust, it automates the repetitive steps of log collection, rule‑matching, and timeline construction, letting analysts focus on investigation rather than manual scripting. With over 3 200 GitHub stars, recent commits (as of 2026‑06‑23) and growing community adoption, it is ready for a serious pilot in production environments.

**Value** – By converting raw Windows event logs into ready‑to‑analyze timelines, Hayabusa eliminates the manual “pull‑parse‑filter” loop that slows down incident response, and it can be chained with SIEMs, SOAR platforms, or custom scripts to build repeatable hunting workflows.

**Practical adoption path** – Start with a small proof‑of‑concept: clone the repo, run the provided README examples on a test Windows host, and validate the generated JSON/CSV timeline against your existing detection rules. Once the basic pipeline works, wrap the CLI in a scheduled job (e.g., via cron or a CI/CD runner) and integrate the output with your downstream analysis tools (Elastic, Splunk, Loki, etc.). Document any required configuration tweaks early, as the integration steps are not fully described in the metadata.

**Production readiness** – The project shows high readiness: active maintenance, a large star/fork base, and a mature Rust codebase with multiple topics indicating ecosystem support. While the integration surface is not extensively documented, the strong community signals and recent activity make it a solid OSS candidate for production pilots, provided you allocate time to verify setup costs and create wrapper scripts for your specific workflow.

### Русский

Hayabusa — это открытый инструмент на Rust, который автоматически преобразует Windows‑event‑логи в Sigma‑правила, генерирует тайм‑лайн для быстрого форензика и устраняет повторяющиеся ручные операции в процессах threat hunting. Типичное внедрение начинается с небольшого proof‑of‑concept: проверяется README, настраивается интеграция с существующей системой сбора логов и планируется расписание периодических задач. По метрикам активности, количеству звёзд (3220) и форков проект считается почти готовым к продакшену, однако перед масштабным rollout стоит уточнить детали установки и интеграции.

### 中文

**项目简介**  
Hayabusa（隼）是基于 Sigma 规则的 Windows 事件日志威胁狩猎与快速取证时间线生成工具，使用 Rust 编写，专注于将繁琐的手工分析自动化。

**价值**  
- **削减重复劳动**：通过预置的 Sigma 规则自动解析 Windows 事件日志，省去手动筛选、关联的时间成本。  
- **可编排的安全流水线**：支持将 Hayabusa 嵌入 CI/CD 或 SOAR 流程，实现定时或触发式的威胁检测与取证报告。  
- **快速可视化**：生成结构化的时间线，帮助安全分析师在短时间内定位攻击路径。

**典型接入方式**  
1. **小范围 PoC**：先克隆仓库，阅读 `README.md`，在测试机器上运行 `hayabusa -c <config>`，验证对已有日志的解析效果。  
2. **容器化部署**：使用官方提供的 Dockerfile 或自行构建镜像，将其作为微服务放入 Kubernetes/Swarm，配合 CronJob 实现定时扫描。  
3. **与已有平台集成**：通过输出的 JSON/CSV 与 SIEM（如 Splunk、Elastic）或 SOAR（如 TheHive、Cortex）进行数据接入，完成端到端的自动化响应链路。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23，项目最近一次提交，拥有 3,220+ 星、276+ Fork，社区活跃。  
- **技术成熟**：核心使用 Rust，性能与安全性俱佳，且已在多个开源安全项目中被引用。  
- **风险点**：官方文档对企业级部署的细节较少，建议在正式上线前完成一次完整的 POC，评估环境依赖、日志采集路径以及后续运维成本。  

总体而言，Hayabusa 已具备在生产环境中进行试点的条件，适合作为自动化威胁狩猎与取证的关键组件，引入后可显著提升安全运营效率。

## 🧭 Practical evaluation

**Value:** Yamato-Security/hayabusa helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3220 GitHub stars
- 276 forks
- updated 2026-06-23
- primary language: Rust
- 20 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 75/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 82/100 |
| recency | 80/100 |
| adoption | 71/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/Yamato-Security/hayabusa) · [← Back to Automation](./README.md)</sub>
