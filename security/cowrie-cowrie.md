# cowrie/cowrie

[![Stars](https://img.shields.io/github/stars/cowrie/cowrie?style=flat-square&color=yellow)](https://github.com/cowrie/cowrie/stargazers) [![Forks](https://img.shields.io/github/forks/cowrie/cowrie?style=flat-square&color=blue)](https://github.com/cowrie/cowrie/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Cowrie SSH/Telnet Honeypot https://docs.cowrie.org/

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6.4k |
| 🍴 **Forks** | 1k |
| 💻 **Language** | Python |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`attacker` `cowrie` `cowrie-ssh` `deception` `decoy` `honeypot` `kippo` `scp` `security` `sftp` `ssh` `telnet`

## 🎯 Categories

Security

## 📝 Summary

### English

**Summary**  
Cowrie is an open‑source SSH and Telnet honeypot written in Python that emulates vulnerable services to capture malicious login attempts, command execution, and file uploads. By logging attacker behavior in a controlled environment, it lets security teams surface threats, privacy breaches, and misconfigurations far earlier in the development and operations pipeline.  

**Value**  
- Provides rich, high‑fidelity telemetry (session recordings, file downloads, command histories) that can be fed into SIEMs, threat‑intel platforms, or automated detection rules.  
- Helps security and DevOps teams validate authentication and privacy controls, audit exposure risk, and fine‑tune intrusion‑detection signatures before they reach production.  

**Practical adoption path**  
1. **Proof of concept** – Deploy Cowrie in a isolated VM or container using the official Docker image; follow the README to configure logging, network bindings, and data export.  
2. **Integration** – Connect Cowrie’s JSON/SQLite logs to existing monitoring pipelines (e.g., ELK, Splunk, or a custom webhook) and verify that attacker sessions are captured correctly.  
3. **Scale** – Harden the host, enable TLS for log transport, and add multiple instances behind a load balancer for broader network coverage.  

**Production readiness**  
Cowrie scores high on readiness: it has >6 400 stars, >1 000 forks, recent commits (as of 2026‑06‑24), active community support, and a mature Python codebase. The project shows strong ecosystem signals and is already used in many enterprise honeypot deployments, making it a solid OSS candidate for a serious pilot—pending final license and maintainer security reviews.

### Русский

Cowrie — это открытый SSH/Telnet‑honeypot, который позволяет обнаруживать попытки несанкционированного доступа и другие угрозы безопасности на ранних стадиях, тем самым ускоряя аудит рисков и усиление контроля доступа. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, следуя README, и постепенно интегрировать его в цепочку мониторинга и реагирования на инциденты. Проект считается готовым к production: активные коммиты, более 6 тыс. звёзд, широкое принятие в сообществе и стабильная экосистема Python делают его надёжным кандидатом для серьёзного пилотного развертывания.

### 中文

**项目简介（2‑3 句话）**  
Cowrie 是一款基于 Python 的开源 SSH/Telnet 蜜罐，能够模拟真实的服务器环境并记录攻击者的交互行为。它通过捕获登录尝试、命令执行和文件下载等细节，为安全团队提供可操作的情报，帮助提前发现潜在的安全与隐私风险。  

**价值**  
- **提前预警**：在攻击者真正入侵生产系统前，就能在受控环境中捕获并分析其行为。  
- **提升安全检测**：提供丰富的日志和会话记录，可用于完善 IDS/IPS、SIEM、威胁情报平台的规则库。  
- **审计与合规**：完整记录攻击路径和工具，帮助满足审计、合规以及内部风险评估的需求。  

**典型接入方式**  
1. **快速 PoC**：在一台隔离的服务器或容器中按照官方 README 部署 Cowrie（Docker 镜像或源码），并配置日志输出到本地或远程的 ELK/Prometheus 等监控系统。  
2. **日志集成**：通过 Filebeat、Fluent Bit 或自建脚本将 `cowrie.log`、`cowrie.json` 等文件推送至中心日志平台，随后在 SIEM 中编写对应的检测规则。  
3. **自动化扩展**：利用 Cowrie 提供的 `logoutput` 插件或自定义脚本，将捕获的恶意二进制文件自动上传至病毒分析沙箱（如 Cuckoo）进行进一步检测。  

**生产可用性**  
- **成熟度高**：GitHub ★6427、Fork ★1039，最近一次提交在 2026‑06‑24，活跃的维护者和社区支撑。  
- **稳定性**：已在多个公开和商业项目中作为核心蜜罐组件使用，具备完善的文档、Docker 镜像以及多语言插件。  
- **风险可控**：项目采用 GPL‑3.0 许可证，无明显元数据泄露风险；但在正式投产前仍需对其依赖库进行一次安全审计，并确认与内部合规政策匹配。  

综上所述，Cowrie 具备高可用的生产级别，适合作为安全监测与风险审计的前置层，建议先在受控环境完成 PoC，验证日志链路和告警规则后，再逐步推广至更大规模的部署。

## 🧭 Practical evaluation

**Value:** cowrie/cowrie helps catch security and privacy issues earlier in the workflow.

**Best use cases**

- strengthen security checks
- add auth or privacy controls
- audit risk earlier

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 6427 GitHub stars
- 1039 forks
- updated 2026-06-24
- primary language: Python
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 75/100 |
| stars | 81/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 76/100 |
| recency | 40/100 |
| adoption | 79/100 |
| production | 61/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/cowrie/cowrie) · [← Back to Security](./README.md)</sub>
