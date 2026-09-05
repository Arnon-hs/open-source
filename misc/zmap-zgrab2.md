# zmap/zgrab2

[![Stars](https://img.shields.io/github/stars/zmap/zgrab2?style=flat-square&color=yellow)](https://github.com/zmap/zgrab2/stargazers) [![Forks](https://img.shields.io/github/forks/zmap/zgrab2?style=flat-square&color=blue)](https://github.com/zmap/zgrab2/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Fast Application Layer Scanner

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.1k |
| 🍴 **Forks** | 369 |
| 💻 **Language** | Go |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`internet-scanning` `network-scanner`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary:** zmap/zgrab2 is an open-source, fast application layer scanner that can be useful for specific workflows, particularly when its README and activity match a concrete use case. While it may require manual inspection and integration checks, it can be a valuable tool for prototypes or internal workflows. With proper maintenance and dependency checks, it can be considered for production use.

**Value:** The value of zmap/zgrab2 lies in its ability to efficiently scan application layers, making it a useful tool for specific workflows. Its fast scanning capabilities can be beneficial for development, testing, and internal use cases.

**Practical Adoption Path:**

1. **Manual Inspection**: Carefully review the README and activity of the project to ensure it aligns with your specific use case.
2. **Integration Checks**: Inspect the integration signals in the discovered metadata to ensure a smooth integration process.
3. **Dependency and Maintenance Checks**: Verify the dependencies and maintenance requirements of the project before adopting it.
4. **Prototype or Internal Workflow**: Use zmap/zgrab2 in a prototype or internal workflow to test its capabilities and identify potential issues.

**Production Readiness:** With proper checks and maintenance, zmap/zgrab2 can be considered for production use. Its medium production readiness score indicates that it can be

### Русский

Резюме:

Заголовок: Быстрый сканер приложения на уровне сети (zmap/zgrab2)

Заголовок на английском: Fast Application Layer Scanner

Описание: Проект zmap/zgrab2 представляет собой быстрый сканер приложения на уровне сети, который может быть полезен в сценариях, когда его README и активность соответствуют конкретной рабочей схеме. Этот сканер может быть использован для интеграции в прототипы или внутренние рабочие процессы с последующим проверкой зависимостей и поддержки.

Уровень готовности к production: Средний. Проект можно использовать для прототипов или внутренних рабочих процессов, но требует тщательной проверки зависимостей и поддержки перед внедрением в производство.

### 中文

**项目简介**  
zmap/zgrab2 是一个用 Go 编写的高速应用层扫描器，能够在网络层快速发现目标后并行抓取 HTTP、HTTPS、SMTP、TLS 等协议的握手或元数据。它常被用于安全审计、资产发现以及大规模互联网测绘。

**价值**  
- **速度与并发**：基于 ZMap 的高速端口发现，配合多协程的协议抓取，可在几分钟内完成数十万甚至上百万主机的应用层信息采集。  
- **灵活的插件式协议实现**：内置多种常用协议抓取模块，也支持自定义 Go 插件，满足特定业务需求。  
- **开源且社区活跃**：拥有 2 k+ Stars、数百个 Fork，最近一次提交在 2026‑06‑29，说明项目仍在维护中。

**典型接入方式**  
1. **作为独立 CLI 工具**：直接在 CI/CD、调度系统（如 cron、Airflow）或容器化环境中调用 `zgrab2`，通过命令行参数指定目标列表、协议和输出格式（JSON/CSV）。  
2. **嵌入自研系统**：利用其 Go 包 (`github.com/zmap/zgrab2`) 在内部服务中直接调用扫描函数，实现与资产库、漏洞管理平台的自动化集成。  
3. **配合 ZMap**：先用 ZMap 完成端口快速探测，再将发现的 IP:Port 列表交给 ZGrab2 进行协议层抓取，形成完整的 “端口 → 应用层” 数据链路。

**生产可用性**  
- **成熟度**：中等（Medium）。在原型验证或内部工具中已被广泛使用，功能稳定；但在正式生产环境部署前，建议完成以下检查：  
  - **依赖审计**：确认所有第三方 Go 模块的许可证兼容性与安全漏洞（使用 `go mod tidy` + `govulncheck`）。  
  - **安全评估**：对抓取的协议实现进行渗透测试，防止因解析异常导致的远程代码执行或资源耗尽。  
  - **监控与限流**：在高并发场景下加入速率限制、超时和错误重试机制，避免对目标网络造成 DoS。  
- **运维要求**：建议使用容器镜像（官方或自行构建的轻量镜像）配合 Kubernetes Job / CronJob 管理；日志输出采用结构化 JSON，便于 ELK/Prometheus 统一收集与告警。  

总体而言，zmap/zgrab2 适合作为内部安全资产发现或大规模互联网测绘的核心组件，在完成依赖安全审查和运维包装后，可安全投入生产使用。

## 🧭 Practical evaluation

**Value:** zmap/zgrab2 may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2137 GitHub stars
- 369 forks
- updated 2026-06-29
- primary language: Go
- 2 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 71/100 |
| topics | 25/100 |
| outlook | 66/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 69/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/zmap/zgrab2) · [← Back to Misc](./README.md)</sub>
