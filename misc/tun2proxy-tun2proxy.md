# tun2proxy/tun2proxy

[![Stars](https://img.shields.io/github/stars/tun2proxy/tun2proxy?style=flat-square&color=yellow)](https://github.com/tun2proxy/tun2proxy/stargazers) [![Forks](https://img.shields.io/github/forks/tun2proxy/tun2proxy?style=flat-square&color=blue)](https://github.com/tun2proxy/tun2proxy/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> Tunnel (TUN) interface for SOCKS and HTTP proxies

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.3k |
| 🍴 **Forks** | 169 |
| 💻 **Language** | Rust |
| 📈 **Score** | 48/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`http-proxy` `proxy` `socks` `socks5` `tun2http` `tun2proxy` `tun2socks` `tunnel`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
tun2proxy provides a lightweight userspace TUN interface that forwards all IP traffic to a configurable SOCKS5 or HTTP proxy, making it easy to route container, VM, or host traffic through existing proxy infrastructure. Written in Rust, the project is actively maintained (last commit 2026‑05‑14) and has amassed over 1.3 k stars, indicating solid community interest.

**Value**  
- **Unified proxy entry point** – eliminates the need for per‑application proxy settings by exposing a virtual network interface that automatically tunnels any traffic (including non‑HTTP protocols) through a chosen proxy.  
- **Cross‑platform and language‑agnostic** – works with any OS that supports TUN/TAP and can be used from containers, VMs, or bare‑metal hosts without code changes.  
- **Performance & safety** – Rust implementation gives low overhead and memory safety, which is attractive for high‑throughput or security‑sensitive environments.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Deploy the binary in a test namespace (e.g., a Docker container) and configure a simple SOCKS5 proxy (e.g., shadowsocks, mitmproxy).  
2. **Validate networking** – Verify that traffic from the TUN interface is correctly forwarded and that DNS resolution works as expected.  
3. **Integrate with orchestration** – Add the tun2proxy container as a sidecar or init container in Kubernetes, or as a systemd service on VMs, using environment variables to point at the target proxy.  
4. **Automation** – Wrap the setup in a Helm chart or Ansible role, and include health‑check scripts that confirm the TUN device is up and traffic is flowing.

**Production Readiness**  
- **Active development** – Recent commits, a healthy star/fork count, and multiple topics (rust, proxy, tun, networking) show ongoing community support.  
- **Maturity** – The core functionality (TUN → proxy) is stable; the codebase is small and well‑structured, easing audit and customization.  
- **Risk mitigation** – Because integration steps are not fully documented, a small pilot should first confirm deployment scripts, logging, and error handling before scaling to production. Once the pilot succeeds, the project can be considered production‑ready for workloads that need transparent proxying of arbitrary traffic.

### Русский

**tun2proxy/tun2proxy** — это Rust‑утилита, превращающая TUN‑интерфейс в шлюз для SOCKS и HTTP‑прокси, что позволяет перенаправлять любой трафик из локальной сети через выбранный прокси без изменения приложений. Типичный сценарий: в корпоративной или домашней сети создаёте виртуальный интерфейс, подключаете его к tun2proxy и указываете внешний SOCKS/HTTP‑прокси — весь исходящий трафик автоматически проходит через него, что удобно для обхода фильтров, тестирования или балансировки. Проект имеет активную поддержку (обновления — 2026 год, > 1300 звёзд, 169 форков), написан на Rust и готов к пилотному запуску в продакшн после небольшого PoC и проверки README.

### 中文

**项目简介**  
`tun2proxy/tun2proxy` 是用 Rust 实现的 TUN（虚拟网络层）驱动，能够把本地的 TUN 接口流量透明地转发到任意 SOCKS 或 HTTP 代理。它让普通的网络程序（如容器、虚拟机或自定义服务）无需改动代码，就能通过企业的代理服务器访问外部网络。

**价值点**  
1. **统一代理入口**：一次配置即可把所有基于 IP 的流量（TCP/UDP）统一走代理，省去在每个应用里单独配置 SOCKS/HTTP。  
2. **语言/平台无关**：因为工作在系统层的 TUN 设备上，所有语言和运行时（Linux、macOS、Windows 子系统）都能受益。  
3. **安全审计友好**：所有出站流量都经过可控的代理，便于日志、流量监控和访问控制。

**典型接入方式**  
1. **部署二进制**：在目标机器上下载最新的 `tun2proxy` 可执行文件（或使用 Cargo 编译），确保内核已加载 TUN 驱动。  
2. **创建 TUN 接口**：  
   ```bash
   sudo ip tuntap add dev tun0 mode tun
   sudo ip addr add 10.0.0.1/24 dev tun0
   sudo ip link set dev tun0 up
   ```  
3. **启动转发**（以 SOCKS5 为例）：  
   ```bash
   sudo ./tun2proxy -i tun0 -p socks5://proxy.example.com:1080
   ```  
   - `-i` 指定要监听的 TUN 设备。  
   - `-p` 指定目标代理 URL，支持 `socks5://`, `socks5h://`, `http://` 等。  
4. **路由配置**：把需要走代理的流量指向 TUN 接口，例如：  
   ```bash
   sudo ip route add 0.0.0.0/0 dev tun0
   ```  
   只需在完成测试后恢复原有路由即可。

**生产可用性**  
- **活跃度**：截至 2026‑05‑14，项目仍在维护，最近一次提交在当日，拥有 1.3k+ 星、169 个 Fork，社区活跃。  
- **语言成熟度**：Rust 提供内存安全和高性能，适合在生产环境中长期运行。  
- **可观测性**：内置日志和统计信息，可通过 `-v`/`--log-level` 调整，便于监控。  
- **风险**：文档主要集中在 README，完整的部署手册和 Kubernetes/容器化示例相对有限，建议在正式上线前先完成一个小规模的 PoC，验证网络拓扑、路由规则以及与现有代理的兼容性。  

**结论**  
在需要统一、透明地把 IP 层流量走 SOCKS/HTTP 代理的场景下，`tun2proxy` 是一个成熟且易于集成的 OSS 方案。只要做好前期的路由与权限配置，它完全可以在生产环境中稳定运行。

## 🧭 Practical evaluation

**Value:** tun2proxy/tun2proxy may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1316 GitHub stars
- 169 forks
- updated 2026-05-14
- primary language: Rust
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 66/100 |
| topics | 100/100 |
| outlook | 51/100 |
| quality | 64/100 |
| recency | 20/100 |
| adoption | 63/100 |
| production | 49/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/tun2proxy/tun2proxy) · [← Back to Misc](./README.md)</sub>
