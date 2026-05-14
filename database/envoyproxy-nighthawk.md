# envoyproxy/nighthawk

[![Stars](https://img.shields.io/github/stars/envoyproxy/nighthawk?style=flat-square&color=yellow)](https://github.com/envoyproxy/nighthawk/stargazers) [![Forks](https://img.shields.io/github/forks/envoyproxy/nighthawk?style=flat-square&color=blue)](https://github.com/envoyproxy/nighthawk/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> L7 (HTTP/HTTPS/HTTP2/HTTP3) performance characterization tool

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 410 |
| 🍴 **Forks** | 91 |
| 💻 **Language** | C++ |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Envoy Proxy’s **Nighthawk** is a high‑performance load‑testing tool for Layer‑7 protocols (HTTP, HTTPS, HTTP/2, HTTP/3). Written in C++, it can generate and measure traffic at extreme rates, providing detailed latency, throughput, and error statistics for services behind Envoy or any HTTP endpoint.  

**Value**  
Nighthawk gives engineering teams a purpose‑built, standards‑compliant benchmark for web‑service performance, enabling them to:  

* Quantify the impact of configuration changes, code releases, or hardware upgrades on latency and throughput.  
* Detect regressions early by integrating the tool into CI pipelines or nightly performance suites.  
* Compare Envoy‑enabled deployments against baseline implementations, helping to justify the operational cost of a service mesh.  

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Clone & build** the repository (requires a recent C++ compiler and CMake). | Guarantees you have the latest binaries and can customize build flags for your environment. |
| 2️⃣  | **Run a sanity check** against a simple HTTP endpoint (e.g., `http://localhost:8080`). | Confirms the tool works on your platform and gives you a baseline performance metric. |
| 3️⃣  | **Create a reusable config** (JSON/YAML) describing the target URL, request headers, concurrency, and duration. | Allows repeatable runs and easy integration with CI systems such as GitHub Actions, Jenkins, or Bazel. |
| 4️⃣  | **Integrate into CI**: add a step that executes `nighthawk_client` with the config and publishes the JSON output to a performance dashboard (Grafana, InfluxDB, or a custom viewer). | Automates regression detection and provides visibility to the whole team. |
| 5️⃣  | **Validate against production‑like traffic** by replaying real request patterns (captured via Envoy access logs or traffic mirroring). | Ensures the benchmark reflects actual workloads rather than synthetic micro‑benchmarks. |
| 6️⃣  | **Iterate**: adjust concurrency, payload size, or protocol (HTTP/2, HTTP/3) to match your service’s expected load and repeat the test after each change. | Drives data‑backed tuning of Envoy filters, routing rules, or underlying service code. |

**Production Readiness**  
- **Maturity**: 410 ⭐ on GitHub, 91 forks, active maintenance (last commit 2026‑05‑14). The codebase is stable, but documentation around CI integration and advanced HTTP/3 usage is thin.  
- **Risk Level**: *Medium*. The tool is production‑grade for performance testing, yet the integration path is not fully documented; teams should allocate time for a pilot to verify build dependencies, networking permissions, and result interpretation.  
- **Recommended Use**: Ideal for internal performance benchmarking, pre‑release validation, and capacity‑planning exercises. Before deploying in a critical production monitoring pipeline, perform a controlled rollout, confirm that the generated load does not overwhelm downstream services, and set up alerting on abnormal latency spikes.  

In short, Nighthawk is a powerful, open‑source load‑testing utility that can become a core part of an organization’s performance‑testing workflow, provided the team invests in a modest onboarding effort to bridge the current documentation gaps.

### Русский

**Envoyproxy/Nighthawk** — это высокопроизводительный open‑source‑инструмент для измерения характеристик L7 (HTTP/HTTPS/HTTP2/HTTP3) запросов, написанный на C++. Он обычно используется командами для быстрой профилизации сетевых сервисов, проверки пропускной способности и отладки конфигураций перед вводом в эксплуатацию. Готовность к production — средняя: продукт подходит для прототипов и внутренних пайплайнов, но требует ручного анализа интеграции и проверки зависимостей перед масштабным развертыванием.

### 中文

**项目简介**  
envoyproxy/nighthawk 是一款面向 L7（HTTP/HTTPS/HTTP2/HTTP3）的性能特性分析工具，能够对服务端点进行高精度的吞吐量、延迟和错误率等指标测量。它以 C++ 实现，轻量且可直接在命令行使用，适合快速评估网络层面的负载表现。

**价值**  
- **精准性能评估**：提供细粒度的请求/响应时延分布、QPS、错误率等数据，帮助团队定位瓶颈。  
- **与 Envoy 深度结合**：可以直接对 Envoy 代理或任何兼容的 HTTP 服务进行压测，便于在微服务架构中进行端到端性能验证。  
- **开源且可定制**：源码可自行编译，支持插件式扩展，满足特定业务场景的自定义需求。

**典型接入方式**  
1. **二进制直接使用**：在 CI/CD 或本地机器上下载预编译的 `nighthawk_client`/`nighthawk_server`，通过命令行指定目标 URL、并发数、持续时间等参数即可开始压测。  
2. **容器化部署**：官方提供 Docker 镜像（`envoyproxy/nighthawk`），在 Kubernetes Job 或 Pod 中运行，便于在集群环境下进行大规模压测。  
3. **集成到 CI**：在 Jenkins、GitHub Actions 等流水线中加入 `nighthawk` 命令，自动对新发布的服务进行回归性能测试，并将结果输出为 JSON/CSV 供后续分析。  

**生产可用性**  
- **成熟度**：GitHub 约 410 星、91 Fork，活跃维护，最近一次提交在 2026‑05‑14，代码基于 C++，具备较好的性能和稳定性。  
- **适用场景**：适合作为内部性能基准、预发布压测或研发阶段的性能回归；在正式生产环境做持续监控时，需要结合更完善的监控体系（如 Prometheus + Grafana）。  
- **风险与注意事项**：元数据中缺乏完整的集成指南，首次接入时可能需要手动验证网络拓扑、TLS 配置以及资源配额；建议在非关键业务环境先进行验证，确认依赖（如 libevent、OpenSSL）与现有系统兼容后，再考虑在生产链路中使用。  

总体而言，Nighthawk 在性能评估方面表现出色，适合作为原型验证或内部工作流的压测工具；在生产环境使用时需做好前置的集成测试和运维监控。

## 🧭 Practical evaluation

**Value:** envoyproxy/nighthawk helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 410 GitHub stars
- 91 forks
- updated 2026-05-14
- primary language: C++

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 49/100 |
| stars | 56/100 |
| topics | 0/100 |
| outlook | 70/100 |
| quality | 64/100 |
| recency | 100/100 |
| adoption | 54/100 |
| production | 69/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/envoyproxy/nighthawk) · [← Back to Database](./README.md)</sub>
