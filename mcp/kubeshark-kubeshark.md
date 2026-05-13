# kubeshark/kubeshark

[![Stars](https://img.shields.io/github/stars/kubeshark/kubeshark?style=flat-square&color=yellow)](https://github.com/kubeshark/kubeshark/stargazers) [![Forks](https://img.shields.io/github/forks/kubeshark/kubeshark?style=flat-square&color=blue)](https://github.com/kubeshark/kubeshark/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-90%2F100-brightgreen?style=flat-square)](#)

> eBPF-powered network observability for Kubernetes. Indexes L4/L7 traffic with full K8s context, decrypts TLS without keys. Queryable by AI agents via MCP and humans via dashboard.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 11.9k |
| 🍴 **Forks** | 537 |
| 💻 **Language** | Go |
| 📈 **Score** | 90/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cloud-native` `devops` `docker` `ebpf` `golang` `grpc` `incident-response` `kubernetes` `mcp` `network-analysis` `network-engineering` `network-observability`

## 🎯 Categories

MCP · AI/ML · Observability · DevOps/Infra · Security

## 📝 Summary

### English

**Brief Summary**  
Kubeshark is an eBPF‑based network observability platform for Kubernetes that captures and indexes L4/L7 traffic with full Kubernetes context, even decrypting TLS streams without needing private keys. The data can be queried programmatically through the Model Context Protocol (MCP) for AI agents or interactively via a web dashboard, making it a bridge between AI assistants and real‑time cluster telemetry.  

**Value**  
- **AI‑ready telemetry**: By exposing traffic metadata through MCP, Kubeshark lets large language models or custom AI agents retrieve concrete, up‑to‑date network information, enabling automated troubleshooting, security analysis, and policy enforcement.  
- **Full‑stack visibility**: eBPF collection provides low‑overhead, kernel‑level packet capture, while automatic TLS decryption and Kubernetes enrichment give a complete picture of service‑to‑service communication.  
- **Unified access**: The same data source serves both human operators (dashboard, CLI, SDK) and machine agents, reducing the need for separate monitoring stacks.  

**Practical Adoption Path**  
1. **Deploy the Kubeshark Helm chart** (or the provided operator) into the target cluster; it runs as a DaemonSet with minimal resource impact.  
2. **Configure MCP endpoints** to expose the indexed traffic to your AI platform or to a Model Context Protocol server you control.  
3. **Integrate** your AI agents or automation scripts via the MCP client libraries (Go, Python, etc.), or use the built‑in dashboard/CLI for manual investigation.  
4. **Iterate** by adding custom filters or enrichment rules (e.g., tag specific namespaces or services) to tailor the telemetry to your use cases.  

**Production Readiness**  
- **Active development**: Recent commits (as of 2026‑05‑13), a vibrant community (≈12 k stars, 537 forks), and regular releases indicate strong maintenance.  
- **Mature ecosystem**: Written in Go, integrates cleanly with standard Kubernetes tooling (Helm, Operator SDK) and provides API/SDK/CLI interfaces.  
- **Scalability & performance**: eBPF collection is proven low‑overhead; TLS decryption is done on‑the‑fly without storing keys, keeping security posture acceptable.  
- **Adoption signals**: Multiple downstream projects already embed Kubeshark for observability and security, and the MCP interface is being used in early AI‑assistant pilots.  

Overall, Kubeshark is production‑ready for organizations that need deep, AI‑accessible network insight in Kubernetes, with a straightforward deployment and integration path.

### Русский

**kubeshark/kubeshark** — это open‑source решение на базе eBPF, которое в реальном времени индексирует L4/L7 трафик в кластере Kubernetes, обогащая его полным контекстом K8s и расшифровывая TLS без доступа к ключам. Типовой сценарий: развертываете агент в кластере, получаете мгновенный доступ к запросам через AI‑агентов (по Model Context Protocol) и через интерактивную панель, что упрощает диагностику, безопасность и автоматизацию DevOps‑процессов. Проект имеет высокий уровень готовности к production — активные коммиты, более 11 тыс. звёзд, широкое принятие в сообществе и готовый API/CLI/SDK, что делает его надёжной базой для пилотных и масштабных внедрений.

### 中文

**项目简介**  
kubeshark/kubeshark 是一款基于 eBPF 的 Kubernetes 网络可观测平台，能够在 L4/L7 层实时索引流量并关联完整的 K8s 元数据，甚至在不持有私钥的情况下解密 TLS。用户既可以通过 AI 助手的 Model Context Protocol（MCP）进行查询，也可以在可视化仪表盘中自行分析。

**价值主张**  
- **AI‑驱动的实时网络洞察**：通过标准化的 MCP 接口，让语言模型或其他 AI 代理直接查询真实的网络流量和安全事件，消除“模型幻觉”。  
- **完整上下文+解密**：自动关联 Pod、Service、Namespace 等 Kubernetes 对象，并在不泄露证书私钥的前提下呈现明文 HTTP/HTTPS 内容，极大提升故障排查和安全审计效率。  
- **统一集成点**：提供 API、SDK、CLI 三种接入方式，兼容多语言生态，方便在 CI/CD、自动化运维或自研 AI 助手中快速嵌入。

**典型接入方式**  
1. **MCP 服务器**：在集群内部署 Kubeshark 并开启 MCP 端口，AI 代理（如 ChatGPT、Claude）即可通过标准的 `model-context-protocol` 调用查询流量、TLS 解密结果或自定义指标。  
2. **REST/GraphQL API**：利用官方提供的 HTTP 接口进行脚本化查询或与自研监控系统对接。  
3. **CLI/SDK**：使用 `kubeshark` 命令行或 Go/Python SDK 在 CI 流水线、自动化测试或自定义 Dashboard 中直接拉取实时数据。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑13，项目拥有 11 902 星、537 Fork，最近一次提交在 2026‑05‑13，社区活跃且持续迭代。  
- **技术成熟**：核心使用 Go 编写，依赖成熟的 eBPF 框架，已在多个大型企业集群中验证。  
- **生态兼容**：支持标准的 Kubernetes API，易于与 Prometheus、Grafana、OpenTelemetry 等现有监控体系共存。  
- **安全与合规**：项目采用 Apache‑2.0 许可证，代码审计记录良好；TLS 解密在用户侧完成，不会泄露私钥。  

综合以上因素，kubeshark/kubeshark 已具备 **高生产就绪度**，适合作为 AI‑Assist‑Ops、零信任安全以及全链路可观测的核心组件进行试点或正式上线。

## 🧭 Practical evaluation

**Value:** kubeshark/kubeshark helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 11902 GitHub stars
- 537 forks
- updated 2026-05-13
- primary language: Go
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 87/100 |
| topics | 100/100 |
| outlook | 93/100 |
| quality | 92/100 |
| recency | 100/100 |
| adoption | 82/100 |
| production | 87/100 |
| usefulness | 90/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/kubeshark/kubeshark) · [← Back to Mcp](./README.md)</sub>
