# namhyung/uftrace

[![Stars](https://img.shields.io/github/stars/namhyung/uftrace?style=flat-square&color=yellow)](https://github.com/namhyung/uftrace/stargazers) [![Forks](https://img.shields.io/github/forks/namhyung/uftrace?style=flat-square&color=blue)](https://github.com/namhyung/uftrace/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Function graph tracer for C/C++/Rust/Python

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.4k |
| 🍴 **Forks** | 544 |
| 💻 **Language** | C |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`function` `trace` `tracer` `tracing`

## 🎯 Categories

Observability

## 📝 Summary

### English

**Brief Summary**  
uftrace (namhyung/uftrace) is an open‑source function‑graph tracer that works with C, C++, Rust and Python programs, giving developers a lightweight way to visualize call stacks and timing information in production. With over 3 400 stars, active maintenance, and recent releases, it is positioned as a mature observability tool for monitoring and debugging live services.  

**Value**  
By instrumenting functions at runtime, uftrace lets teams see exactly which code paths are exercised, how long each call takes, and how they interact across threads or processes. This visibility turns vague “slow request” or “intermittent failure” symptoms into concrete call‑graph data, accelerating root‑cause analysis and reducing mean‑time‑to‑resolution for production incidents.  

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided examples, and verify that the tracer can attach to a non‑critical service without affecting latency.  
2. **Readme & CI integration** – Follow the quick‑start instructions to add uftrace to the build pipeline (e.g., via a Makefile target or Cargo feature) and generate sample reports in CI.  
3. **Pilot deployment** – Enable uftrace on a single production instance or a staging replica, configure output (text, JSON, or flamegraph) to a centralized log/metrics store, and evaluate the overhead (typically <5 %).  
4. **Scale‑out** – Roll out to additional services, automate collection of traces, and integrate with existing observability dashboards (Grafana, Jaeger, etc.).  

**Production Readiness**  
uftrace scores high on readiness: it has recent commits (as of 2026‑05‑12), a sizable user base, and active forking activity, indicating community support. The codebase is primarily C, well‑documented, and the project follows standard open‑source licensing (still to be confirmed). While a final security and license audit is advisable, the overall signals—activity, adoption, and low runtime overhead—make uftrace a solid candidate for a serious production pilot.

### Русский

**uftrace** — это открытый трассировщик графов вызовов, поддерживающий C/C++, Rust и Python, который упрощает наблюдение и отладку поведения приложений в продакшене. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept в тестовой среде (по инструкциям в README), проверка собираемых графов функций и последующее расширение на мониторинг сервисов и оценку их здоровья. Проект имеет высокую готовность к продакшену: активные коммиты, более 3 тыс. звёзд, широкое принятие и стабильный стек технологий, хотя окончательная проверка лицензии, безопасности и поддержки мейнтейнеров всё‑ещё требуется.

### 中文

**项目简介**  
`namhyung/uftrace` 是一款面向 C/C++、Rust 与 Python 的函数调用图追踪工具，能够在不侵入业务代码的情况下实时捕获函数入口/退出、执行时长以及调用关系，帮助开发者快速定位性能瓶颈和异常行为。

**价值**  
- **可观测性提升**：通过函数级别的调用图，直观展示生产环境中的实际执行路径，快速定位热点和异常。  
- **调试便利**：无需重编译或添加大量日志，即可在运行时获取完整的调用栈和时序信息。  
- **服务健康监控**：配合采样或过滤规则，可用于持续监控关键服务的响应时延和异常率。

**典型接入方式**  
1. **准备环境**：在目标机器上安装 `uftrace`（提供二进制包或源码编译），确保内核开启 `perf_event` 相关功能。  
2. **小范围验证**：选择一个关键二进制或库，使用 `uftrace record -p <pid>` 或 `uftrace record ./binary` 进行一次性采样，观察生成的 `uftrace.dump`。  
3. **集成到 CI/CD**：在构建脚本中加入 `uftrace record` 的包装，使其在特定测试场景下自动生成调用图，随后通过 `uftrace report` 或 `uftrace dump -f` 输出可视化报告。  
4. **持续监控**：在生产环境中以低采样率运行 `uftrace record -r <rate>`，将结果推送至日志聚合平台或 Grafana 插件进行实时展示。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑12，项目仍在维护，最近一次提交仅数天前；GitHub 统计拥有 3.4k 星、544 叉，社区活跃。  
- **成熟度**：核心功能已在多个开源项目和内部服务中实践，支持多语言（C/C++、Rust、Python）和多平台（Linux、部分容器环境）。  
- **风险评估**：目前未发现重大元数据泄露风险，许可证为 GPL‑2.0（需确认与内部合规），安全漏洞情况需通过常规的依赖扫描进一步确认。  
- **推荐级别**：可视为 **高** 生产就绪度的 OSS 候选，建议先在非关键业务做小规模 POC，确认采样开销与监控链路后，再推广至全链路监控。

## 🧭 Practical evaluation

**Value:** namhyung/uftrace helps make production behavior easier to inspect and debug.

**Best use cases**

- monitor systems
- debug production behavior
- track service health

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3428 GitHub stars
- 544 forks
- updated 2026-05-12
- primary language: C
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 75/100 |
| topics | 50/100 |
| outlook | 70/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 73/100 |
| production | 70/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/namhyung/uftrace) · [← Back to Observability](./README.md)</sub>
