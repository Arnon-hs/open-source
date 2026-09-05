# mokeyish/smartdns-rs

[![Stars](https://img.shields.io/github/stars/mokeyish/smartdns-rs?style=flat-square&color=yellow)](https://github.com/mokeyish/smartdns-rs/stargazers) [![Forks](https://img.shields.io/github/forks/mokeyish/smartdns-rs?style=flat-square&color=blue)](https://github.com/mokeyish/smartdns-rs/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> A cross platform local DNS server (Dnsmasq like) written in rust to obtain the fastest website IP for the best Internet experience, supports DoT, DoQ, DoH, DoH3.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 965 |
| 🍴 **Forks** | 65 |
| 💻 **Language** | Rust |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dns` `dns-over-h3` `dns-over-https` `dns-over-quic` `dns-over-tls` `dns-server` `dnsmasq` `doh` `dot` `linux` `macos` `pi-hole`

## 🎯 Categories

Backend · Security

## 📝 Summary

### English

**Brief Summary**  
SmartDNS‑RS (mokeyish/smartdns-rs) is a cross‑platform, Rust‑based local DNS resolver that mimics Dnsmasq but adds modern encrypted DNS protocols (DoT, DoQ, DoH, DoH3). It continuously probes upstream resolvers to pick the fastest IP address for each domain, delivering a smoother, lower‑latency internet experience.  

**Value**  
- **Performance‑first DNS** – By automatically selecting the quickest IP, it reduces page‑load times and improves reliability for end‑users and latency‑sensitive services.  
- **Security & privacy** – Built‑in support for DNS‑over‑TLS, DNS‑over‑QUIC, DNS‑over‑HTTPS and the upcoming DNS‑over‑HTTPS/3 ensures encrypted queries without extra tooling.  
- **Rust safety & speed** – The implementation benefits from Rust’s memory safety guarantees and low overhead, making it suitable for both desktop and server environments.  

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided Docker image or binary, and point a test machine’s DNS to `127.0.0.1`. Verify that the resolver correctly selects faster IPs and that encrypted DNS works with your upstream providers.  
2. **Integration** – Replace existing local resolvers (e.g., Dnsmasq, systemd‑resolved) in a controlled environment (development laptops, CI runners, or a staging VM). Adjust the configuration file to list preferred upstream DoT/DoH endpoints.  
3. **Automation** – Incorporate the binary into your infrastructure as a systemd service or container orchestrated by Kubernetes/Podman, exposing port 53/UDP and the encrypted ports as needed.  
4. **Monitoring & Tuning** – Use the built‑in metrics endpoint (if enabled) or integrate with Prometheus to watch latency statistics and health checks, then fine‑tune upstream lists or caching policies.  

**Production Readiness**  
- **Maturity**: 965 ★ on GitHub, active maintenance (last commit 2026‑06‑27) and a modest fork base indicate a healthy community, but the project is still positioned as a “prototype‑ready” tool rather than a battle‑tested enterprise service.  
- **Stability**: Core DNS functionality is solid, yet edge‑case handling (e.g., DNSSEC validation, large zone files) may require additional testing.  
- **Operational overhead**: Deployment is straightforward (binary or Docker), but you’ll need to validate the startup scripts, system‑service wrappers, and ensure that your environment’s firewall permits the required encrypted ports.  
- **Risk**: Integration documentation is limited; verify the build pipeline, dependency licenses, and perform a security audit of the Rust crates used before wide‑scale rollout.  

Overall, SmartDNS‑RS is a compelling option for teams that want an ultra‑fast, encrypted local DNS resolver with minimal configuration effort, suitable for internal pilots or as a performance layer in larger networking stacks, provided a small validation phase is completed first.

### Русский

**SmartDNS‑RS** — кроссплатформенный локальный DNS‑сервер на Rust (аналог Dnsmasq), который автоматически выбирает самый быстрый IP‑адрес сайта, поддерживая DoT, DoQ, DoH и DoH3. Он удобен для прототипирования AI‑фич, построения RAG‑агентов и оценки моделей, позволяя быстро добавить сетевой слой с безопасным и ускоренным DNS без разработки собственного стека. Проект имеет средний уровень готовности к production: достаточная популярность (965 ★, 65 forks) и актуальные обновления, но требует небольшого PoC и проверки зависимостей перед масштабным внедрением.

### 中文

**项目简介**  
`mokeyish/smartdns-rs` 是一款用 Rust 编写的跨平台本地 DNS 服务器，功能类似 Dnsmasq。它通过 DoT / DoQ / DoH / DoH3 等加密协议查询多个上游 DNS，并实时挑选出响应最快的 IP，帮助终端获得最优的访问速度。

**价值**  
- **提升网络体验**：自动选取最快 IP，显著降低页面加载和下载延迟。  
- **安全可靠**：支持 DNS‑over‑TLS、DNS‑over‑HTTPS、DNS‑over‑QUIC 等加密协议，防止 DNS 劫持和窥探。  
- **轻量高效**：Rust 天然的零成本抽象和低内存占用，使其在资源受限的设备（路由器、嵌入式系统）上也能流畅运行。  
- **易于扩展**：源码开放、插件化设计，方便在现有网络架构中加入自定义过滤、日志或 AI 关联（如基于模型的恶意域名检测）。

**典型接入方式**  
1. **本地部署**：在服务器或路由器上编译运行 `smartdns-rs`，将本机 DNS 设置指向 `127.0.0.1:53`（或自定义端口），即可为局域网内所有设备提供加速 DNS。  
2. **容器化**：官方提供 Docker 镜像，`docker run -p 53:53/udp -p 53:53/tcp mokeyish/smartdns-rs:latest`，配合 Kubernetes DaemonSet 在每个节点上运行，适合云原生环境。  
3. **与现有 DNS 体系集成**：在 `smartdns-rs` 中配置上游 DNS 列表（如 Cloudflare、Google、Quad9），并使用 `forward`、`fallback` 或 `policy` 规则让其与现有的 BIND / CoreDNS 共存，作为加速层。  
4. **AI/ML 辅助**：通过读取 `smartdns-rs` 的日志或插件接口，将查询数据喂入模型，实现恶意域名自动识别或基于用户行为的自适应路由。

**生产可用性**  
- **成熟度**：GitHub ★965、Fork 65，最近一次提交在 2026‑06‑27，活跃度较高，代码基于 Rust，天然具备安全性和并发性能。  
- **适用场景**：内部网络加速、企业 VPN DNS 前置、IoT 设备的安全 DNS 解析、研发环境的快速原型搭建。  
- **风险与注意事项**  
  - **集成成本**：需要自行编写或使用已有的 `systemd`/`docker` 启动脚本，且上游 DNS 的选择和策略配置需根据业务调优。  
  - **运维监控**：建议配合 Prometheus exporter（项目已提供）监控查询延迟、缓存命中率等指标。  
  - **依赖管理**：Rust 生态更新较快，定期审计 `Cargo.lock` 中的依赖版本，防止出现安全漏洞。  
- **结论**：在经过一次小范围的 PoC（如在单台机器或少量容器中验证加速效果）并完成配置、监控和安全审计后，可视为 **中等成熟度** 的生产级组件，适合在内部或对可靠性要求不极端的外部服务中直接投产。

## 🧭 Practical evaluation

**Value:** mokeyish/smartdns-rs helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 965 GitHub stars
- 65 forks
- updated 2026-06-27
- primary language: Rust
- 18 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 64/100 |
| topics | 100/100 |
| outlook | 71/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 58/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/mokeyish/smartdns-rs) · [← Back to Backend](./README.md)</sub>
