# FylerOrg/fyler.nvim

[![Stars](https://img.shields.io/github/stars/FylerOrg/fyler.nvim?style=flat-square&color=yellow)](https://github.com/FylerOrg/fyler.nvim/stargazers) [![Forks](https://img.shields.io/github/forks/FylerOrg/fyler.nvim?style=flat-square&color=blue)](https://github.com/FylerOrg/fyler.nvim/network) [![Language](https://img.shields.io/badge/lang-Lua-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> A neovim file manager which can edit file system like a buffer with tree view

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 739 |
| 🍴 **Forks** | 49 |
| 💻 **Language** | Lua |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`file-manager` `neovim-plugin` `nvim` `telescope-extension`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
FylerOrg/fyler.nvim is a Neovim plugin that turns the file system into an editable buffer with a tree‑view interface, letting you browse, create, rename, and delete files directly from within Neovim. With 739 ★ and recent updates (as of 2026‑06‑27), it offers a lightweight, Lua‑native solution for developers who want a tighter “file‑manager‑as‑code” workflow.

**Value**  
- **Seamless workflow:** Eliminates context‑switching between the editor and an external file manager, speeding up refactoring, project navigation, and bulk file operations.  
- **Programmable API:** Exposes signals and functions that can be hooked into custom Lua scripts or other plugins, enabling automation (e.g., auto‑generating project scaffolds).  
- **Low overhead:** Pure‑Lua implementation means no external binaries are required, keeping the Neovim startup time minimal.

**Practical adoption path**  
1. **Trial:** Add `fyler.nvim` to your plugin manager (e.g., `packer.nvim` or `lazy.nvim`) and enable the default keymaps.  
2. **Customization:** Use the provided API (`fyler.open()`, `fyler.rename()`, etc.) to tailor the tree view to your project layout or to integrate with existing tooling (e.g., LSP, git plugins).  
3. **Automation:** Write small Lua wrappers that trigger `fyler` actions from other plugins or CI scripts, gradually replacing ad‑hoc shell commands.  
4. **Evaluation:** Monitor performance and stability in a non‑critical branch before promoting to the main development environment.

**Production readiness**  
- **Maturity:** Medium. The plugin is actively maintained, has a solid star count, and recent commits suggest ongoing support, but the contributor base is small.  
- **Risk considerations:** Verify the license (MIT‑style) aligns with your policy, run a quick security audit of the Lua code, and confirm that the maintainer responds to issues.  
- **Fit for production:** Suitable for internal tools, prototypes, or teams that already rely heavily on Neovim. For mission‑critical environments, pair it with a fallback external file manager and establish a maintenance plan (e.g., pinning a known good commit).

### Русский

Резюме проекта FylerOrg/fyler.nvim:

FylerOrg/fyler.nvim - это открытый проект Neovim, который позволяет редактировать файловую систему, подобно буферу с деревовидным представлением. Этот проект может быть полезен для конкретных рабочих процессов, если его README и активность соответствуют конкретной цели. Проект находится на среднем уровне готовности к production, что означает, что он может быть полезен для прототипов или внутренних рабочих процессов, но требует проверки зависимостей и поддержки перед внедрением в производство.

### 中文

**项目简介**  
FylerOrg/fyler.nvim 是一款基于 Neovim 的文件管理插件，能够在编辑器中以树状视图直接浏览、创建、移动、删除文件和目录，让文件系统像普通 buffer 一样进行交互式编辑。

**价值**  
- **提升工作流效率**：在编辑代码时无需切换到终端或文件浏览器，所有文件操作都在同一窗口完成，极大缩短查找与管理文件的时间。  
- **无缝集成 Neovim 生态**：使用 Lua 编写，天然兼容插件管理器（如 lazy.nvim、packer.nvim），并提供 API 接口，方便二次开发或与其他插件（如 telescope、nvim-tree）联动。  
- **轻量且可定制**：核心功能仅几千行代码，支持自定义键位、显示样式和过滤规则，适合个人工作流或团队内部工具链。

**典型接入方式**  
```lua
-- 使用 lazy.nvim 安装
require('lazy').setup({
  {
    'FylerOrg/fyler.nvim',
    config = function()
      require('fyler').setup{
        -- 关键配置示例
        hide_dotfiles = false,
        keymaps = {
          open   = 'o',
          rename = 'r',
          delete = 'd',
        },
      }
    end,
  },
})
```
- 通过上述方式即可在 Neovim 启动时加载插件。  
- 若需要在其他插件中调用，可使用公开的 Lua API，例如 `require('fyler').open(path)`、`require('fyler').rename(old, new)` 等。

**生产可用性**  
- **成熟度**：截至 2026‑06‑27，项目已有 739 星、49 Fork，最近一次提交在同一天，活跃度良好。  
- **适用场景**：非常适合原型开发、内部工具或个人日常使用；在对文件操作频繁且希望保持全键盘工作流的团队中表现尤佳。  
- **风险与注意事项**：仍需自行审查许可证（MIT）以及潜在的安全依赖；在大规模生产环境使用前建议做好以下检查：  
  1. **依赖锁定**：确认插件及其依赖的 Lua 版本在目标环境中稳定。  
  2. **维护者沟通**：关注 Issues/PR 以确认维护者的响应速度。  
  3. **性能评估**：在大项目目录下测试树渲染和文件操作的响应时间。  

综合来看，fyler.nvim 已具备中等生产可用性，适合作为内部或原型项目的文件管理方案，在完成上述检查后即可投入正式使用。

## 🧭 Practical evaluation

**Value:** FylerOrg/fyler.nvim may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 739 GitHub stars
- 49 forks
- updated 2026-06-27
- primary language: Lua
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 61/100 |
| topics | 50/100 |
| outlook | 65/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 56/100 |
| production | 67/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/FylerOrg/fyler.nvim) · [← Back to Misc](./README.md)</sub>
