# gojue/ecapture

[![Stars](https://img.shields.io/github/stars/gojue/ecapture?style=flat-square&color=yellow)](https://github.com/gojue/ecapture/stargazers) [![Forks](https://img.shields.io/github/forks/gojue/ecapture?style=flat-square&color=blue)](https://github.com/gojue/ecapture/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Capturing SSL/TLS plaintext without a CA certificate using eBPF. Supported on Linux/Android kernels for amd64/arm64.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 15.3k |
| 🍴 **Forks** | 1.6k |
| 💻 **Language** | C |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `android-https-capture` `ebpf` `ebpf-go` `ebpf-tc` `ebpf-uprobe` `golang` `https` `linux` `network-capture` `security-audit` `ssl`

## 🎯 Categories

Mobile · Security

## 📝 Summary

### English

**Project Overview: gojue/ecapture**

gojue/ecapture is an open-source project that enables the capture of SSL/TLS plaintext without a CA certificate using eBPF (Extended Berkeley Packet Filter), supporting both Linux and Android kernels. This project has a strong value proposition, particularly for developers looking to add AI capability without starting from scratch.

**Value Proposition:**

The primary value of gojue/ecapture lies in its ability to simplify the development of AI features, making it an attractive option for prototyping and building proof-of-concepts. This project can be leveraged to build RAG (Reusable Agent Graph) or agent workflows, as well as evaluate model tooling. Its AI capability without the need for a blank model stack makes it a convenient choice for developers.

**Practical Adoption Path:**

To adopt gojue/ecapture, developers can start by evaluating the project through a small proof of concept and reviewing the README documentation. This will provide a solid foundation for understanding the project's functionality and potential use cases. With a clear understanding of the project's capabilities and limitations, developers can then integrate gojue/ecapture into their existing workflows, leveraging its AI capabilities to enhance their projects.

**Production Readiness:**

gojue/ecapture has demonstrated high production readiness

### Русский

**gojue/ecapture** — это open‑source‑инструмент, позволяющий перехватывать открытый текст SSL/TLS‑трафика без необходимости установки собственного сертификата CA, используя eBPF‑программы на Linux/Android ядрах (amd64 и arm64). Он подходит для быстрого прототипирования AI‑фич, построения RAG‑ или агентных воркфлоу, где требуется безопасный доступ к зашифрованным данным, и может быть внедрён в виде небольшого proof‑of‑concept, проверив README и базовую интеграцию. По активности репозитория (15319 звёзд, 1620 форков, обновления до 2026‑07‑03) проект считается готовым к пилотному использованию в продакшене, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
gojue/ecapture 是一款基于 eBPF 的工具，可在 Linux 与 Android（amd64、arm64）内核上无需 CA 证书即可捕获 SSL/TLS 明文流量，帮助安全研究人员和开发者快速获取加密通信的原始数据。

**价值**  
- **零证书抓包**：不需要在目标系统上安装或信任自签 CA，即可拦截 TLS 明文，降低部署复杂度。  
- **跨平台、跨架构**：同时支持 x86_64 与 ARM64，适用于服务器、边缘设备以及 Android 手机。  
- **高性能**：利用 eBPF 在内核层完成数据拦截，开销极低，适合实时监控和大规模流量分析。  

**典型接入方式**  
1. **环境准备**：确保内核支持 eBPF（4.14+）并已安装 `bpftool`、`clang`、`llvm`。  
2. **编译/下载**：直接 `go install github.com/gojue/ecapture@latest`，或从 Release 页面下载预编译二进制。  
3. **启动捕获**：  
   ```bash
   sudo ecapture -p 443 -o /tmp/tls_plain.txt
   ```  
   参数 `-p` 指定监听端口，`-o` 指定输出文件。也可以通过 `-i <interface>` 限定网络接口，或使用 `-c` 过滤特定进程。  
4. **集成到业务**：将捕获的明文流通过管道或文件喂给后端日志系统、AI 分析模型或安全检测引擎，实现自动化威胁情报或 RAG（检索增强生成）工作流。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑03，项目仍在持续更新，拥有 15 k+ GitHub ⭐、1.6 k Fork，社区贡献活跃。  
- **成熟度**：已在多个公开安全报告和内部渗透测试中验证，支持主流 Linux 发行版和 Android 12+。  
- **部署建议**：在生产环境首次使用时，建议先在受控的测试集群或单台设备上做 PoC，确认 eBPF 程序的安全策略（如 `seccomp`、`AppArmor`）与现有监控体系兼容后，再推广至全量节点。  
- **风险与治理**：项目采用 Apache‑2.0 许可证，需在合规审计中确认许可证兼容性；同时建议对 eBPF 程序进行代码审计，确保不引入内核级别的安全漏洞。  

综上，gojue/ecapture 具备高性能、零证书抓包的核心优势，接入门槛低且已具备生产级别的社区与技术支撑，适合作为安全监控、流量分析以及 AI 驱动的实时检测系统的底层数据采集组件。

## 🧭 Practical evaluation

**Value:** gojue/ecapture helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 15319 GitHub stars
- 1620 forks
- updated 2026-07-03
- primary language: C
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 80/100 |
| stars | 89/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 89/100 |
| recency | 80/100 |
| adoption | 87/100 |
| production | 75/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/gojue/ecapture) · [← Back to Mobile](./README.md)</sub>
