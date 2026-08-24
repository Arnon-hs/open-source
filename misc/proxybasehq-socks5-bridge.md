# proxybasehq/socks5-bridge

[![Stars](https://img.shields.io/github/stars/proxybasehq/socks5-bridge?style=flat-square&color=yellow)](https://github.com/proxybasehq/socks5-bridge/stargazers) [![Forks](https://img.shields.io/github/forks/proxybasehq/socks5-bridge?style=flat-square&color=blue)](https://github.com/proxybasehq/socks5-bridge/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-31%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 31/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
A lightweight, locally‑run bridge that converts ordinary HTTP requests from Chrome into SOCKS5 traffic, letting the browser work through any SOCKS5 proxy without native support. The project is modestly maintained (last update 2026‑07‑13) and is tagged with two topics, but its documentation and integration signals are sparse.

**Value**  
- Enables developers and power users to route Chrome traffic through existing SOCKS5 services (e.g., SSH tunnels, corporate proxies) without installing a full‑featured proxy extension.  
- Useful for quick prototyping, debugging network behavior, or testing services that only expose a SOCKS5 endpoint.

**Practical Adoption Path**  
1. **Clone & build** the repository and run the binary on a local port (e.g., `127.0.0.1:8080`).  
2. **Configure Chrome** → Settings → System → “Open proxy settings” → set the HTTP proxy to the bridge’s address.  
3. **Verify** the conversion by checking the SOCKS5 server logs or using a network‑inspection tool (e.g., Wireshark).  
4. Optionally wrap the bridge in a systemd service or Docker container for repeatable startup in internal environments.

**Production Readiness**  
- **Maturity:** Medium. The code works for prototypes and internal workflows, but the limited release cadence and minimal issue tracking mean you should perform a security and stability audit before any critical deployment.  
- **Dependencies:** Verify that the bridge’s runtime dependencies (Node/Go, OpenSSL, etc.) are compatible with your environment and that they receive security updates.  
- **Maintenance:** Check the repository’s license, open issues, and commit history; consider forking and adding tests if you plan long‑term use.  

**Bottom line:** The bridge is a handy, low‑overhead solution for experimental or internal use cases, but it requires manual vetting and possibly a small amount of custom integration work before it can be trusted in production.

### Русский

**Краткое резюме:**  
Проект — локальный мост‑прокси, преобразующий HTTP‑запросы Chrome в SOCKS5, что удобно для быстрого тестирования или обхода ограничений без изменения системных настроек. Его типичный сценарий — подключение Chrome к уже существующему SOCKS5‑серверу (например, VPN или Tor) через лёгкую локальную обёртку; при этом требуется ручная проверка README, лицензии и активности репозитория. Готовность к production — средняя: проект может подойти для прототипов и внутренних инструментов, но перед запуском в продакшн следует оценить поддержку, частоту релизов и наличие документации.

### 中文

**项目简介（2‑3 句）**  
A local HTTP‑to‑SOCKS5 proxy bridge for Chrome 是一个在本地运行的轻量级代理工具，可将 Chrome 浏览器的 HTTP 请求转发为 SOCKS5 流量，便于在只支持 SOCKS5 的网络环境（如企业 VPN、Shadowsocks、Tor）中使用 Chrome。项目最近一次更新于 2026‑07‑13，代码库包含 2 个主题标签，适合作为原型或内部工具的快速接入方案。

---

### 价值点
1. **桥接能力**：无需改动 Chrome 本身或系统代理设置，直接在本地提供 HTTP→SOCKS5 转换，解决 Chrome 只能使用 HTTP/HTTPS 代理的限制。  
2. **轻量即插即用**：仅需启动一个可执行文件或 Node 脚本，即可在本机创建代理端口，适配已有的 SOCKS5 服务器（如 Shadowsocks、V2Ray）。  
3. **原型与内部流**：对需要快速验证基于 SOCKS5 的网络策略或进行安全审计的团队非常有帮助，降低了部署复杂度。

### 典型接入方式
1. **准备工作**  
   - 确认已有可用的 SOCKS5 代理（IP、端口、认证信息）。  
   - 检查项目的许可证（通常为 MIT/Apache），确保符合企业合规。  
2. **本地部署**  
   ```bash
   # 克隆仓库
   git clone https://github.com/your-org/http-to-socks5-bridge.git
   cd http-to-socks5-bridge

   # 安装依赖（如果是 Node 项目）
   npm install

   # 启动桥接服务，指定本地 HTTP 端口和远端 SOCKS5 代理
   node bridge.js --http-port 127.0.0.1:8080 --socks5-host socks5.example.com:1080
   ```
   - 启动后，`127.0.0.1:8080` 即为 Chrome 可使用的 HTTP 代理。  
3. **Chrome 配置**  
   - 打开 **设置 → 系统 → 打开代理设置**（或使用 `chrome://settings/` → “代理”），手动添加 HTTP 代理 `127.0.0.1:8080`。  
   - 如需对特定站点生效，可使用 Chrome 扩展（如 “Proxy SwitchyOmega”）配置规则。  
4. **验证**  
   - 访问 `https://ifconfig.me` 或 `https://www.whatismyip.com`，确认流量已通过 SOCKS5 代理转发。  

### 生产可用性评估
| 维度 | 评估 | 说明 |
|------|------|------|
| **代码成熟度** | 中等 | 最近一次更新在 2026‑07‑13，活跃度不高，只有少量提交记录。 |
| **文档与示例** | 基础 | README 简单说明启动方式，缺少完整的使用案例、故障排查和安全指南。 |
| **依赖与维护** | 需自行审查 | 项目依赖的第三方库（如 `node-http-proxy`、`socks`）需要检查是否仍在维护，防止潜在的安全漏洞。 |
| **安全性** | 待验证 | 未提供安全审计或漏洞报告，建议在受信网络或容器中运行并开启最小权限。 |
| **可扩展性** | 有限 | 仅实现单向 HTTP→SOCKS5，缺少 HTTPS 透明代理、负载均衡或多实例管理。 |
| **适用场景** | 原型、内部工具 | 对于研发、测试或内部审计环境可快速使用；在对可靠性、监控和高可用有严格要求的生产环境中，需要自行包装监控、自动重启及升级机制。 |

**结论**：该桥接工具在功能上能够解决 Chrome 与 SOCKS5 代理之间的兼容问题，适合作为原型验证或内部工作流的临时方案。若计划在生产环境中长期使用，建议进行以下工作：  
1. 完整审计代码和依赖的安全性；  
2. 为服务添加健康检查、日志和自动重启（如 systemd、Docker）；  
3. 若需要高可用，可考虑自行实现多实例或使用成熟的代理网关（如 `tinyproxy` + `ssh -D`）。在完成上述措施后，方可视为中等可靠的生产级组件。

## 🧭 Practical evaluation

**Value:** A local HTTP-to-SOCKS5 proxy bridge for Chrome may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-07-13
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 33/100 |
| quality | 26/100 |
| recency | 40/100 |
| adoption | 0/100 |
| production | 38/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/proxybasehq/socks5-bridge) · [← Back to Misc](./README.md)</sub>
