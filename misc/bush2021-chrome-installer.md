# Bush2021/chrome_installer

[![Stars](https://img.shields.io/github/stars/Bush2021/chrome_installer?style=flat-square&color=yellow)](https://github.com/Bush2021/chrome_installer/stargazers) [![Forks](https://img.shields.io/github/forks/Bush2021/chrome_installer?style=flat-square&color=blue)](https://github.com/Bush2021/chrome_installer/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Auto-updated Google Chrome offline installers for Windows (Stable/Beta/Dev/Canary, x86/x64/ARM64) with direct links and SHA-256, via GitHub Actions

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.5k |
| 🍴 **Forks** | 113 |
| 💻 **Language** | Python |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`github-actions` `google-chrome` `offline-installer` `windows`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
Bush2021/chrome_installer automatically generates and publishes up‑to‑date offline installers for every Google Chrome channel (Stable, Beta, Dev, Canary) and architecture (x86, x64, ARM64) on GitHub. The repository supplies direct download URLs together with SHA‑256 hashes, refreshed via a GitHub Actions workflow that runs daily.

**Value**  
- Eliminates the need to manually locate, verify, and store Chrome installers for internal testing, CI pipelines, or air‑gapped environments.  
- Guarantees integrity with published SHA‑256 hashes and provides a single, version‑controlled source of truth for all Chrome builds.  
- The Python‑based tooling and GitHub‑Actions pipeline are easy to fork or extend, fitting naturally into existing DevOps workflows.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided script locally to fetch the latest installer for the required channel/architecture, and verify the hash.  
2. **Integration** – Add a step in your CI/CD pipeline (e.g., GitHub Actions, Azure Pipelines, Jenkins) that calls the script or consumes the generated JSON/URL file to download the installer during build or test stages.  
3. **Customization** – If you need a different update cadence or additional channels, fork the repo and adjust the GitHub‑Actions schedule or the Python logic; the project’s README gives clear guidance on doing so.  

**Production readiness**  
- **Activity & community**: 1,541 stars, 113 forks, last update 2026‑06‑24, and a well‑maintained Python codebase indicate strong community interest and ongoing maintenance.  
- **Reliability**: The daily GitHub‑Actions run ensures the installer list is always current; SHA‑256 hashes provide cryptographic verification.  
- **Risk considerations**: No immediate metadata or licensing red flags, but a final security audit of the Python script and verification of the repository’s license (MIT‑style) are advisable before wide deployment.  

Overall, the project is mature enough for a serious pilot in production environments, especially where automated, verifiable Chrome binaries are required.

### Русский

**Bush2021/chrome_installer** — это репозиторий, автоматически собирающий актуальные офлайн‑инсталляторы Google Chrome (Stable, Beta, Dev, Canary) для всех поддерживаемых архитектур Windows (x86, x64, ARM64) и публикующий их с прямыми ссылками и SHA‑256‑хешами через GitHub Actions. Типовой сценарий внедрения — скрипт или CI‑pipeline, который в нужный момент скачивает проверенный офлайн‑пакет из репозитория, тем самым устраняя зависимость от онлайн‑загрузок и гарантируя согласованность версии браузера в тестовых и продакшн‑окружениях. По уровню готовности проект считается почти готовым к production: активные коммиты, более 1500 звёзд, регулярные релизы и открытый Python‑код, однако перед масштабным использованием следует проверить лицензию, политику безопасности и наличие ответственного мейнтейнера.

### 中文

**项目简介**  
Bush2021/chrome_installer 自动维护 Windows 版 Google Chrome（Stable、Beta、Dev、Canary）离线安装包的最新版本，提供 x86、x64、ARM64 三种架构的直接下载链接及对应的 SHA‑256 校验值，所有文件均由 GitHub Actions 每日构建并同步更新。

**价值**  
- **可靠的离线安装源**：在没有网络或受限网络环境下，仍能快速获取官方最新的 Chrome 安装包。  
- **完整的校验信息**：每个下载链接都附带 SHA‑256，便于在内部系统中进行安全校验，防止被篡改。  
- **多渠道覆盖**：一次性提供四个渠道（Stable/Beta/Dev/Canary）和三种架构，满足不同测试、部署或内部镜像的需求。  
- **自动化更新**：基于 GitHub Actions 的每日构建，确保离线包始终与官方同步，无需手动维护脚本或镜像。

**典型接入方式**  

| 场景 | 接入步骤 | 关键点 |
|------|----------|--------|
| **CI/CD 自动化** | 1. 在流水线脚本（如 GitHub Actions、GitLab CI、Jenkins）中添加 `curl`/`wget` 下载对应渠道和架构的链接。<br>2. 使用提供的 SHA‑256 通过 `sha256sum -c` 进行校验。<br>3. 将下载的 MSI/EXE 安装到构建机器或制品库。 | 只需读取项目根目录下的 `README.md` 中的表格或直接访问 `https://github.com/Bush2021/chrome_installer/blob/main/links.json`（若有）获取最新链接。 |
| **内部镜像/私有仓库** | 1. 编写定时任务（cron）或 GitHub Action，定期（如每日）拉取最新链接并下载。<br>2. 将文件上传至内部文件服务器或制品库（Nexus、Artifactory）。 | 通过项目的 `download.py`（若提供）或自行解析 `links.json`，实现全自动同步。 |
| **安全审计/合规** | 1. 在安全审计脚本中加入 SHA‑256 校验步骤。<br>2. 将校验结果记录到审计日志。 | 项目已提供哈希值，省去手动查询官方页面的步骤。 |

**生产可用性评估**  

- **活跃度**：最近一次提交在 2026‑06‑24，星标 1541、fork 113，表明社区关注度和使用率均较高。  
- **技术成熟度**：核心实现使用 Python，代码结构简洁，依赖少，易于在各种环境中部署。  
- **安全性**：所有下载链接均指向官方 Google CDN，且项目公开提供 SHA‑256，降低供应链风险。仍建议在生产环境中加入二次签名或内部镜像的额外校验。  
- **运维成本**：只需在内部维护一个定时同步任务或在 CI 中直接拉取，无需自行维护 Chrome 版本库。  
- **风险**：需确认项目许可证（MIT/Apache 等）与贵公司合规要求匹配；另外，虽然目前维护者活跃，但仍建议在关键业务中设置 fallback（如直接访问 Google 官方下载页面）以防止突发中断。

**结论**  
Bush2021/chrome_installer 具备高可用的离线 Chrome 安装包供应能力，接入成本低，适合作为内部部署、自动化测试或受限网络环境下的 Chrome 安装源。经过一次小范围的 PoC 验证（例如在 CI 中拉取并校验一次），即可在生产环境中安全推广使用。

## 🧭 Practical evaluation

**Value:** Bush2021/chrome_installer may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1541 GitHub stars
- 113 forks
- updated 2026-06-24
- primary language: Python
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 68/100 |
| topics | 50/100 |
| outlook | 53/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 63/100 |
| production | 57/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/Bush2021/chrome_installer) · [← Back to Misc](./README.md)</sub>
