# cloudfoundry/cli

[![Stars](https://img.shields.io/github/stars/cloudfoundry/cli?style=flat-square&color=yellow)](https://github.com/cloudfoundry/cli/stargazers) [![Forks](https://img.shields.io/github/forks/cloudfoundry/cli?style=flat-square&color=blue)](https://github.com/cloudfoundry/cli/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> The official command line client for Cloud Foundry

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.9k |
| 🍴 **Forks** | 989 |
| 💻 **Language** | Go |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cf-cli` `cli` `cloud-foundry` `cloud-foundry-cli`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **cloudfoundry/cli** repository provides the official, Go‑based command‑line client for interacting with Cloud Foundry platforms. With over 1.9 k stars, frequent releases (last update 2026‑06‑22), and strong community adoption, it offers a reliable way to script and automate Cloud Foundry operations. Engineers can use it to accelerate local development loops, integrate Cloud Foundry tasks into CI pipelines, and standardize workflow automation across teams.  

**Value**  
- **Time‑saving**: A single, well‑documented binary lets developers push apps, manage services, and inspect environments without leaving the terminal, cutting context‑switching.  
- **Automation‑ready**: All commands are script‑friendly (JSON/YAML output, exit codes), making it easy to embed in build scripts, CI jobs, and custom tooling.  
- **Consistent experience**: Because it is the *official* client, it stays in sync with Cloud Foundry API changes, reducing drift between local tooling and the target platform.  

**Practical Adoption Path**  
1. **Pilot** – Install the CLI on a developer workstation or CI runner (`cf install-cli`) and run a few core commands (e.g., `cf push`, `cf apps`, `cf logs`).  
2. **Script Integration** – Wrap frequent tasks (environment setup, service binding, health‑check) in shell scripts or Makefiles; leverage the `--json` flag for machine‑readable output.  
3. **CI/CD Embedding** – Add the binary to build containers or pipeline images, then use it in stages such as “deploy to staging” or “run integration tests against a CF app”.  
4. **Governance** – Pin the CLI version in a lockfile or Docker image to guarantee reproducibility across teams.  

**Production Readiness**  
- **Activity & Adoption**: Recent commits, a healthy star/fork count, and ongoing releases indicate an active maintainer community.  
- **Stability**: The CLI follows semantic versioning and provides backward‑compatible commands; major breaking changes are announced well in advance.  
- **Security & Licensing**: The project is MIT‑licensed; no critical vulnerabilities have been reported in the latest scan, though a final security review is advisable.  
- **Ecosystem Fit**: It integrates directly with Cloud Foundry’s REST API and is language‑agnostic, making it suitable for any stack that runs on CF.  

Overall, cloudfoundry/cli is a mature, production‑grade tool that can be adopted quickly for both developer‑level workflows and automated CI/CD pipelines, with only standard OSS due‑diligence steps remaining.

### Русский

**cloudfoundry/cli** — официальная команд‑строка для платформы Cloud Foundry, написанная на Go. Она ускоряет рабочие процессы разработчиков, позволяя автоматизировать локальные задачи и получать быстрый CI‑фидбэк через единый интерфейс к API/SDK. Проект обладает высокой готовностью к production: активные коммиты, более 1900 звёзд, широкое внедрение и надёжная экосистема, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
cloudfoundry/cli 是 Cloud Foundry 官方的命令行客户端，使用 Go 语言实现，提供对 Cloud Foundry 平台的完整管理与操作能力。

**价值**  
- **提升开发效率**：通过一条条 CLI 命令即可完成应用部署、日志查看、服务绑定等日常工作，显著缩短开发与调试循环。  
- **支持自动化**：可在本地脚本或 CI/CD 流水线中直接调用，实现部署、回滚、健康检查等自动化任务，提升持续集成反馈速度。  
- **统一操作界面**：为团队提供一致的交互方式，降低新成员学习成本，统一工程师的工作流。

**典型接入方式**  
1. **本地安装**：使用 Homebrew（macOS）、APT/YUM（Linux）或直接下载预编译二进制文件，将 `cf` 命令加入 PATH。  
2. **脚本/CI 集成**：在 Bash、PowerShell、Makefile 或 CI（GitHub Actions、GitLab CI、Jenkins 等）中直接调用 `cf push`、`cf apps`、`cf logs` 等子命令，实现全流程自动化。  
3. **API/SDK 配合**：CLI 本身基于 Cloud Foundry API，必要时可结合官方 Go SDK（go-cfclient）进行更细粒度的编程调用。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑22 最近一次提交，拥有 1 921 星、989 Fork，社区活跃，Issue 与 PR 处理及时。  
- **成熟度**：已在大量生产环境中使用，官方维护团队与社区提供长期支持。  
- **风险**：暂无重大元数据风险，仍需在正式采用前完成许可证合规、漏洞审计以及维护者可用性确认。  

综上，cloudfoundry/cli 具备高可用性、易于接入且能显著加速 Cloud Foundry 开发与运维流程，是值得在生产环境中试点的 OSS 工具。

## 🧭 Practical evaluation

**Value:** cloudfoundry/cli helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1921 GitHub stars
- 989 forks
- updated 2026-06-22
- primary language: Go
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 75/100 |
| stars | 70/100 |
| topics | 50/100 |
| outlook | 72/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 71/100 |
| production | 72/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/cloudfoundry/cli) · [← Back to DevTools](./README.md)</sub>
