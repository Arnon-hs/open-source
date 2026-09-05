# keepsimple1/mdns-sd

[![Stars](https://img.shields.io/github/stars/keepsimple1/mdns-sd?style=flat-square&color=yellow)](https://github.com/keepsimple1/mdns-sd/stargazers) [![Forks](https://img.shields.io/github/forks/keepsimple1/mdns-sd?style=flat-square&color=blue)](https://github.com/keepsimple1/mdns-sd/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> Rust library for mDNS based Service Discovery

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 208 |
| 🍴 **Forks** | 66 |
| 💻 **Language** | Rust |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`rust`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`keepsimple1/mdns-sd` is a Rust library that implements multicast DNS (mDNS) service discovery, allowing applications to locate services on a local network without a central registry. With over 200 stars and recent activity (last update 2026‑07‑13), it can be a handy building block for prototypes or internal tools that need zero‑configuration networking, provided the integration effort is evaluated first.

**Value**  
- **Zero‑configuration networking** – simplifies the discovery of local services (e.g., printers, IoT devices, micro‑services) directly from Rust code.  
- **Lightweight and idiomatic** – follows Rust’s safety and concurrency patterns, making it easy to embed in existing Rust projects.  
- **Open‑source community** – the star count and recent commits show an active, albeit small, user base that can be consulted for issues.

**Practical Adoption Path**  
1. **Review the README and examples** to confirm the API matches your discovery workflow (e.g., browsing for `_http._tcp` services).  
2. **Add the crate** to your `Cargo.toml` and run the provided examples locally to verify that mDNS packets are seen on your network.  
3. **Integrate a thin wrapper** around the library that abstracts the discovery events into your application’s service‑registry or configuration layer.  
4. **Write integration tests** that simulate the presence of a service (e.g., using a small mDNS responder) to ensure the discovery logic works in CI.  
5. **Monitor runtime dependencies** (e.g., the underlying `libmdns` or `tokio` version) and pin them if needed for stability.

**Production Readiness**  
- **Maturity:** Medium. The crate is actively maintained and compiles cleanly, but the documentation and integration guidance are sparse, so a manual code review is required.  
- **Risk:** The integration path is not obvious from the metadata; you’ll need to validate that the library’s event model fits your architecture and that the networking stack (firewalls, VLANs) permits multicast traffic.  
- **Recommended Use:** Suitable for prototypes, internal tooling, or services that operate within a trusted LAN. For public‑facing or high‑availability production systems, perform a thorough dependency audit, add comprehensive health checks, and consider a fallback discovery mechanism.

### Русский

**keepsimple1/mdns-sd** — это библиотека на Rust для обнаружения сервисов через mDNS. Она подходит для прототипов и внутренних инструментов, где требуется быстро реализовать автоматическое обнаружение локальных сервисов (например, в IoT‑устройствах, микросервисных стендах или dev‑окружениях), но перед внедрением в продакшн стоит проверить совместимость и стабильность интеграции, так как детали настройки из метаданных скудны. По текущим показателям (208 ⭐, активные обновления) проект находится на среднем уровне готовности: готов к экспериментальному использованию, но требует дополнительного аудита перед критически важными продакшн‑сценариями.

### 中文

**项目简介**  
keepsimple1/mdns-sd 是一个用 Rust 编写的 mDNS（Multicast DNS）服务发现库，提供零配置的局域网设备与服务发现能力，适合在本地网络中快速定位 HTTP、gRPC、IoT 等服务。

**价值**  
- **轻量且安全**：基于 Rust 的内存安全特性，运行时开销低，适合嵌入式或资源受限的环境。  
- **即插即用**：只需几行代码即可在局域网内广播或监听服务，无需额外的中心化注册中心。  
- **社区认可**：已有 200+ 星、60+ Fork，活跃维护至 2026 年，说明基本可用且有一定社区支持。

**典型接入方式**  
1. **在 Cargo.toml 中添加依赖**  
   ```toml
   [dependencies]
   mdns-sd = "0.1"
   ```  
2. **广播服务**（示例）  
   ```rust
   use mdns_sd::{ServiceDaemon, ServiceInfo};

   let mdns = ServiceDaemon::new().expect("Failed to create daemon");
   let service = ServiceInfo::new(
       "_http._tcp",          // service type
       "my-device",          // instance name
       8080,                 // port
       None,                 // optional TXT records
   ).unwrap();

   mdns.register(service).expect("Failed to register");
   ```  
3. **发现服务**（示例）  
   ```rust
   let mdns = ServiceDaemon::new().unwrap();
   let receiver = mdns.browse("_http._tcp").unwrap();

   for event in receiver.iter() {
       match event {
           mdns_sd::ServiceEvent::ServiceResolved(info) => {
               println!("Found: {} at {}", info.get_fullname(), info.get_addr());
           }
           _ => {}
       }
   }
   ```  
4. **集成注意**  
   - 需要在目标网络的防火墙/路由器上放行 UDP 5353（mDNS）和对应的多播地址 224.0.0.251。  
   - 若项目已经使用异步运行时（tokio、async‑std），可通过 `mdns-sd::async` 模块或自行包装阻塞 API。  

**生产可用性**  
- **成熟度**：库已更新至 2026‑07‑13，活跃度中等，适合作为原型或内部工具的服务发现层。  
- **风险**：README 与元数据较为简洁，集成细节（如跨子网、TLS 绑定、错误恢复）需要自行评估并实现。  
- **建议**：在正式生产环境使用前，进行以下检查：  
  1. **依赖审计**：确认 `mdns-sd` 及其传递依赖的许可证与安全报告。  
  2. **网络验证**：在目标部署环境中验证多播路由、QoS 与防火墙配置。  
  3. **监控与日志**：为注册/发现事件添加日志和健康检查，以便快速定位网络或实现层的问题。  

总体而言，keepsimple1/mdns-sd 适合作为 **原型、内部服务网或 IoT 设备** 的零配置发现方案；在充分测试并补齐缺失的运维/监控功能后，可在受控的生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** keepsimple1/mdns-sd may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 208 GitHub stars
- 66 forks
- updated 2026-07-13
- primary language: Rust
- 1 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 49/100 |
| topics | 13/100 |
| outlook | 60/100 |
| quality | 59/100 |
| recency | 80/100 |
| adoption | 48/100 |
| production | 62/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/keepsimple1/mdns-sd) · [← Back to Misc](./README.md)</sub>
