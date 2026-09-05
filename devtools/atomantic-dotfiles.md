# atomantic/dotfiles

[![Stars](https://img.shields.io/github/stars/atomantic/dotfiles?style=flat-square&color=yellow)](https://github.com/atomantic/dotfiles/stargazers) [![Forks](https://img.shields.io/github/forks/atomantic/dotfiles?style=flat-square&color=blue)](https://github.com/atomantic/dotfiles/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> 🖥️ Automated Configuration, Preferences and Software Installation for macOS

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.4k |
| 🍴 **Forks** | 430 |
| 💻 **Language** | Shell |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`configuration` `developer-tools` `dotfiles` `iterm2` `machine` `macos`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief summary**  
atomantic/dotfiles is an open‑source collection of shell scripts that automate macOS configuration, preferences, and software installation. With over 1 300 ⭐ on GitHub, it lets engineers spin up a fully provisioned development environment in minutes, cutting down repetitive setup work.

**Value**  
The repo bundles common macOS tweaks, Homebrew package installs, and IDE settings, so developers can stop manually configuring new machines and focus on coding and code review. By codifying the environment, teams gain reproducible setups, faster onboarding, and more consistent CI feedback.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo on a single developer workstation, run the `setup.sh` (or the README‑documented entry point) and verify that the expected tools and preferences are applied.  
2. **Iterate** – Add any organization‑specific tools or customizations to a fork, and keep the changes version‑controlled.  
3. **Pilot** – Deploy the fork to a small group of engineers (e.g., a new‑joiner cohort) and collect feedback on missing steps or conflicts.  
4. **Scale** – Integrate the script into your onboarding pipeline (e.g., as a step in a CI/CD job or a bootstrap script for new VMs) and document the process in your internal README.

**Production readiness**  
The project is **medium‑ready**: it is actively maintained (last commit 2026‑06‑24) and widely used, but the integration flow isn’t fully documented and may require tailoring to your toolchain. Before promoting it to production you should:  
* audit the external dependencies (Homebrew taps, macOS settings) for security and licensing,  
* lock versions of critical packages,  
* add automated tests or validation steps to catch breaking changes, and  
* establish a maintenance owner to keep the fork up‑to‑date with upstream changes.  

With those checks in place, atomantic/dotfiles is a solid foundation for internal prototypes and can be hardened for production‑grade developer workstations.

### Русский

**atomantic/dotfiles** — набор скриптов на Shell, который автоматизирует настройку macOS: конфигурацию среды, предпочтения и установку необходимого ПО, позволяя инженерам сократить время на подготовку рабочего места и ускорить циклы разработки и ревью. Типичное внедрение начинается с небольшого proof‑of‑concept: запуск скриптов в отдельном репозитории, проверка README и адаптация под собственные инструменты, после чего можно масштабировать на всех разработчиков команды. Проект имеет средний уровень готовности к production — подходит для прототипов и внутренних воркфлоу, но требует проверки зависимостей и планов поддержки перед широким использованием.

### 中文

**项目简介（2‑3 句）**  
atomantic/dotfiles 是一套面向 macOS 的自动化配置、偏好设置与软件安装脚本，使用 Shell 编写，可一键为新机器搭建完整的开发环境。它通过统一的 dotfiles 与 Brew、MAS 等包管理器，实现工程师在本地机器上的环境一致性和快速启动。

**价值**  
- **节省时间**：一次执行即可完成系统偏好、终端、编辑器、Git、语言工具等数十项配置，避免手动逐项设置。  
- **提升一致性**：所有团队成员使用相同的配置文件，减少“在我机器上可以工作”的问题。  
- **加速 CI 反馈**：本地环境与 CI 环境保持同步，能够更快复现和排查构建/测试失败。

**典型接入方式**  
1. **阅读并 Fork/Clone 项目**：先检查 README，确认所需的 macOS 版本和依赖（Homebrew、MAS 等）。  
2. **执行安装脚本**：在新机器上运行 `./install.sh`（或项目提供的入口脚本），脚本会自动：  
   - 安装 Homebrew、MAS 并根据 `Brewfile`、`MASfile` 拉取软件；  
   - 链接或复制 `.zshrc`、`.gitconfig`、`.vimrc` 等配置文件；  
   - 设置系统偏好（Dock、键盘、显示等）。  
3. **定制化**：在 Fork 后可通过修改 `dotfiles/` 目录下的各个文件或添加自定义脚本，满足团队或个人的特殊需求。  
4. **CI/脚本化使用**：将安装脚本写入 CI 镜像构建或 Dockerfile 中，实现“代码即环境”。

**生产可用性**  
- **成熟度**：已有 1.3k+ 星、430+ Fork，最近一次更新在 2026‑06‑24，活跃度较高。  
- **适用场景**：非常适合原型开发、内部研发环境或新成员入职的快速搭建；在生产环境使用前，需要：  
  - **依赖审计**：确认 Brewfile、MASfile 中的软件版本符合公司安全合规要求。  
  - **维护计划**：定期同步上游更新，避免脚本因 macOS 系统升级而失效。  
  - **小范围验证**：先在几台机器或一个小团队做 POC，评估安装时长、冲突风险以及后续维护成本。  
- **综合评估**：在完成上述检查后，可视为 **Medium** 级别的生产可用方案，适合作为内部工作流的基础设施；若需在大规模或高安全性环境中使用，建议进一步封装为内部镜像或通过配置管理工具（如 Ansible、Chef）进行统一管理。

## 🧭 Practical evaluation

**Value:** atomantic/dotfiles helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1363 GitHub stars
- 430 forks
- updated 2026-06-24
- primary language: Shell
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 66/100 |
| stars | 67/100 |
| topics | 75/100 |
| outlook | 74/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 66/100 |
| production | 68/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/atomantic/dotfiles) · [← Back to DevTools](./README.md)</sub>
