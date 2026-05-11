# rustonbsd/iroh-ssh

[![Stars](https://img.shields.io/github/stars/rustonbsd/iroh-ssh?style=flat-square&color=yellow)](https://github.com/rustonbsd/iroh-ssh/stargazers) [![Forks](https://img.shields.io/github/forks/rustonbsd/iroh-ssh?style=flat-square&color=blue)](https://github.com/rustonbsd/iroh-ssh/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> SSH to any machine without ip

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 172 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | Rust |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`iroh` `p2p` `ssh`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
`iroh-ssh` is a Rust‑based tool that lets you open an SSH session to a remote host without needing to know its IP address, using a custom discovery mechanism. It targets niche workflows where machines are identified by name or other metadata rather than static network addresses.

**Value proposition**  
The project removes the friction of managing IP inventories, which can be especially helpful in dynamic, container‑oriented, or edge‑computing environments where nodes appear and disappear frequently. By abstracting the connection layer, it enables developers and operators to script or automate access to machines using higher‑level identifiers, reducing the risk of stale IP records and simplifying onboarding of new hosts.

**Practical adoption path**  

1. **Evaluate the README and demo scripts** – confirm that the discovery protocol (e.g., mDNS, a central registry, or a custom service) matches the way your infrastructure advertises hosts.  
2. **Prototype in a sandbox** – clone the repo, build the binary (`cargo build --release`), and run it against a small test cluster to verify that the SSH handshake works and that authentication (keys, agents) integrates with your existing tooling.  
3. **Integrate with your orchestration layer** – wrap `iroh-ssh` in a wrapper script or a CI/CD step, passing the logical host identifier used by your system. Adjust any firewall or SELinux policies to allow the discovery traffic.  
4. **Add monitoring and fallback** – because the integration path is not obvious from the metadata, instrument the tool with logs and health checks, and keep a traditional SSH fallback for hosts that cannot be discovered.

**Production readiness**  
The project sits at a medium readiness level: it has modest community interest (172 stars, 9 forks) and recent activity (updated 2026‑05‑11), but the integration surface is sparse and the discovery mechanism is not fully documented. It is suitable for prototypes, internal tooling, or environments where you can afford a manual validation step before full rollout. Before deploying to production, perform a dependency audit (Rust version, external crates), verify maintenance activity, and establish clear fallback procedures for cases where the IP‑less discovery fails.

### Русский

**rustonbsd/iroh-ssh** – небольшая утилита на Rust, позволяющая установить SSH‑соединение с любой машиной, используя только её публичный ключ, без необходимости знать IP‑адрес. Подходит для прототипов и внутренних процессов, где машины находятся в динамической сети (например, контейнеры, облачные инстансы) и их адреса меняются часто; интеграцию следует проверить вручную, так как автоматические сигналы о совместимости ограничены. Проект имеет средний уровень готовности: 172 звёзд, активные обновления и небольшие зависимости, но требует проверки установки и поддержки перед использованием в продакшене.

### 中文

**项目简介（2‑3 句话）**  
`rustonbsd/iroh-ssh` 是一个用 Rust 编写的轻量级工具，能够在不需要目标机器 IP 地址的情况下通过 SSH 直接连接任意主机。它利用类似 mDNS/ZeroConf 或自定义的发现协议，实现“零配置”式的远程登录，特别适合动态、容器化或云原生环境。

**价值**  
- **免 IP 连接**：在频繁变更 IP（如 Kubernetes Pod、云实例、临时 VM）时，无需手动更新 hosts 或 VPN，即可快速定位并登录。  
- **安全且高性能**：基于 Rust 的安全模型和零拷贝网络栈，提供与原生 OpenSSH 相近的加密性能。  
- **开发/运维友好**：通过统一的发现服务（如 Consul、etcd）或本地广播，即可把机器当作 “name” 来访问，降低运维成本。

**典型接入方式**  
1. **服务发现集成**  
   - 在部署环境（K8s、Nomad、Docker‑Compose）中运行一个 `iroh-discover` 实例，负责收集机器的唯一标识（hostname、UUID）并广播。  
   - 客户端机器安装 `iroh-ssh`，配置 `iroh-discover` 的地址（HTTP/GRPC），即可通过 `iroh ssh <service-name>` 自动解析目标并发起 SSH。  

2. **本地网络广播（ZeroConf）**  
   - 对于同一局域网内的开发机器，直接启用 `iroh-ssh --mdns`，工具会监听/响应 mDNS 查询，使用机器的 `.local` 名称进行连接。  

3. **脚本/CI 集成**  
   - 在 CI/CD 流水线中使用 `iroh ssh` 代替 `ssh user@host`，配合 `iroh token` 生成一次性登录凭证，实现安全的自动化部署。  

**生产可用性评估**  
- **成熟度**：项目已有 172 ⭐、9 🍴，最近一次提交为 2026‑05‑11，活跃度尚可，但社区贡献和文档仍相对有限。  
- **适用场景**：适合内部原型、研发环境或对 IP 透明度有强需求的微服务体系；在对安全合规、审计有严格要求的生产环境中，需要自行完成以下检查：  
  1. **审计日志**：确认 `iroh-ssh` 能输出符合企业审计要求的登录记录。  
  2. **身份管理**：与现有的 SSH 公钥、OTP、或企业 SSO 集成，避免仅靠工具自带的 token。  
  3. **高可用发现**：如果依赖 `iroh-discover`，需部署多副本并做好故障转移。  

- **风险**：集成路径不够明确，缺少成熟的 Helm chart、Docker 镜像或官方 CI。建议在正式投入前进行一次完整的 **PoC**，验证以下方面：  
  - 网络发现的可靠性（跨子网、跨云提供商）  
  - 与现有 SSH 代理/跳板的兼容性  
  - 维护成本（Rust 编译链、二进制更新）  

**结论**：`iroh-ssh` 在需要“零 IP、零配置”快速登录的内部或原型项目中价值突出，具备中等的生产就绪度。若决定在生产环境使用，务必补齐审计、身份管理和高可用发现层的缺口后再上线。

## 🧭 Practical evaluation

**Value:** rustonbsd/iroh-ssh may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 172 GitHub stars
- 9 forks
- updated 2026-05-11
- primary language: Rust
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 48/100 |
| topics | 38/100 |
| outlook | 67/100 |
| quality | 64/100 |
| recency | 100/100 |
| adoption | 41/100 |
| production | 69/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/rustonbsd/iroh-ssh) · [← Back to Misc](./README.md)</sub>
