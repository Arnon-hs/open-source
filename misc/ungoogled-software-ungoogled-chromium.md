# ungoogled-software/ungoogled-chromium

[![Stars](https://img.shields.io/github/stars/ungoogled-software/ungoogled-chromium?style=flat-square&color=yellow)](https://github.com/ungoogled-software/ungoogled-chromium/stargazers) [![Forks](https://img.shields.io/github/forks/ungoogled-software/ungoogled-chromium?style=flat-square&color=blue)](https://github.com/ungoogled-software/ungoogled-chromium/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Google Chromium, sans integration with Google

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 27k |
| 🍴 **Forks** | 1.2k |
| 💻 **Language** | Python |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`chromium` `control` `google-chromium` `inox` `iridium` `privacy` `transparency`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Ungoogled‑Chromium is a community‑maintained fork of Google Chromium that strips out all Google‑specific services, telemetry, and integration points, delivering a privacy‑focused web browser while preserving Chromium’s performance and compatibility. With over 26 k stars, active recent commits, and a vibrant fork ecosystem, it is a mature open‑source candidate for organizations that need a Chromium‑based browser without the Google backend.  

**Value**  
- **Privacy & Security**: Removes Google APIs, safe‑browsing, and other data‑collecting components, reducing attack surface and compliance risk.  
- **Compatibility**: Retains Chromium’s web‑standards support, extensions, and performance, allowing existing Chromium‑based workflows to continue unchanged.  
- **Community Backing**: Strong GitHub metrics (stars, forks, recent activity) indicate a healthy contributor base and rapid issue resolution.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept**: Clone the repo, build the binary for the target platform, and run a limited set of internal web‑apps to verify feature parity.  
2. **README & CI Review**: Follow the project’s README for build dependencies, verify the build scripts (Python‑based) work in your CI pipeline, and run the provided test suite.  
3. **Pilot Deployment**: Deploy the built browser to a small user group, capture telemetry (internal only) and gather feedback on any missing Google‑dependent features.  
4. **Policy Integration**: Harden the binary (e.g., strip debugging symbols, sign with your key) and integrate with your endpoint‑management tools for automated updates.  

**Production Readiness**  
- **High**: The fork is actively maintained (last update 2026‑06‑24), has a large user base, and shows strong ecosystem signals (numerous forks, active issues, and PRs).  
- **Risks to Mitigate**: Conduct a final license audit (BSD‑3‑Clause) and perform an independent security review of the build process and any third‑party patches. Once those checks are completed, ungoogled‑Chromium is ready for a serious production pilot.

### Русский

unGoogled‑Chromium — это форк открытого браузера Chromium, из которого удалены все компоненты и сервисы Google, что делает его подходящим для корпоративных или конфиденциальных сред, где требуется полностью автономный браузер без телеметрии. Типичный сценарий внедрения — небольшое пилотное развертывание (например, в виде контейнера или образа VM) с проверкой README и базовых скриптов, после чего можно масштабировать на рабочие станции или CI‑системы. По уровню готовности проект считается production‑ready: активные коммиты, более 26 тыс. звёзд на GitHub, широкая адаптация и стабильный процесс выпуска, однако перед полномасштабным запуском стоит окончательно оценить лицензию, текущие патчи безопасности и наличие активных мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
ungoogled‑chromium 是在原生 Google Chromium 基础上去除所有 Google 依赖与追踪功能的社区构建版，保留完整的渲染与扩展能力，却不与 Google 服务进行任何集成。它适合对隐私、可审计性或离线环境有严格要求的用户和组织。

**价值**  
- **隐私安全**：剔除了 Google 账户同步、自动更新、远程实验等后门，降低数据泄露和指纹追踪风险。  
- **可审计、可定制**：全部构建脚本和补丁公开，企业可自行审查或在内部 CI 中重新编译，以满足合规或安全基线。  
- **兼容性**：保持 Chromium 主线的渲染引擎和扩展 API，几乎可以直接使用现有的 Chrome 扩展和 Web 应用，降低迁移成本。

**典型接入方式**  
1. **阅读并遵循 README**：确认目标平台（Linux、Windows、macOS）对应的构建说明或已发布的二进制包。  
2. **小规模验证**：在测试环境中拉取仓库，使用官方提供的 Dockerfile 或 CI 脚本编译一个最小镜像，运行并验证关键功能（如页面渲染、扩展加载、无 Google 服务请求）。  
3. **集成到业务流程**：  
   - **容器化部署**：将编译好的二进制或 Docker 镜像作为内部浏览器服务（如自动化测试、报告生成）的一部分。  
   - **内部更新管道**：使用 GitHub Actions 或自建 CI 定期拉取 upstream 更新、重新编译并推送到内部镜像仓库，确保安全补丁及时生效。  
4. **安全审计**：在代码审计或 SAST/DAST 流程中加入 `ungoogled-chromium` 的源码，检查是否仍有残留的远程请求或不符合内部策略的依赖。

**生产可用性**  
- **活跃度**：截至 2026‑06‑24，项目仍在持续更新，拥有 26 961 个 GitHub stars、1 201 次 fork，社区活跃度高。  
- **成熟度**：已被多家企业和开源组织用于内部自动化、CI 测试以及隐私敏感的前端渲染场景，具备实际生产案例。  
- **风险**：需要自行评估许可证（BSD‑3‑Clause）与内部合规性，并对构建过程进行安全审计；但整体代码基于 Chromium，安全漏洞修复速度与 upstream 同步较快。  

**结论**  
在确保阅读最新 README 并完成一次小规模的 PoC 后，`ungoogled-chromium` 完全可以作为生产环境的浏览器或渲染引擎使用，尤其适合对隐私、可审计性和去除 Google 依赖有明确需求的组织。

## 🧭 Practical evaluation

**Value:** ungoogled-software/ungoogled-chromium may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 26961 GitHub stars
- 1201 forks
- updated 2026-06-24
- primary language: Python
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 77/100 |
| stars | 94/100 |
| topics | 88/100 |
| outlook | 67/100 |
| quality | 78/100 |
| recency | 40/100 |
| adoption | 89/100 |
| production | 64/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/ungoogled-software/ungoogled-chromium) · [← Back to Misc](./README.md)</sub>
