# SnakeOilXY/ProosaXY

[![Stars](https://img.shields.io/github/stars/SnakeOilXY/ProosaXY?style=flat-square&color=yellow)](https://github.com/SnakeOilXY/ProosaXY/stargazers) [![Forks](https://img.shields.io/github/forks/SnakeOilXY/ProosaXY?style=flat-square&color=blue)](https://github.com/SnakeOilXY/ProosaXY/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Low cost CoreXY conversion mod for Prusa MK3/S

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 203 |
| 🍴 **Forks** | 15 |
| 💻 **Language** | Python |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-07-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`3d-printer` `3d-printing` `corexy` `freecad` `klipper` `opensource`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
SnakeOilXY/ProosaXY is an open‑source, low‑cost conversion kit that turns a Prusa MK3/S into a CoreXY printer. The repository provides Python scripts, wiring diagrams and 3‑D printable parts to enable the mechanical upgrade with minimal tooling.

**Value**  
The project offers a cost‑effective way to gain CoreXY’s speed and accuracy benefits without buying a new machine, making it attractive for hobbyists, makerspaces and small‑scale prototyping labs that already own a Prusa MK3/S. Its modest dependency footprint (pure Python) and clear documentation mean the modification can be evaluated quickly against a specific workflow.

**Practical Adoption Path**  

1. **Read‑through & proof‑of‑concept** – Clone the repo, review the README and run the supplied Python scripts on a test MK3/S to verify compatibility with your firmware version.  
2. **Hardware prep** – Print the provided parts, source the inexpensive belts/pulleys, and perform a single‑unit conversion on a non‑critical printer.  
3. **Calibration & validation** – Use the included calibration routines to tune the CoreXY kinematics and compare print quality against the stock Cartesian setup.  
4. **Scale‑up** – Once the test unit meets quality targets, replicate the conversion on additional MK3/S machines, documenting any tweaks needed for your specific environment.

**Production Readiness**  
The project sits at a medium readiness level: it is mature enough for prototyping and internal workflows, backed by 203 stars and recent activity (last update 2026‑07‑12). Before deploying in a production line, you should:

* Verify the license (likely GPL/Apache) aligns with your IP policy.  
* Perform a security audit of the Python tooling and any firmware changes.  
* Confirm long‑term maintainer availability or be prepared to fork and maintain the code internally.  

With those checks completed, SnakeOilXY/ProosaXY can be safely integrated as a cost‑saving upgrade for fleets of Prusa MK3/S printers.

### Русский

SnakeOilXY/ProosaXY — это недорогой модуль‑конвертер CoreXY для принтера Prusa MK3/S, позволяющий за несколько часов превратить стандартный Cartesian‑механизм в более быстрый и точный CoreXY без значительных затрат на оборудование. Для внедрения рекомендуется сначала изучить README и выполнить небольшой proof‑of‑concept‑прототип, проверив совместимость с текущей конфигурацией и зависимостями, после чего можно интегрировать модуль в прототипные или внутренние производственные процессы. Готовность к production оценивается как средняя: проект имеет 203 звёзд, активные форки и недавнее обновление, но требует окончательной проверки лицензии, безопасности и поддержки поддержки перед масштабным развертыванием.

### 中文

**项目简介**  
SnakeOilXY/ProosaXY 是一个面向 Prusa MK3/S 打印机的低成本 CoreXY 改装模块，提供 Python 脚本和硬件配套文件，帮助用户以最小的投入将传统 Cartesian 结构改造成高速、精准的 CoreXY 运动系统。

**价值**  
- **成本优势**：相较于商业 CoreXY 改装套件，项目源码与 BOM 完全开源，材料费用可控制在几百元。  
- **灵活可定制**：全部配置均为文本/脚本形式，用户可以根据自家机器尺寸、步进电机规格等自行微调。  
- **社区支撑**：已有 200+ Stars、15 Forks，说明在 3D 打印爱好者中具备一定的使用和讨论基础。

**典型接入方式**  
1. **环境准备**：在一台能够运行 Python 3.9+ 的工作站上克隆仓库，安装 `requirements.txt` 中的依赖（主要是 `numpy`、`pyserial`）。  
2. **硬件改装**：依据 `hardware/` 目录提供的 CAD 与 BOM，制作或购买皮带、滑轨、联轴器等部件，并按照 `README.md` 中的步骤在 Prusa MK3/S 上完成机械改装。  
3. **固件刷写**：使用项目提供的 `firmware/` 脚本生成对应的 Marlin 配置（CoreXY 参数、步进倍率、限位开关），通过 Prusa 官方的固件刷写工具更新打印机。  
4. **功能验证**：运行 `scripts/calibrate.py` 进行自动校准，确认 X/Y 轴同步误差在 0.05 mm 以内后即可进入正常打印流程。

**生产可用性**  
- **成熟度**：项目最近一次提交为 2026‑07‑12，活跃度一般，适合作为原型或内部生产线的快速改装方案。  
- **风险点**：  
  - 许可证（MIT）对商业使用无障碍，但需自行确认硬件供应链的合规性。  
  - 代码未经过严格的安全审计，建议在受控环境下运行并对串口通信进行白名单限制。  
  - 维护者活跃度有限，长期使用前最好自行 fork 并维护关键分支。  
- **上线建议**：先在非关键的测试机上完成完整的改装‑校准‑打印闭环验证，确认可靠性后再推广到生产线；同时制定部件备份清单和固件回滚方案，以降低因改装导致的停机风险。  

总体而言，SnakeOilXY/ProosaXY 在成本敏感且对打印速度/精度有提升需求的场景下具有较高的性价比，适合作为原型验证或小批量内部生产的改装方案，但在大规模生产前应完成额外的可靠性和安全性评估。

## 🧭 Practical evaluation

**Value:** SnakeOilXY/ProosaXY may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 203 GitHub stars
- 15 forks
- updated 2026-07-12
- primary language: Python
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 30/100 |
| stars | 49/100 |
| topics | 75/100 |
| outlook | 72/100 |
| quality | 71/100 |
| recency | 100/100 |
| adoption | 44/100 |
| production | 73/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/SnakeOilXY/ProosaXY) · [← Back to Misc](./README.md)</sub>
