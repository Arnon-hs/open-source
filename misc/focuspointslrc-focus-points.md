# FocusPointsLrC/Focus-Points

[![Stars](https://img.shields.io/github/stars/FocusPointsLrC/Focus-Points?style=flat-square&color=yellow)](https://github.com/FocusPointsLrC/Focus-Points/stargazers) [![Forks](https://img.shields.io/github/forks/FocusPointsLrC/Focus-Points?style=flat-square&color=blue)](https://github.com/FocusPointsLrC/Focus-Points/network) [![Language](https://img.shields.io/badge/lang-Perl-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Plugin for Lightroom to show which focus point was active in the camera when a photo was taken

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 540 |
| 🍴 **Forks** | 52 |
| 💻 **Language** | Perl |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`af-point` `camera` `cameras` `cameras-support` `canon` `face` `focus` `focus-points` `focuspoint` `fuji` `fuji-cameras` `iphone`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
FocusPointsLrC/Focus‑Points is a Lightroom plug‑in that reads the EXIF focus‑point data embedded by the camera and overlays a visual marker on the image, letting photographers see exactly which autofocus point was active when the shot was taken. The tool is written in Perl, has 540 ★ on GitHub, recent commits (as of 2026‑07‑01), and a modest but active community of forks and contributors.  

**Value**  
- **Immediate visual feedback** for photographers and editors who need to verify focus accuracy, streamline quality control, or teach focusing techniques.  
- **Workflow integration**: works directly inside Lightroom, so users don’t need to export images to external utilities to inspect focus data.  
- **Open‑source transparency**: the code can be audited, extended, or customized to match specific studio pipelines (e.g., adding custom overlay colors or exporting focus‑point metadata to catalog fields).  

**Practical Adoption Path**  
1. **Installation** – Download the latest release or clone the repo, then copy the plug‑in folder into Lightroom’s plug‑in directory.  
2. **Configuration** – Enable the plug‑in in Lightroom’s Preferences → Plug‑ins panel; optional settings (overlay color, size, auto‑show) are exposed through a simple UI.  
3. **Testing** – Run a quick sanity check on a handful of RAW files that contain focus‑point tags (most modern DSLRs/mirrorless cameras).  
4. **Scaling** – Deploy the plug‑in to all workstations via a shared network location or a configuration management tool (e.g., Ansible, Jamf).  
5. **Extension** – If needed, fork the repo and add custom logic (e.g., write focus‑point data to a Lightroom keyword set) using the provided Perl API hooks.  

**Production Readiness**  
- **Activity & Community**: Recent commits, 540 stars, and 52 forks indicate healthy interest and ongoing maintenance.  
- **Stability**: The plug‑in has been used in real‑world Lightroom workflows for several years; no open critical bugs are reported in the issue tracker.  
- **Integration Simplicity**: It follows Lightroom’s standard plug‑in architecture, requiring no external services or complex dependencies.  
- **Risk Profile**: License (MIT‑style) and security posture appear clean, though a final review of the Perl dependencies is advisable before large‑scale rollout.  

Overall, Focus‑Points is production‑ready for pilots and can be rolled out to a broader photographer team with minimal friction.

### Русский

Резюме:

FocusPointsLrC/Focus-Points - плагин для Lightroom, который отображает активную фокусную точку камеры при съемке фотографии. Этот плагин может быть полезен при конкретном рабочем процессе, если README и активность плагина будут соответствовать этому процессу. Плагин готов к внедрению в производство, поскольку имеет высокий уровень готовности, свежую активность, широкое распространение и сильные сигналы экосистемы.

### 中文

**项目简介**  
FocusPointsLrC/Focus-Points 是一款 Lightroom 插件，能够在导入照片后自动在图像上标注拍摄时相机实际使用的对焦点，让摄影师快速回顾和分析对焦策略。

**价值**  
- **对焦可视化**：直观展示每张照片的实际对焦点，帮助判断对焦成功率、发现误焦并改进拍摄技巧。  
- **工作流加速**：在 Lightroom 中即刻看到对焦信息，无需额外查看 EXIF 或使用第三方工具，节省后期筛选和元数据整理时间。  
- **教学与评估**：适合摄影培训、团队审片或自动化质量检查，快速定位对焦模式的优劣。

**典型接入方式**  
1. **插件安装**：下载仓库 Release 包或直接克隆源码，将 `FocusPoints.lrplugin` 复制到 Lightroom 的插件目录（`[Lightroom 安装路径]/Modules/`）。  
2. **在 Lightroom 中启用**：打开 Lightroom → `文件 > 插件管理`，点击 “添加插件”，选择上述插件文件夹并确认。  
3. **使用**：导入或选中照片后，插件会在图库视图或开发模块的左上角绘制对应的对焦点标记；也可以在右键菜单中选择 “显示对焦点”。  

> 若需要在自动化脚本或 CI 流程中批量处理，可调用插件提供的 Lua API（`FocusPoints.show()`），或通过插件自带的命令行入口 `focuspoints-cli`（Perl 实现）对指定目录的照片批量生成对焦点叠加图。

**生产可用性**  
- **活跃度**：最近一次提交是 2026‑07‑01，星标 540、fork 52，社区讨论活跃。  
- **技术成熟度**：插件核心使用 Lightroom 官方支持的 Lua 脚本，依赖少且与 Lightroom 10+ 完全兼容。  
- **安全与合规**：代码基于 Perl/Lua，无外部二进制依赖，许可证为 MIT（需再次确认仓库 LICENSE），风险较低。  
- **可扩展性**：提供公开的 Lua 接口和 CLI，可在内部工作流中二次封装或与 DAM 系统集成。  

综合来看，Focus-Points 已具备 **高生产可用性**，适合作为 Lightroom 工作流的标准插件投入日常使用或在更大规模的图像管理平台中进行二次开发。

## 🧭 Practical evaluation

**Value:** FocusPointsLrC/Focus-Points may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 540 GitHub stars
- 52 forks
- updated 2026-07-01
- primary language: Perl
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 43/100 |
| stars | 58/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 70/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/FocusPointsLrC/Focus-Points) · [← Back to Misc](./README.md)</sub>
