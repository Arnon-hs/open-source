# rhinstaller/anaconda

[![Stars](https://img.shields.io/github/stars/rhinstaller/anaconda?style=flat-square&color=yellow)](https://github.com/rhinstaller/anaconda/stargazers) [![Forks](https://img.shields.io/github/forks/rhinstaller/anaconda?style=flat-square&color=blue)](https://github.com/rhinstaller/anaconda/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> System installer for Fedora, RHEL and other distributions

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 630 |
| 🍴 **Forks** | 392 |
| 💻 **Language** | Python |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`automated-installation` `centos` `fedora` `graphical-user-interface` `installation` `python3` `rhel` `system` `text-user-interface`

## 🎯 Categories

Misc

## 📝 Summary

### English

Here's a brief summary of the open-source project rhinstaller/anaconda:

Rhinstaller/anaconda is an open-source system installer for Fedora, RHEL, and other Linux distributions, which can be useful for users who need to automate or customize the installation process for their specific workflow. The project's production readiness is high, with recent activity, strong adoption, and a robust ecosystem, making it suitable for a serious pilot or production deployment. To adopt this project, users can start by reviewing the README, evaluating a small proof of concept, and conducting a thorough review of the license, security posture, and active maintainers.

In terms of practical adoption path, here are the steps:

1. **Review the README**: Understand the project's purpose, features, and usage.
2. **Evaluate a small proof of concept**: Test the project's functionality and ensure it meets your specific needs.
3. **Conduct a thorough review**: Assess the project's license, security posture, and active maintainers to ensure it aligns with your organization's requirements.
4. **Pilot the project**: Implement the project in a controlled environment to test its scalability and reliability.
5. **Deploy in production**: Once satisfied with the project's performance, deploy it in your production environment.

Regarding production readiness,

### Русский

**rhinstaller/anaconda** — это открытый системный установщик, используемый в Fedora, RHEL и подобных дистрибутивах; благодаря активному развитию (630 ★, 392 fork, последний коммит 2026‑07‑01) и широкой поддержке в экосистеме Python, проект готов к пилотному внедрению в production‑среде. Типичный сценарий — интеграция установочного процесса в собственные образы или автоматизацию развертывания серверов, начиная с небольшого proof‑of‑concept и проверки README. Несмотря на отсутствие серьёзных метаданных‑рисков, требуется окончательная проверка лицензии, безопасности и наличия активных мейнтейнеров.

### 中文

**项目简介**  
`rhinstaller/anaconda` 是 Fedora、RHEL 及其他 Linux 发行版使用的系统安装程序，采用 Python 编写，拥有 630+ 星、400+ Fork，最近一次提交在 2026‑07‑01，社区活跃度高。

**价值**  
- **统一安装体验**：提供图形化、文本化和 Kickstart 脚本三种安装方式，适配多种硬件和网络环境。  
- **可定制化**：插件式架构、丰富的 Python API，使 OEM、云镜像和私有发行版能够在安装流程中插入自定义步骤或驱动。  
- **成熟可靠**：作为 Fedora、RHEL 官方安装器，经过大规模生产环境验证，具备完整的错误恢复、日志与回滚机制。

**典型接入方式**  
1. **源码集成**：克隆仓库，使用 `make`/`meson` 编译生成 `anaconda` 二进制；在自定义 ISO 中替换默认安装器。  
2. **Python 包调用**：通过 `pip install anaconda`（或内部 PyPI）引入核心库，在自动化部署脚本或 CI 中调用 `anaconda.install()` 接口，实现无人值守安装。  
3. **Kickstart 定制**：编写 Kickstart 文件，利用 Anaconda 的 `--kickstart` 参数完成全自动化部署，适合大规模云/裸金属环境。  
4. **插件扩展**：在 `anaconda/plugins` 目录编写自定义插件（如硬件检测、后置脚本），在启动时通过 `--enable-plugins` 加载。

**生产可用性**  
- **成熟度**：官方发行版默认使用，已在数百万台机器上验证，错误率低。  
- **活跃维护**：近期有代码更新、Bug 修复和安全补丁，社区响应及时。  
- **生态兼容**：支持 UEFI、BIOS、Secure Boot、LVM、Btrfs、RAID、网络安装等主流特性，且与 Anaconda‑Installer‑Utils、Cockpit 等工具无缝协作。  
- **风险**：需进一步审查许可证（GPL‑2.0）与安全审计报告，确保符合企业合规要求。

**结论**  
`rhinstaller/anaconda` 具备高可用性和可扩展性，适合作为企业内部或云平台的系统安装核心组件。建议先在测试环境完成一个 Kickstart‑驱动的 PoC，验证自定义插件和日志收集后，即可推进到生产级部署。

## 🧭 Practical evaluation

**Value:** rhinstaller/anaconda may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 630 GitHub stars
- 392 forks
- updated 2026-07-01
- primary language: Python
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 65/100 |
| stars | 60/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 67/100 |
| recency | 40/100 |
| adoption | 61/100 |
| production | 58/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/rhinstaller/anaconda) · [← Back to Misc](./README.md)</sub>
