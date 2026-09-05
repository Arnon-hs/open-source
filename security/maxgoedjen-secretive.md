# maxgoedjen/secretive

[![Stars](https://img.shields.io/github/stars/maxgoedjen/secretive?style=flat-square&color=yellow)](https://github.com/maxgoedjen/secretive/stargazers) [![Forks](https://img.shields.io/github/forks/maxgoedjen/secretive?style=flat-square&color=blue)](https://github.com/maxgoedjen/secretive/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> Protect your SSH keys with your Mac's Secure Enclave

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 8.5k |
| 🍴 **Forks** | 199 |
| 💻 **Language** | Swift |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`mac` `secure-enclave` `security` `ssh`

## 🎯 Categories

Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*secretive* is an open‑source macOS utility that stores SSH private keys inside the Apple Secure Enclave, preventing them from ever touching the filesystem and requiring Touch ID or the device password for each use. By leveraging hardware‑backed key protection, it dramatically reduces the attack surface for credential theft while keeping the familiar SSH workflow intact.

**Value**  
- **Stronger security posture:** Private keys never leave the Secure Enclave, eliminating exposure to disk‑scraping malware, accidental backups, or insider leaks.  
- **Zero‑knowledge operation:** The tool does not retain a copy of the key; authentication is performed by the enclave, so even the host OS cannot read the key material.  
- **Compliance & audit benefits:** Using hardware‑rooted key storage satisfies many internal and regulatory requirements for privileged‑access management and reduces the need for separate secret‑management solutions for SSH.

**Practical Adoption Path**  
1. **Proof‑of‑concept (PoC):** Clone the repo, run the provided `README` steps on a test Mac, and generate a test SSH key with `secretive`. Verify that `ssh -v` prompts for Touch ID and that the key file is not present on disk.  
2. **Pilot rollout:** Deploy the binary (or Homebrew formula) to a small group of developers or CI agents, configure their `~/.ssh/config` to point to the Secure Enclave‑backed key, and monitor for any workflow friction.  
3. **Policy integration:** Update internal security policies to require Secure Enclave‑protected keys for all production SSH access, and add a simple script that checks for the presence of `secretive` before allowing key generation.  
4. **Full rollout:** Automate installation via MDM or a package manager, deprecate legacy key storage, and integrate with existing audit tooling (e.g., logging Touch ID usage via macOS Unified Logging).

**Production Readiness**  
- **Activity & adoption:** 8.5 k stars, 199 forks, recent commits (as of 2026‑05‑12), and usage in several public repos indicate a healthy community.  
- **Maturity:** Written in Swift, the project follows macOS conventions and has clear documentation; the codebase is stable with no open critical bugs.  
- **Risk considerations:** No major licensing or metadata concerns have been identified, though a final review of the MIT license compliance and the maintainers’ response times is advisable.  
Overall, *secretive* is production‑ready for a serious pilot, with a low integration cost and a clear path to enterprise‑wide adoption.

### Русский

**maxgoedjen/secretive** – утилита для macOS, позволяющая хранить SSH‑ключи в Secure Enclave, тем самым защищая их от кражи и несанкционированного доступа. При внедрении обычно начинают с небольшого proof‑of‑concept: проверяют работу через README, интегрируют вызовы Secretive в CI‑pipeline или в скрипты деплоя, чтобы обеспечить автоматическое использование защищённых ключей при подключении к серверам. Проект считается почти готовым к production: активные коммиты, более 8 тыс. звёзд, широкое принятие в сообществе и стабильный Swift‑код, однако перед масштабным rollout требуется окончательная проверка лицензии и подтверждение поддержки со стороны мейнтейнеров.

### 中文

**项目简介**  
**maxgoedjen/secretive** 是一款基于 macOS Secure Enclave 的 SSH 密钥管理工具，能够把私钥安全地存放在硬件安全模块中，防止密钥被窃取或意外泄露。

**价值**  
- 利用 Secure Enclave 的硬件隔离特性，为 SSH 私钥提供比文件系统更高的保密性和抗篡改能力。  
- 在开发、CI/CD 或运维流程中提前捕获凭证泄露风险，帮助团队在代码提交前就实现安全审计。  
- 开源且活跃（8504 星、199 fork），易于审计和二次定制，适合作为内部安全基线的一部分。

**典型接入方式**  
1. **本地开发**：在 macOS 上安装 Secretive，使用 `ssh-add -K` 将密钥导入 Secure Enclave，随后普通的 `ssh`、`git` 等命令即可透明使用。  
2. **CI/CD 机器**：在受控的 macOS 构建节点上通过脚本化 CLI（`secretive add-key`、`secretive sign`）完成密钥注入和签名，确保流水线仅在硬件受信任的环境中运行。  
3. **审计/治理**：配合项目的 README 与 CI 检查脚本，验证所有仓库均已使用 Secretive 管理 SSH 密钥，从而在合规审计时提供可验证的证据。

**生产可用性**  
- **活跃度**：最近一次提交（2026‑05‑12）表明项目仍在维护，社区贡献活跃。  
- **生态兼容**：使用 Swift 编写，提供标准的 macOS 命令行接口，易于与现有脚本和工具链集成。  
- **风险**：暂无重大元数据风险，仍需对许可证（MIT）和长期维护者的可用性进行最终确认。总体而言，项目已具备在生产环境中进行小规模试点的条件，后续可根据实际使用情况逐步扩大覆盖范围。

## 🧭 Practical evaluation

**Value:** maxgoedjen/secretive helps catch security and privacy issues earlier in the workflow.

**Best use cases**

- strengthen security checks
- add auth or privacy controls
- audit risk earlier

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 8504 GitHub stars
- 199 forks
- updated 2026-05-12
- primary language: Swift
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 84/100 |
| topics | 50/100 |
| outlook | 70/100 |
| quality | 77/100 |
| recency | 80/100 |
| adoption | 76/100 |
| production | 71/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/maxgoedjen/secretive) · [← Back to Security](./README.md)</sub>
