# spaceship-prompt/spaceship-prompt

[![Stars](https://img.shields.io/github/stars/spaceship-prompt/spaceship-prompt?style=flat-square&color=yellow)](https://github.com/spaceship-prompt/spaceship-prompt/stargazers) [![Forks](https://img.shields.io/github/forks/spaceship-prompt/spaceship-prompt?style=flat-square&color=blue)](https://github.com/spaceship-prompt/spaceship-prompt/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> 🚀✨ Minimalistic, powerful and extremely customizable Zsh prompt

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 20.5k |
| 🍴 **Forks** | 969 |
| 💻 **Language** | Shell |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`oh-my-zsh` `prompt` `shell` `shell-prompt` `shell-theme` `spaceship` `terminal` `zsh` `zsh-theme` `zsh-users`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Spaceship Prompt is a minimalistic yet feature‑rich Zsh prompt that can be heavily customized through modules, colors, and async status updates. With over 20 k GitHub stars, frequent releases, and a vibrant community, it offers a polished, ready‑to‑use shell experience for developers who want a modern, informative prompt without writing their own from scratch.  

**Value**  
- **Productivity boost** – real‑time Git, Docker, Node, and many other status indicators are displayed directly in the prompt, reducing context‑switching.  
- **Extensibility** – more than 30 built‑in modules can be toggled or extended with custom scripts, fitting almost any workflow.  
- **Consistency** – a single, well‑maintained codebase ensures the prompt looks and behaves the same across machines, easing onboarding for teams that standardize on Zsh.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Add the repository as a submodule or install via the recommended `npm`/`brew` method on a test workstation.  
2. **Readme validation** – Follow the quick‑start section to enable the prompt, then experiment with a few modules relevant to your stack (e.g., `git`, `node`, `k8s`).  
3. **Customization** – Create a local `.zshrc` snippet that selects the needed modules, sets preferred colors, and disables unwanted defaults.  
4. **Team rollout** – Package the configuration in a shared dotfiles repo or a configuration management tool (Ansible, Chef, etc.) and document the install steps for new developers.

**Production Readiness**  
- **Activity & maintenance** – Updated as of 2026‑06‑24 with regular releases and active issue triage.  
- **Adoption** – 20 524 stars, 969 forks, and numerous third‑party tutorials indicate broad real‑world use.  
- **Stability** – Core functionality is mature; breaking changes are rare and clearly documented.  
- **Risk mitigation** – The only notable risk is the initial learning curve for the module system; a small pilot (as outlined above) will surface any setup costs before wider deployment.  

Overall, Spaceship Prompt is production‑ready for teams that already use Zsh and want a powerful, maintainable prompt with minimal integration effort.

### Русский

**Spaceship Prompt** — это минималистичный, но при этом мощный и полностью настраиваемый Zsh‑prompt, который уже собрал более 20 тыс. ⭐ на GitHub, активно поддерживается (обновления — июнь 2026) и имеет широкое сообщество (≈ 1 к fork‑ов). Его типичное внедрение — небольшая проба: добавить репозиторий в `.zshrc`, скопировать базовую конфигурацию из README и постепенно адаптировать темы, сегменты и плагины под свои нужды; такой подход позволяет быстро оценить совместимость с текущим workflow. По уровню готовности к production проект считается «high»: стабильные релизы, активная разработка и проверенная экосистема делают его надёжным кандидатом для серьёзных пилотных внедрений.

### 中文

**简短介绍**  
Spaceship Prompt（`spaceship-prompt/spaceship-prompt`）是一款极简却功能强大的 Zsh 主题，提供丰富的模块化信息（Git 状态、Node、Python、Docker 等）并支持高度自定义，让终端既美观又高效。  

**价值**  
- **信息一目了然**：在同一行展示项目、版本管理、容器、云服务等关键上下文，提升开发和运维的感知效率。  
- **高度可配置**：通过环境变量或插件机制自由增删模块、调整颜色、修改布局，几乎可以适配任何工作流。  
- **社区成熟**：超过 20 k 星、近 1 k Fork，活跃维护并兼容最新 Zsh、macOS、Linux 与 Windows（WSL）环境，已有大量企业和开源团队在生产中使用。  

**典型接入方式**  
1. **安装**（推荐使用插件管理器）  
   ```bash
   # 使用 Oh My Zsh
   git clone https://github.com/spaceship-prompt/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt"
   ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
   # 然后在 .zshrc 中设置
   ZSH_THEME="spaceship"
   ```  
   或者通过 Homebrew、apt、yum、asdf 等包管理器直接 `brew install spaceship-prompt`。  

2. **自定义**  
   在 `~/.zshrc` 中添加环境变量，例如：  
   ```bash
   SPACESHIP_PROMPT_ORDER=git_node_python
   SPACESHIP_GIT_BRANCH_COLOR="cyan"
   SPACESHIP_TIME_SHOW=true
   ```  
   通过 `spaceship` 官方文档可以查阅全部可配置项。  

3. **验证**  
   重新加载 Zsh（`source ~/.zshrc`）或打开新终端窗口，确认提示符已切换为 Spaceship 并显示期望模块。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑24，持续发布新版本，Issue 与 PR 响应及时。  
- **兼容性**：官方支持 Zsh ≥ 5.0，已在 macOS、Ubuntu、Debian、Fedora、Arch、Windows WSL 等多平台通过 CI 测试。  
- **风险控制**：接入成本主要在于插件管理器的选择和自定义变量的调研，建议先在非关键机器或 CI 环境做一次 “最小化模块” 的 PoC，确认无冲突后再推广到全员终端。  

综上，Spaceship Prompt 已具备成熟的社区、活跃的维护和灵活的配置能力，完全可以在生产环境中作为统一的 Zsh 提示符方案使用。

## 🧭 Practical evaluation

**Value:** spaceship-prompt/spaceship-prompt may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 20524 GitHub stars
- 969 forks
- updated 2026-06-24
- primary language: Shell
- 10 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 75/100 |
| stars | 92/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 79/100 |
| recency | 40/100 |
| adoption | 87/100 |
| production | 59/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/spaceship-prompt/spaceship-prompt) · [← Back to Misc](./README.md)</sub>
