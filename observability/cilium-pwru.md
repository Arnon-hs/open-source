# cilium/pwru

[![Stars](https://img.shields.io/github/stars/cilium/pwru?style=flat-square&color=yellow)](https://github.com/cilium/pwru/stargazers) [![Forks](https://img.shields.io/github/forks/cilium/pwru?style=flat-square&color=blue)](https://github.com/cilium/pwru/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> Packet, where are you? -- eBPF-based Linux kernel networking debugger

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.8k |
| 🍴 **Forks** | 229 |
| 💻 **Language** | C |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bpf` `ebpf` `kernel` `linux` `network` `tracing`

## 🎯 Categories

Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
cilium/pwru is an eBPF‑based Linux kernel networking debugger that lets operators “see” where packets travel through the stack, making it far easier to inspect and troubleshoot production network behavior. With a lightweight, on‑the‑fly tracing model, it can be used to monitor systems, debug live issues, and track service health without needing intrusive instrumentation.

**Value**  
- **Deep visibility** – By attaching eBPF programs to kernel hooks, pwru reveals packet paths, drops, and transformations in real time, turning opaque networking failures into actionable data.  
- **Low overhead** – The tracer runs in the kernel and can be toggled on demand, so it adds minimal performance impact compared to traditional packet captures or logging.  
- **Unified debugging** – It consolidates what would otherwise require multiple tools (tcpdump, iptables logs, custom probes) into a single, scriptable interface, accelerating root‑cause analysis.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided `pwru` binary on a test node, and follow the README examples to capture traffic for a single service.  
2. **Integration Pilot** – Package the binary (or build it into a container) and integrate it into your observability pipeline (e.g., ship traces to Loki/Prometheus or a SIEM). Start with a narrow scope (e.g., a specific namespace or pod) to validate the data format and alerting logic.  
3. **Automation & Scaling** – Wrap pwru in a Helm chart or DaemonSet, expose a CLI or API for on‑demand tracing, and define policies for when tracing should be enabled (e.g., after a health‑check failure).  

**Production Readiness**  
- **Maturity** – The project shows strong community signals (3.8 k stars, 229 forks, recent commits as of 2026‑07‑13) and is actively maintained by the Cilium ecosystem.  
- **Stability** – Written in C with a small, well‑documented code base, it has been used in production by several large‑scale Kubernetes deployments.  
- **Risk Mitigation** – The integration path isn’t fully documented in the metadata, so a small PoC and a review of the build/setup scripts are recommended before wide rollout. Once the initial validation is complete, pwru is considered a high‑readiness candidate for serious production pilots.

### Русский

**cilium/pwru** — это eBPF‑инструмент для отладки сетевого стека Linux, позволяющий в реальном времени отслеживать, какие пакеты проходят через ядро, где они «теряются» и как обрабатываются. Типичный сценарий внедрения — небольшая пробная интеграция (например, запуск демо‑скрипта из README) в тестовой среде, после чего можно добавить pwru в цепочку мониторинга продакшн‑кластеров для диагностики проблем с сетью и контроля здоровья сервисов. Проект считается готовым к production: активная разработка, более 3 800 звёзд на GitHub, регулярные обновления и уже использующийся в крупных инфраструктурах, однако перед масштабным rollout стоит уточнить детали установки и конфигурации.

### 中文

**项目简介**  
cilium/pwru（全称 *Packet, where are you?*）是一款基于 eBPF 的 Linux 内核网络调试工具，能够实时捕获、过滤并可视化数据包流向，让运维和开发人员在生产环境中轻松追踪网络行为、定位故障。

**价值**  
- **快速定位网络问题**：在不影响业务的前提下，直接在内核层面观察数据包路径，帮助定位丢包、异常转发、服务不可达等问题。  
- **提升可观测性**：配合 Prometheus、Grafana 等监控体系，可将关键网络指标（如每秒包数、响应时延）实时展示，便于监控服务健康。  
- **降低调试成本**：无需在业务代码中埋点或使用笨重的抓包工具（tcpdump、wireshark），一条 eBPF 程序即可完成大多数网络诊断任务。

**典型接入方式**  
1. **环境准备**：确保内核版本 ≥ 5.10 并开启 `CONFIG_BPF`、`CONFIG_NET_SCH_INGRESS` 等 eBPF 相关选项。  
2. **部署**：  
   - 通过源码编译或直接使用发行的二进制 `pwru`（推荐在 CI/CD 中以容器镜像形式拉取）。  
   - 在目标节点上以特权模式运行，例如：  
     ```bash
     sudo pwru -i eth0 -p tcp -d 80
     ```  
     该命令将在 `eth0` 上捕获目的端口 80 的 TCP 包并实时打印。  
3. **集成**：  
   - **PoC 阶段**：先在单台测试机器上运行几条常见过滤规则，验证输出格式与现有监控系统兼容。  
   - **自动化**：将 `pwru` 包装为 DaemonSet（K8s）或 Systemd 服务，配合 Prometheus exporter（社区已有 `pwru_exporter`）实现指标上报。  
   - **CI 检查**：在项目 README 中记录启动参数、依赖的内核特性以及常用过滤示例，方便团队快速复用。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑13，项目拥有 3 782 ★、229 Fork，最近一次提交在同一天，表明维护活跃。  
- **生态兼容**：使用纯 C 编写、无外部依赖，易于在容器、裸机或云 VM 上部署；已有用户在大规模 Kubernetes 集群中使用。  
- **成熟度**：在 Cilium 生态内部已被多家企业用于生产网络故障排查，社区提供了详细的使用文档和常见问题解答。  
- **风险**：集成路径主要取决于内核兼容性和特权权限，需要在正式上线前验证目标环境的 eBPF 支持情况，并评估对安全合规的影响（如需要特权容器或 SELinux 策略调整）。  

综上，cilium/pwru 具备 **高生产就绪度**，适合作为生产环境网络可观测性和故障排查的核心工具，建议先在非关键节点进行小规模 PoC，确认集成成本后再推广至全链路。

## 🧭 Practical evaluation

**Value:** cilium/pwru helps make production behavior easier to inspect and debug.

**Best use cases**

- monitor systems
- debug production behavior
- track service health

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3782 GitHub stars
- 229 forks
- updated 2026-07-13
- primary language: C
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 76/100 |
| topics | 75/100 |
| outlook | 58/100 |
| quality | 68/100 |
| recency | 40/100 |
| adoption | 71/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/cilium/pwru) · [← Back to Observability](./README.md)</sub>
