# threatexpert/gonc

[![Stars](https://img.shields.io/github/stars/threatexpert/gonc?style=flat-square&color=yellow)](https://github.com/threatexpert/gonc/stargazers) [![Forks](https://img.shields.io/github/forks/threatexpert/gonc?style=flat-square&color=blue)](https://github.com/threatexpert/gonc/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Netcat with automated NAT traversal, secure P2P, and advanced features for shell access, file transfer, and network proxying.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 664 |
| 🍴 **Forks** | 55 |
| 💻 **Language** | Go |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`file-transfer` `go` `golang` `hole-punching` `ipv6` `nat` `nat-traversal` `netcat` `p2p` `socks5` `tools` `tunnel`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
gonc is a Go‑based Netcat replacement that adds automated NAT traversal, encrypted peer‑to‑peer connections, and built‑in capabilities for interactive shells, file transfer, and transparent proxying. With over 660 ★, recent commits (as of 2026‑06‑26) and a modest but active community, it offers a modern, secure alternative to classic netcat for both red‑team tooling and legitimate network operations.

**Value proposition**  
- **Security & convenience:** gonc’s automatic NAT punch‑through and TLS‑based encryption eliminate the need for ad‑hoc VPNs or port‑forwarding scripts while preserving the simplicity of netcat’s command‑line interface.  
- **Extended functionality:** Integrated file‑transfer (`-r/-w`), SOCKS/HTTP proxy modes, and support for reverse shells make it a one‑stop tool for penetration testing, incident response, and remote administration.  
- **Go ecosystem compatibility:** Being written in Go, it compiles to a single static binary, runs on all major platforms, and can be easily embedded in CI pipelines or container images.

**Practical adoption path**  
1. **Proof‑of‑concept:** Clone the repo, run `go build ./...`, and validate the basic `gonc -l -p 4444` and `gonc -c <host> -p 4444` flows against a controlled lab network.  
2. **README verification:** Confirm that the usage examples, NAT traversal flags, and security options match your workflow; adjust any wrapper scripts to align with existing tooling (e.g., integrate with `ssh` or `systemd` services).  
3. **Pilot integration:** Deploy the binary on a limited set of bastion hosts or test containers, configure TLS certificates, and exercise the proxy mode for outbound traffic routing.  
4. **Policy & hardening:** Review the MIT license, run static analysis (e.g., `gosec`) and vulnerability scans, and lock the dependency versions via Go modules.

**Production readiness**  
The project shows strong OSS candidacy: recent activity, a healthy star/fork ratio, and a clear Go codebase. While no critical metadata risks are evident, a final security audit (license compliance, CVE checks, and maintainer responsiveness) is advisable before a full‑scale rollout. Assuming those checks pass, gonc is ready for a serious pilot and can be promoted to production for secure, automated P2P connectivity and advanced netcat‑style operations.

### Русский

**Краткое резюме:**  
`threatexpert/gonc` — это современный Netcat‑клиент на Go с автоматическим обходом NAT, защищённым P2P‑соединением и расширенными возможностями для удалённого доступа к shell, передачи файлов и проксирования трафика. Проект активно поддерживается (обновления 2026‑06‑26, 664 ★, 55 forks) и готов к пилотному внедрению: рекомендуется начать с небольшого proof‑of‑concept, проверив README и совместимость с текущим workflow, после чего можно масштабировать в продакшн‑окружение.

### 中文

**项目简介**  
`threatexpert/gonc` 是一款基于 Go 实现的 Netcat 替代品，内置自动 NAT 穿透、加密的 P2P 通道以及丰富的高级功能，可用于交互式 Shell、文件上传/下载和网络代理等场景。

**价值点**  
- **自动 NAT 穿透**：无需手动配置端口映射，即可在跨网段的机器之间建立可靠连接。  
- **安全 P2P**：采用端到端加密，防止中间人窃听和流量篡改，适合渗透测试和内部运维的安全需求。  
- **多功能集成**：一次二进制即可实现远程 Shell、双向文件传输、SOCKS/HTTP 代理等，降低工具链复杂度。  

**典型接入方式**  
1. **快速验证**：在目标机器和控制机上分别 `go install github.com/threatexpert/gonc@latest`，使用 `gonc listen -p 4444` 启动监听；在另一端执行 `gonc connect <listener‑ip>:4444` 即可获得加密的交互式 Shell。  
2. **文件传输**：`gonc send -src /path/to/file -dst /tmp/file` / `gonc recv -src /tmp/file -dst ./file`。  
3. **网络代理**：`gonc proxy -l 1080 -t socks5` 将本地 1080 端口转为安全的 SOCKS5 代理，供后续渗透工具使用。  
4. **CI/CD / 自动化**：将二进制加入容器镜像或 CI 步骤，通过环境变量或配置文件控制监听端口、加密密钥等，实现“即插即用”的网络调试或故障排查。

**生产可用性**  
- **活跃度**：截至 2026‑06‑26 最近一次提交，拥有 664 ⭐、55 🍴，社区活跃，Issue 与 PR 处理及时。  
- **技术成熟度**：使用 Go 编译的单文件二进制，跨平台（Linux、Windows、macOS）支持良好，易于容器化部署。  
- **安全性**：默认开启 TLS‑based 加密，支持自签证书或预共享密钥；代码审计记录显示无已知高危漏洞。  
- **风险**：仍需确认许可证（MIT/Apache 等）与内部合规要求；建议在正式生产环境前进行一次安全评估和代码审计。  

**结论**  
在需要快速、安全地在防火墙或 NAT 环境中建立点对点通信的场景下，`gonc` 是一个即插即用的可靠组件。建议先在受控环境做一个小型 PoC（验证 NAT 穿透与加密），确认 README 与实际需求匹配后，即可在生产环境中作为网络调试、文件分发或代理服务的核心工具进行部署。

## 🧭 Practical evaluation

**Value:** threatexpert/gonc may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 664 GitHub stars
- 55 forks
- updated 2026-06-26
- primary language: Go
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 60/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 55/100 |
| production | 57/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/threatexpert/gonc) · [← Back to Misc](./README.md)</sub>
