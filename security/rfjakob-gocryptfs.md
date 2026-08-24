# rfjakob/gocryptfs

[![Stars](https://img.shields.io/github/stars/rfjakob/gocryptfs?style=flat-square&color=yellow)](https://github.com/rfjakob/gocryptfs/stargazers) [![Forks](https://img.shields.io/github/forks/rfjakob/gocryptfs?style=flat-square&color=blue)](https://github.com/rfjakob/gocryptfs/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Encrypted overlay filesystem written in Go

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.5k |
| 🍴 **Forks** | 298 |
| 💻 **Language** | Go |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`encryption` `filesystem` `fuse` `gcm` `golang`

## 🎯 Categories

Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
gocryptfs is an open‑source encrypted overlay filesystem written in Go that provides on‑the‑fly, per‑file encryption with a simple, POSIX‑compatible interface. It is actively maintained, widely adopted (4.5 k ★, 300 forks), and can be dropped into existing workflows to protect data at rest without altering applications. The project’s strong community signals make it a solid candidate for a security‑focused pilot.

**Value**  
- **Early security & privacy enforcement:** By encrypting files transparently at the filesystem layer, gocryptfs catches data‑leak risks before they reach downstream services or backups.  
- **Minimal friction:** It works like any regular mount point, so developers and operators can continue using familiar tools while gaining strong confidentiality guarantees.  
- **Audit‑ready:** The clear Go codebase and active issue tracker simplify security reviews and compliance checks.

**Practical Adoption Path**  
1. **Proof‑of‑Concept:** Spin up a small test environment (e.g., a single VM or container) and mount a test directory with gocryptfs following the README. Verify that existing applications read/write files unchanged while the data on disk is encrypted.  
2. **Integration Checklist:** Review licensing, confirm the maintainer’s response cadence, and run a static analysis scan of the Go source.  
3. **Pilot Deployment:** Deploy gocryptfs on a non‑critical service (e.g., log storage or temporary workspaces) and instrument monitoring for mount health and performance.  
4. **Scale‑out:** After successful pilot metrics, roll out to broader workloads, optionally adding key‑management integration (e.g., HashiCorp Vault) for automated secret handling.

**Production Readiness**  
- **Maturity:** Recent commits (as of 2026‑07‑12), high star/fork count, and usage in several production projects indicate a stable codebase.  
- **Performance:** Go implementation offers low overhead; benchmarks show comparable throughput to other user‑space encryption tools.  
- **Supportability:** Active maintainers and a responsive community provide timely issue resolution and security patches.  
Overall, gocryptfs is production‑ready for a serious pilot, with the primary remaining steps being a final license/security review and integration testing in your specific environment.

### Русский

**Краткое резюме:** gocryptfs — это высокопроизводительная файловая система‑надстройка с прозрачным шифрованием, написанная на Go, которая позволяет сразу внедрять контроль доступа и защиту конфиденциальных данных в процессе разработки. Типичный сценарий — небольшое пилотное внедрение (например, в виде mount‑точки для тестовых репозиториев) с последующей проверкой README и базовых функций, после чего система может быть масштабирована до полноценного production‑окружения. По уровню готовности проект считается «high»: активные коммиты, более 4500 звёзд, широкое принятие и зрелая экосистема, однако перед запуском в прод необходимо окончательно проверить лицензию, текущий security‑posture и наличие активных мейнтейнеров.

### 中文

**项目简介**  
rfjakob/gocryptfs 是用 Go 实现的加密层文件系统，提供透明的文件加密与解密，能够在任何支持 FUSE 的平台上以目录覆盖的方式安全存储数据。  

**价值**  
- 在代码提交、CI/CD 或本地开发阶段即对敏感文件进行加密，帮助团队提前发现安全与隐私风险。  
- 通过统一的加密入口，简化后续的权限审计、合规检查和数据泄露防护。  

**典型接入方式**  
1. **小规模验证**：在测试环境或 CI 步骤中创建一个临时的加密挂载点（`gocryptfs -init /path/to/crypt` → `gocryptfs /path/to/crypt /path/to/mount`），将需要保护的目录映射进去，验证加解密性能和兼容性。  
2. **CI/CD 集成**：在构建脚本中加入 `gocryptfs` 命令，将敏感配置文件或制品加密后再上传至制品库或对象存储。  
3. **生产部署**：在容器或虚拟机启动脚本里先挂载加密目录，再将业务进程指向挂载点，实现“加密即文件系统”。  

**生产可用性**  
- **成熟度**：GitHub ★4523，最近一次提交在 2026‑07‑12，活跃的维护者和持续的社区贡献表明项目已进入稳健期。  
- **可行性**：作为 OSS 候选，具备完整的文档、示例和常见问题解答，且依赖 Go 语言，易于在微服务或容器化环境中编译和部署。  
- **风险**：需进一步审查许可证兼容性、上游安全报告以及维护者响应速度，但整体风险较低，适合作为安全加固的首批试点。  

**结论**：gocryptfs 在安全、隐私保护以及合规审计方面提供了轻量且高效的加密层，建议先在非关键业务做 PoC 验证，随后在生产环境中逐步推广。

## 🧭 Practical evaluation

**Value:** rfjakob/gocryptfs helps catch security and privacy issues earlier in the workflow.

**Best use cases**

- strengthen security checks
- add auth or privacy controls
- audit risk earlier

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4523 GitHub stars
- 298 forks
- updated 2026-07-12
- primary language: Go
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 78/100 |
| topics | 63/100 |
| outlook | 57/100 |
| quality | 67/100 |
| recency | 40/100 |
| adoption | 73/100 |
| production | 57/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/rfjakob/gocryptfs) · [← Back to Security](./README.md)</sub>
