# jotego/jtcores

[![Stars](https://img.shields.io/github/stars/jotego/jtcores?style=flat-square&color=yellow)](https://github.com/jotego/jtcores/stargazers) [![Forks](https://img.shields.io/github/forks/jotego/jtcores?style=flat-square&color=blue)](https://github.com/jotego/jtcores/network) [![Language](https://img.shields.io/badge/lang-Verilog-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> FPGA cores compatible with multiple arcade game machines and KiCAD schematics of arcade games. Working on MiSTer FPGA/Analogue Pocket

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 307 |
| 🍴 **Forks** | 53 |
| 💻 **Language** | Verilog |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`arcade` `fpga` `kicad-schematics` `misterfpga` `retrogaming`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
jotego/jtcores is an open‑source collection of Verilog FPGA cores that emulate a wide range of classic arcade machines, accompanied by KiCAD schematics for the original hardware. The project targets FPGA platforms such as the MiSTer and the Analogue Pocket, enabling hobbyists and developers to run arcade games on modern, low‑latency hardware. With over 300 ★ on GitHub and recent activity, it serves as a ready‑made building block for arcade‑retro projects.

**Value proposition**  
- **Hardware‑level compatibility** – The cores reproduce the exact timing and video/audio behavior of dozens of arcade boards, which is essential for accurate preservation and for developers who need a faithful reference implementation.  
- **Design assets** – KiCAD schematics give users a complete view of the original PCB, useful for hardware reverse‑engineering, custom board design, or educational purposes.  
- **Cross‑platform support** – Ready‑to‑run on MiSTer (a popular open‑source retro‑gaming console) and the Analogue Pocket, lowering the barrier to integrate arcade emulation into existing FPGA‑based products.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repository, run the provided Makefile or scripts on a MiSTer board to load a single core (e.g., *jtframe* → *jtgng*). Verify that the core boots and runs a ROM you own.  
2. **Documentation check** – Review the README, core‑specific docs, and the KiCAD files to ensure they match your target workflow (e.g., board redesign or integration into a larger FPGA system).  
3. **Customization** – If you need additional I/O (e.g., custom button mapping, HDMI output), fork the repo and modify the top‑level wrapper; the modular structure (jtframe core library + per‑game cores) makes this straightforward.  
4. **CI/validation** – Add the core to your own CI pipeline (e.g., using the provided simulation testbenches) to catch regressions before committing to production.  

**Production readiness**  
- **Maturity** – Medium. The codebase is actively maintained (last commit 2026‑06‑28) and widely used in the MiSTer community, making it suitable for prototypes and internal tools.  
- **Dependencies** – Primarily Verilog and standard FPGA toolchains (Quartus, Vivado, or open‑source Yosys/nextpnr). Verify compatibility with your target device’s tool version.  
- **Risk considerations** – The repository lacks a formal security audit and the licensing details need confirmation (likely GPL‑3 or similar). Before shipping a commercial product, perform a license compliance check and a lightweight security review of the Verilog sources.  
- **Scalability** – Because each arcade system is encapsulated as a separate core, you can start with a single game and later expand the library without major architectural changes.  

Overall, jtcores offers a solid, community‑validated foundation for integrating authentic arcade emulation into FPGA‑based products, provided you perform the usual due‑diligence on licensing, security, and toolchain compatibility.

### Русский

**jotego/jtcores** — открытый набор FPGA‑ядер для эмуляции множества аркадных машин, сопровождающийся KiCAD‑схемами и поддержкой платформ MiSTer, Analogue Pocket и других. Проект подходит для быстрого прототипирования аркадных консолей или интеграции в кастомные FPGA‑решения, при этом рекомендуется начать с небольшого proof‑of‑concept и проверки README/активности репозитория. Готовность к production — средняя: ядра стабильно работают, но перед выпуском в продакшн следует уточнить лицензию, состояние безопасности и наличие активных мейнтейнеров.

### 中文

**项目简介**  
jotego/jtcores 是一个开源的 FPGA 核心库，提供兼容多款街机游戏机的硬件实现以及对应的 KiCAD 原理图，支持 MiSTer FPGA 与 Analogue Pocket 等平台。  

**价值**  
- **快速原型**：直接复用成熟的 Verilog 核心，可在 FPGA 开发板上几乎即插即用地运行经典街机游戏。  
- **硬件参考**：完整的 KiCAD 设计帮助硬件工程师快速搭建或定制自己的街机/复古游戏板卡。  
- **社区活跃**：307 ⭐、53 fork，近期仍在更新，拥有一定的社区支持与文档（README、示例）。  

**典型接入方式**  
1. **代码获取**：`git clone https://github.com/jotego/jtcores.git`。  
2. **子模块/核心选择**：在 `cores/` 目录下挑选目标游戏（如 `jtgng`, `jttora`），阅读对应的 `README.md` 获取编译指令。  
3. **集成到现有 FPGA 项目**：  
   - 将所需核心的 Verilog 文件以及依赖的 `jtframe`、`jt12` 等公共库加入项目源码树。  
   - 在顶层模块中实例化核心，连接时钟、复位、视频、音频、IO（按钮、SD 卡）等信号。  
   - 使用 Quartus / Vivado 等工具编译生成 bitstream，下载到 MiSTer/Analogue Pocket 开发板。  
4. **验证**：使用项目自带的 ROM 测试向导或自行准备的游戏 ROM，确认视频/音频输出正常。  

**生产可用性**  
- **成熟度**：处于 **Medium** 级别，适合作为原型或内部工具使用；核心已在多个社区 FPGA 项目中验证。  
- **依赖管理**：主要依赖 Verilog 代码和 KiCAD 文件，外部库较少，易于审计。  
- **维护状态**：最近一次提交在 2026‑06‑28，仍有活跃维护者，但需自行检查许可证（GPL‑3.0）与安全审计。  
- **上线建议**：在正式生产前，先做小范围的 PoC（如单一游戏核心），完成以下步骤后再评估大规模部署：  
  1. 完整跑通编译‑下载‑运行闭环。  
  2. 对关键信号（时钟、IO）进行时序分析，确保满足目标 FPGA 的约束。  
  3. 编写或补全项目文档，锁定依赖的 commit 哈希，防止上游突变。  

总体来说，jtcores 为需要在 FPGA 上实现复古街机游戏的团队提供了即插即用的硬件/软件资产，适合作为原型平台或内部工具；在完成上述验证与合规检查后，可进入小批量生产或定制化硬件开发阶段。

## 🧭 Practical evaluation

**Value:** jotego/jtcores may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 307 GitHub stars
- 53 forks
- updated 2026-06-28
- primary language: Verilog
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 43/100 |
| stars | 53/100 |
| topics | 63/100 |
| outlook | 65/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 50/100 |
| production | 67/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/jotego/jtcores) · [← Back to Misc](./README.md)</sub>
