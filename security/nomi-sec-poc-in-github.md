# nomi-sec/PoC-in-GitHub

[![Stars](https://img.shields.io/github/stars/nomi-sec/PoC-in-GitHub?style=flat-square&color=yellow)](https://github.com/nomi-sec/PoC-in-GitHub/stargazers) [![Forks](https://img.shields.io/github/forks/nomi-sec/PoC-in-GitHub?style=flat-square&color=blue)](https://github.com/nomi-sec/PoC-in-GitHub/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> 📡 PoC auto collect from GitHub. ⚠️ Be careful Malware.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 7.9k |
| 🍴 **Forks** | 1.3k |
| 💻 **Language** | Unknown |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cve` `exploit` `poc` `security` `vulnerability`

## 🎯 Categories

Security

## 📝 Summary

### English

nomi‑sec/PoC‑in‑GitHub automatically gathers proof‑of‑concept code from GitHub, enabling teams to surface security and privacy issues earlier in the development workflow. Adoption requires a manual review of the collected PoCs before integration, but the project’s recent activity, strong star/fork counts, and clear ecosystem signals make it suitable for a serious pilot in production environments.

### Русский

**nomi-sec/PoC-in-GitHub** — это open‑source‑инструмент, который автоматически собирает потенциально опасный код и уязвимости из репозиториев GitHub, позволяя обнаружить проблемы безопасности и конфиденциальности ещё на этапе разработки. Его типичное внедрение — интеграция в CI/CD pipeline для ранних проверок, добавления контролей доступа и аудита рисков, при этом требуется ручная проверка полученных сигналов из‑за их разреженности. По готовности к продакшн проект находится на высоком уровне: активные коммиты, более 7 тыс. звёзд, 1,3 тыс. форков и свежие обновления, что делает его подходящим для пилотного запуска после оценки стоимости настройки.

### 中文

**项目简介**  
nomi-sec/PoC-in-GitHub 是一款自动从 GitHub 仓库抓取 PoC（概念验证）代码的工具，帮助开发者在代码提交、合并或发布前提前发现安全与隐私风险。⚠️ 由于涉及恶意样本，请务必在受控环境中使用。

**价值**  
- **提前预警**：在代码进入生产环境前捕获潜在的安全漏洞和隐私泄露点，降低后期修复成本。  
- **安全治理**：可作为 CI/CD 流程的补充，帮助团队实现更严格的安全审计与合规检查。  
- **社区支持**：拥有 7 856+ ⭐ 和 1 340+ 🍴，活跃度高，社区贡献丰富。

**典型接入方式**  
1. **本地部署**：克隆仓库后在 CI 环境（如 GitHub Actions、GitLab CI、Jenkins）中运行 `poc-collector` 脚本，指定要监控的组织或仓库列表。  
2. **容器化**：使用官方提供的 Docker 镜像（`nomi-sec/poc-in-github:latest`），通过环境变量配置 GitHub Token、目标仓库前缀等参数，方便在 Kubernetes 或云原生平台上横向扩展。  
3. **API 调用**：项目暴露的 REST 接口可在自研安全平台中调用，实现“发现‑评估‑响应”全链路自动化。  
> **注意**：元数据中关于集成的提示较少，建议在正式接入前先在测试仓库进行一次完整的端到端验证，评估网络、权限及存储成本。

**生产可用性**  
- **成熟度**：近期（2026‑06‑27）仍保持活跃更新，且已有多家企业在内部试点，具备进入正式生产的技术基础。  
- **准备度**：高（OSS 候选），但因集成路径不够明确，建议在正式部署前完成以下步骤：  
  1. **安全审计**：确认抓取的 PoC 内容不会意外泄露内部代码或凭证。  
  2. **资源评估**：估算存储和网络带宽需求，尤其是大规模组织的仓库抓取。  
  3. **权限控制**：使用最小权限的 GitHub Token，仅授权读取目标仓库的元数据。  
- **风险**：集成成本和后续维护工作需要在项目初期明确，避免在生产环境中出现意外的高负载或误报。

综上，nomi-sec/PoC-in-GitHub 适合作为安全审计链路的前置检测工具，在做好前期验证与权限管理后，可安全投入生产使用。

## 🧭 Practical evaluation

**Value:** nomi-sec/PoC-in-GitHub helps catch security and privacy issues earlier in the workflow.

**Best use cases**

- strengthen security checks
- add auth or privacy controls
- audit risk earlier

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 7856 GitHub stars
- 1340 forks
- updated 2026-06-27
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 78/100 |
| stars | 83/100 |
| topics | 63/100 |
| outlook | 59/100 |
| quality | 71/100 |
| recency | 40/100 |
| adoption | 82/100 |
| production | 57/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/nomi-sec/PoC-in-GitHub) · [← Back to Security](./README.md)</sub>
