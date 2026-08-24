# ibhagwan/fzf-lua

[![Stars](https://img.shields.io/github/stars/ibhagwan/fzf-lua?style=flat-square&color=yellow)](https://github.com/ibhagwan/fzf-lua/stargazers) [![Forks](https://img.shields.io/github/forks/ibhagwan/fzf-lua?style=flat-square&color=blue)](https://github.com/ibhagwan/fzf-lua/network) [![Language](https://img.shields.io/badge/lang-Lua-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Improved fzf.vim written in lua

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.3k |
| 🍴 **Forks** | 258 |
| 💻 **Language** | Lua |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`fzf` `lua` `neovim` `neovim-plugin` `nvim` `nvim-plugin`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
`ibhagwan/fzf-lua` is a Lua‑based rewrite of the popular `fzf.vim` plugin that brings fuzzy‑finding capabilities to Neovim with a faster, more configurable core. Its high star count, recent commits, and active community make it a strong candidate for teams that already use Neovim and want a native‑Lua alternative to the original Vimscript implementation.

**Value**  
- **Performance & Extensibility**: By leveraging Lua, the plugin runs inside Neovim’s native runtime, delivering lower latency and richer extension points than the original `fzf.vim`.  
- **Unified Ecosystem**: It integrates directly with Neovim’s Lua API, allowing developers to script custom pickers, pipelines, and UI tweaks without bridging to external processes.  
- **Broad Adoption**: With >4 k stars and a growing number of forks, the project has proven useful in many personal and team configurations, providing a reliable reference for best practices.

**Practical Adoption Path**  
1. **Prototype** – Add the plugin via a plugin manager (e.g., `packer.nvim` or `lazy.nvim`) and replace existing `fzf.vim` commands with the Lua equivalents (`require('fzf-lua').files()`, etc.).  
2. **Configuration** – Use the provided Lua API to tailor keybindings, layout, and previewers to match your workflow; the README offers ready‑made snippets for common use cases (git status, buffers, grep, etc.).  
3. **Integration** – Hook the plugin into existing tooling (e.g., LSP diagnostics, Telescope fallbacks, CI scripts) by calling its functions from your own Lua modules.  
4. **Validation** – Run your test suite and performance benchmarks to confirm the expected speed gains and stability in your CI environment.

**Production Readiness**  
- **Active Maintenance**: Last commit on 2026‑07‑03, frequent releases, and responsive issue handling indicate a healthy maintainer base.  
- **Ecosystem Signals**: Strong GitHub metrics (4.3 k stars, 258 forks) and inclusion in many community dotfiles demonstrate real‑world usage.  
- **Risk Profile**: No known licensing or critical security concerns, but a final review of the MIT license and any external binary dependencies is advisable before a full production rollout.  

Overall, `fzf-lua` offers a mature, high‑performance fuzzy‑finding solution for Neovim teams ready to modernize their workflow with Lua‑native plugins.

### Русский

Резюме:

Проект ibhagwan/fzf-lua представляет собой улучшенную версию fzf.vim, написанную на языке Lua. Он может быть полезен в конкретном рабочем процессе, если README и активность проекта соответствуют его потребностям. Проект готов к внедрению в производство на высоком уровне, учитывая его недавнюю активность, широкое принятие и сильные сигналы экосистемы.

### 中文

**项目简介**

ibhagwan/fzf-lua 是一个基于 Lua 实现的 fzf.vim 的改进版本。它提供了一个高效的文件查找和过滤功能，适合用于 Vim 编辑器。

**价值**

ibhagwan/fzf-lua 的价值在于它可以提高 Vim 编辑器的文件查找和过滤效率，帮助开发者快速找到需要的文件。

**典型接入方式**

典型接入方式是通过 Vim 编辑器的插件系统，将 ibhagwan/fzf-lua 安装为 Vim 的插件。具体步骤如下：

1. 安装 ibhagwan/fzf-lua 的 Git 仓库。
2. 在 Vim 的配置文件中添加 ibhagwan/fzf-lua 的插件设置。
3. 重启 Vim 编辑器。

**生产可用性**

ibhagwan/fzf-lua 的生产可用性较高，主要原因是：

1. 近期活动：项目维护者最近更新了项目。
2. 广泛采用：项目有 4344 个 GitHub star 和 258 个 fork。
3. 强大的生态系统：项目支持 Lua 语言

## 🧭 Practical evaluation

**Value:** ibhagwan/fzf-lua may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4344 GitHub stars
- 258 forks
- updated 2026-07-03
- primary language: Lua
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 60/100 |
| stars | 77/100 |
| topics | 75/100 |
| outlook | 58/100 |
| quality | 69/100 |
| recency | 40/100 |
| adoption | 73/100 |
| production | 58/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/ibhagwan/fzf-lua) · [← Back to Misc](./README.md)</sub>
