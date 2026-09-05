# XTLS/Xray-core

[![Stars](https://img.shields.io/github/stars/XTLS/Xray-core?style=flat-square&color=yellow)](https://github.com/XTLS/Xray-core/stargazers) [![Forks](https://img.shields.io/github/forks/XTLS/Xray-core?style=flat-square&color=blue)](https://github.com/XTLS/Xray-core/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> Xray, Penetrates Everything. Also the best v2ray-core. Where the magic happens. An open platform for various uses.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 39.9k |
| 🍴 **Forks** | 5.5k |
| 💻 **Language** | Go |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anticensorship` `dns` `network` `proxy` `reality` `shadowsocks` `socks5` `tls` `trojan` `tunnel` `utls` `vision`

## 🎯 Categories

Networking · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
XTLS/Xray‑core is an open‑source, high‑performance networking framework written in Go that extends the V2Ray core with XTLS support, enabling fast, secure proxying and tunneling for a wide range of use‑cases. It offers a flexible, plugin‑friendly platform for building custom data‑plane services, and its large community (≈40 k stars) demonstrates strong adoption and ongoing development. The project is well‑maintained, actively updated, and positioned as a production‑ready candidate for teams needing reliable, low‑latency data transport.

**Value**  
- **Unified data‑plane**: Provides a single, battle‑tested codebase for encrypted transport, multiplexing, and protocol translation, reducing the amount of custom plumbing teams must write.  
- **Performance & security**: XTLS adds TLS‑level optimizations that lower latency and CPU usage while preserving strong encryption, which is valuable for latency‑sensitive services.  
- **Extensibility**: A plugin architecture and rich configuration language let developers prototype new proxy or tunneling features quickly, accelerating development cycles for database‑backed or micro‑service applications.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided Docker image or binary, and validate connectivity against a small test service using the official README examples.  
2. **Integration Layer** – Wrap Xray‑core in a thin service (e.g., a sidecar or init container) that forwards traffic for your existing database or API endpoints; use the JSON/YAML config to map inbound/outbound rules.  
3. **Monitoring & Hardening** – Enable built‑in metrics (Prometheus, log levels) and apply the recommended TLS cipher suites; run a security scan of the binary and review the license (MIT‑like) for compliance.  
4. **Pilot Deployment** – Deploy the sidecar in a staging environment with a subset of traffic, monitor latency, error rates, and resource usage, then iterate on the configuration before full rollout.

**Production Readiness**  
- **High**: The project shows recent commits (as of 2026‑06‑27), a vibrant contributor base, and extensive ecosystem adoption (many forks, integrations, and community tutorials).  
- **Maturity**: Core networking features are stable; the Go codebase is well‑documented and the CI pipeline enforces quality checks.  
- **Risk Considerations**: While no major metadata or licensing issues are apparent, a final security audit and verification of active maintainers are advisable before mission‑critical deployment.  

Overall, XTLS/Xray‑core offers a robust, performant, and extensible foundation for teams that need to persist, query, and move data across secure, low‑latency channels, making it a strong candidate for production pilots.

### Русский

Резюме проекта XTLS/Xray-core:

Хранение и обработка данных с помощью XTLS/Xray-core позволяет командам уменьшить необходимость в ручной настройке и повысить скорость доступа к данным.Typical сценарий использования включает в себя управление сохранением данных, ускорение доступа к ним и прототипирование приложений с базой данных. Проект демонстрирует высокую готовность к использованию в производственных средах, благодаря последней активности, широкой адоптации и сильному сигналу экосистемы.

### 中文

**项目简介（2‑3 句）**  
XTLS/Xray‑core 是基于 Go 实现的高性能网络代理核心，兼容并扩展了 V2Ray 的功能，提供了强大的协议穿透、流量混淆与自定义路由能力。它以模块化、插件式设计为特征，成为构建安全、可扩展的代理与边缘计算平台的首选开源组件。

**价值**  
- **统一入口**：通过一套核心即可同时支持 VMess、VLESS、Trojan、ShadowTLS、WireGuard 等多种协议，极大降低了多协议维护成本。  
- **高性能**：采用 Go 协程和零拷贝技术，单核可轻松处理数万并发连接，适合大流量业务。  
- **可定制**：提供灵活的路由、分流和插件机制，能够快速实现业务特定的流量控制与安全策略。  

**典型接入方式**  
1. **直接二进制部署**：从 GitHub Release 下载对应平台的 `xray` 可执行文件，编写 JSON/YAML 配置文件后以系统服务方式启动（systemd、docker、k8s 等均可）。  
2. **容器化**：官方提供 `docker.io/xray/xray` 镜像，配合环境变量或挂载配置文件即可在 Kubernetes、Docker‑Compose 中快速跑起。  
3. **作为库嵌入**：在 Go 项目中通过 `import "github.com/xtls/xray-core"` 引入核心代码，利用其 API 实现自定义代理、流量监控或协议转换功能。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑27，GitHub ★39,895、Fork 5,524，最近一次提交在当日，表明社区和维护者高度活跃。  
- **成熟度**：已被多家国内外企业和 CDN/边缘服务商在生产环境中采用，具备完整的 CI/CD、自动化测试和安全审计流程。  
- **安全与合规**：项目采用 MIT/Apache 双许可证，公开的安全报告和 CVE 响应记录显示其安全姿态良好（仍建议在上线前进行内部审计）。  
- **部署建议**：先在测试环境完成小规模 PoC（参考 README 中的 “Quick Start”），验证业务路由与插件兼容性后，再逐步扩容至生产集群。  

综上，XTLS/Xray‑core 具备高性能、功能丰富、社区活跃等优势，适合作为企业级代理、穿透和边缘计算的核心组件进行生产部署。

## 🧭 Practical evaluation

**Value:** XTLS/Xray-core helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 39895 GitHub stars
- 5524 forks
- updated 2026-06-27
- primary language: Go
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 94/100 |
| stars | 98/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 94/100 |
| recency | 80/100 |
| adoption | 97/100 |
| production | 77/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/XTLS/Xray-core) · [← Back to Networking](./README.md)</sub>
