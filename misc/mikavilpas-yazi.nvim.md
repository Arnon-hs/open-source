# mikavilpas/yazi.nvim

[![Stars](https://img.shields.io/github/stars/mikavilpas/yazi.nvim?style=flat-square&color=yellow)](https://github.com/mikavilpas/yazi.nvim/stargazers) [![Forks](https://img.shields.io/github/forks/mikavilpas/yazi.nvim?style=flat-square&color=blue)](https://github.com/mikavilpas/yazi.nvim/network) [![Language](https://img.shields.io/badge/lang-Lua-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> A Neovim Plugin for the yazi terminal file manager

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.7k |
| 🍴 **Forks** | 51 |
| 💻 **Language** | Lua |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`neovim` `plugin` `yazi` `yazi-plugin`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
`mikavilpas/yazi.nvim` is a lightweight Neovim plugin that lets you launch and control the **yazi** terminal file manager directly from the editor. With a few simple commands it opens a split terminal running yazi, synchronises the current buffer, and forwards yazi’s events back into Neovim, making file navigation feel native.  

**Value**  
- **Seamless workflow**: Developers who already use yazi for fast, keyboard‑driven file browsing can stay inside Neovim without context‑switching to a separate terminal window.  
- **Extensible signals**: The plugin emits Lua callbacks and CLI hooks that other plugins (e.g., project trees, status lines) can listen to, enabling custom integrations such as auto‑refreshing buffers or updating Git status.  
- **Low overhead**: Implemented in pure Lua, it adds minimal startup cost and works with any recent Neovim (0.9+).  

**Practical adoption path**  
1. **Add the plugin** via your favourite manager (e.g., `packer`, `lazy.nvim`).  
2. **Configure** the optional key‑maps and callbacks (e.g., `YaziOpen`, `YaziClose`).  
3. **Install yazi** on the host system (the plugin only calls the external binary).  
4. **Iterate**: test the basic open/close flow, then hook into events (`on_enter`, `on_exit`) to tailor buffer handling or integrate with other tools.  

**Production readiness**  
- **Maturity**: 1.7k stars, 51 forks, recent commit (2026‑05‑11) indicate healthy community interest.  
- **Stability**: Core functionality (open/close, event forwarding) is straightforward and has few external dependencies beyond the yazi binary.  
- **Risk considerations**: The repository lacks a formal license file and has limited documentation on security or long‑term maintainer commitment, so a quick audit of the license and a review of any open issues is advisable before deploying to critical environments.  
- **Recommendation**: Suitable for prototypes, internal tooling, or teams already using yazi; with a brief license/security check and a test‑suite validation, it can be promoted to production for regular development workflows.

### Русский

**mikavilpas/yazi.nvim** — это Lua‑плагин для Neovim, позволяющий управлять файлами через терминальный файловый менеджер yazi прямо из редактора (например, открывать, перемещать и просматривать файлы через `:Yazi` и получать сигналы о выбранных элементах). Он подходит для разработчиков, которые уже используют yazi в своей локальной среде и хотят интегрировать его в рабочий процесс Neovim без переключения контекстов. Проект имеет средний уровень готовности к production: активные коммиты, более 1700 звёзд и поддержка основных API, но перед внедрением в критически важные системы рекомендуется проверить лицензию, безопасность зависимостей и наличие поддерживающего мейнтейнера.

### 中文

**项目简介**  
`mikavilpas/yazi.nvim` 是一个 Neovim 插件，用于在编辑器内部无缝调用并交互 **yazi** 这款高性能终端文件管理器。它通过 Lua 实现，提供快捷键、自动刷新和文件选中等功能，让用户在编辑代码时即可完成文件浏览、打开、移动等操作，提升工作流的连贯性。

**价值**  
- **提升效率**：无需离开 Neovim，即可使用 yazi 的分屏预览、批量操作等特性，省去在终端与编辑器之间切换的时间。  
- **统一体验**：保持 Neovim 的键位风格和 UI 统一，降低学习成本，适合已经在使用 yazi 的开发者。  
- **可定制**：插件暴露 Lua API，支持自定义快捷键、事件回调和行为扩展，方便根据团队工作流进行二次开发。

**典型接入方式**  
1. **插件管理器安装**（以 `lazy.nvim` 为例）  
   ```lua
   {
     "mikavilpas/yazi.nvim",
     dependencies = { "folke/which-key.nvim" },   -- 可选，用于键位提示
     config = function()
       require("yazi").setup{
         -- 下面的选项仅为示例，可根据需求自行配置
         open_on_startup = true,
         keymaps = {
           open = "<leader>yo",   -- 打开 yazi
           select = "<CR>",       -- 选中文件后返回 Neovim
         },
       }
     end,
   }
   ```
2. **使用快捷键**：安装后，默认会在 `:Yazi` 命令或配置的快捷键下启动 yazi，选中文件后自动在当前 buffer 中打开。  
3. **API 调用**（高级用法）  
   ```lua
   local yazi = require("yazi")
   yazi.open({ cwd = vim.fn.expand("%:p:h") })   -- 在当前文件所在目录打开 yazi
   ```

**生产可用性**  
- **成熟度**：已有 1700+ ⭐、50+ forks，最近一次提交在 2026-05-11，活跃度良好。  
- **依赖**：仅依赖 Neovim (>=0.9) 与外部的 `yazi` 可执行文件，部署成本低。  
- **风险**：仍需确认许可证兼容性（MIT/Apache 等），以及对内部安全策略的审查；插件本身的错误处理相对简单，建议在生产环境中配合监控或回退方案。  
- **适用场景**：非常适合作为原型、内部工具或对文件管理有高频需求的团队使用；在对可靠性要求极高的生产环境中，建议先在预上线环境进行充分测试后再推广。

## 🧭 Practical evaluation

**Value:** mikavilpas/yazi.nvim may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1708 GitHub stars
- 51 forks
- updated 2026-05-11
- primary language: Lua
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 43/100 |
| stars | 69/100 |
| topics | 50/100 |
| outlook | 67/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 62/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/mikavilpas/yazi.nvim) · [← Back to Misc](./README.md)</sub>
