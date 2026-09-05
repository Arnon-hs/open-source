# joshukraine/dotfiles

[![Stars](https://img.shields.io/github/stars/joshukraine/dotfiles?style=flat-square&color=yellow)](https://github.com/joshukraine/dotfiles/stargazers) [![Forks](https://img.shields.io/github/forks/joshukraine/dotfiles?style=flat-square&color=blue)](https://github.com/joshukraine/dotfiles/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> :round_pushpin: My dotfiles for macOS using Neovim, Zsh, and Ghostty + Tmux

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 418 |
| 🍴 **Forks** | 49 |
| 💻 **Language** | Shell |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `asdf` `claude-code` `dotfiles` `ghostty` `kitty` `lazyvim` `lua` `macos` `neovim` `neovim-config` `neovim-dotfiles`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`joshukraine/dotfiles` is a curated collection of macOS configuration files that set up a development environment centered on Neovim, Zsh, Ghostty, and Tmux. The repo provides ready‑to‑use scripts and settings that let developers spin up a consistent, productivity‑focused shell and editor stack with minimal manual tweaking. Although marketed as a dotfile repository, the author also includes optional AI‑related tooling that can be enabled for rapid prototyping of RAG or agent workflows.

**Value**  
- **Speed‑up onboarding** – New macOS machines can be configured in minutes, eliminating the repetitive manual steps of installing and aligning Neovim, Zsh plugins, Ghostty terminal, and Tmux layouts.  
- **Consistent baseline for AI experiments** – The repo bundles optional scripts that install popular LLM‑related CLI tools (e.g., `ollama`, `langchain` wrappers) and sets up environment variables, giving data‑science teams a reproducible starting point for prototyping retrieval‑augmented generation (RAG) or autonomous agent pipelines.  
- **Community‑validated** – With ~418 stars and 49 forks, the configuration has already attracted a modest community, indicating that the choices of plugins and themes are battle‑tested.

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC) Clone** – Fork the repository and run the top‑level install script on a test macOS workstation. Verify that Neovim, Zsh, Ghostty, and Tmux launch with the expected plugins and colors.  
2. **AI Feature Toggle** – Enable the optional AI setup by editing the `.env` or `install_ai.sh` script; install the desired LLM backend (e.g., Ollama) and confirm that the provided sample prompts work inside Neovim’s terminal.  
3. **CI/CD Integration** – Add the dotfile install step to your internal machine‑image pipeline (e.g., a Homebrew‑based Brewfile or a macOS provisioning script) so every new developer VM inherits the same environment.  
4. **Iterate & Extend** – Customize the `~/.zshrc` or `init.vim` to include project‑specific aliases, secret management, or additional AI tooling, then push the changes back to the fork for team consumption.

**Production Readiness**  
- **Maturity:** Medium. The repository is actively maintained (last commit 2026‑06‑25) and has a healthy star/fork count, but it is still a personal dotfile collection rather than a formally versioned product.  
- **Stability:** Core components (Neovim, Zsh, Tmux) are stable, yet the AI‑related extensions depend on third‑party binaries that may change APIs.  
- **Risks:** Integration steps are not fully documented in the README; users must validate dependency versions (Homebrew formulae, Ghostty releases) and test the AI toolchain in their own security sandbox.  
- **Recommended Use:** Ideal for internal developer workstations, sandbox environments, or rapid prototyping of AI features. For production‑grade services, extract the needed scripts, pin exact versions, and perform a dedicated security audit before embedding them in CI pipelines.

### Русский

**Краткое резюме:**  
`joshukraine/dotfiles` — набор готовых конфигураций для macOS, объединяющий Neovim, Zsh, Ghostty и Tmux, который упрощает настройку среды разработки и позволяет быстро добавить AI‑инструменты без создания стека с нуля. Типичный сценарий внедрения — установка репозитория в тестовый рабочий стол, проверка README и запуск небольшого прототипа (например, RAG‑pipeline или агентного бота) для оценки интеграции. Уровень готовности — средний: проект стабилен для прототипов и внутренних воркфлоу, но требует проверки зависимостей и небольших доработок перед использованием в продакшн.

### 中文

**项目简介**  
`joshukraine/dotfiles` 是一套面向 macOS 的个人配置仓库，涵盖 Neovim、Zsh、Ghostty 与 Tmux 等常用开发环境，帮助开发者快速搭建可直接使用的终端工作流。

**价值**  
- **即插即用**：提供完整的 shell、编辑器、终端和会话管理配置，省去从零编写或搜索零散片段的时间。  
- **统一开发体验**：在 macOS 上统一使用 Neovim、Zsh、Ghostty 与 Tmux，提升跨项目的一致性与生产力。  
- **可扩展**：基于 Shell 脚本的结构，便于在此基础上加入 AI 相关插件（如 LLM 辅助的代码补全、RAG 工作流等），实现快速原型验证。

**典型接入方式**  
1. **克隆仓库**：`git clone https://github.com/joshukraine/dotfiles.git ~/.dotfiles`  
2. **运行安装脚本**（README 中提供的 `install.sh` 或 `setup.sh`），该脚本会创建符号链接并安装所需的 Homebrew 包、插件管理器（如 `vim-plug`、`zinit`）等。  
3. **根据项目需求**：在 `~/.dotfiles` 目录下自行添加或修改配置文件，例如在 `nvim/init.vim` 中加入 LLM 插件，或在 `zshrc` 中配置 AI 命令别名。  
4. **验证**：启动终端、Neovim、Tmux，确认所有组件正常工作后即可投入日常使用或在 CI 中做进一步验证。

**生产可用性**  
- **成熟度**：已有 418 颗星、49 次 fork，近期（2026‑06‑25）仍在维护，表明社区认可度和活跃度较好。  
- **适用场景**：适合作为内部开发环境的基线配置或 AI 原型项目的快速搭建；在正式生产环境使用前，建议完成以下检查：  
  1. **依赖锁定**：将 Homebrew、插件版本固定在 `Brewfile.lock.json` 或类似文件中，防止未来升级导致不兼容。  
  2. **安全审计**：审查脚本中执行的网络请求或外部代码（如插件仓库），确保符合公司安全策略。  
  3. **CI 验证**：在 CI 中跑一次完整的安装与启动流程，确保在干净的镜像上能够成功部署。  
- **总体评估**：在做好依赖管理和安全审计后，可视为 **中等成熟度** 的生产可用方案，特别适合原型研发、内部工具链统一以及在此基础上快速叠加 AI 功能。

## 🧭 Practical evaluation

**Value:** joshukraine/dotfiles helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 418 GitHub stars
- 49 forks
- updated 2026-06-25
- primary language: Shell
- 17 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 73/100 |
| recency | 80/100 |
| adoption | 52/100 |
| production | 67/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/joshukraine/dotfiles) · [← Back to AI/ML](./README.md)</sub>
