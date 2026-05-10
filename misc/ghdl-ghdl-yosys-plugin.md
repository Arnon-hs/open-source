# ghdl/ghdl-yosys-plugin

[![Stars](https://img.shields.io/github/stars/ghdl/ghdl-yosys-plugin?style=flat-square&color=yellow)](https://github.com/ghdl/ghdl-yosys-plugin/stargazers) [![Forks](https://img.shields.io/github/forks/ghdl/ghdl-yosys-plugin?style=flat-square&color=blue)](https://github.com/ghdl/ghdl-yosys-plugin/network) [![Language](https://img.shields.io/badge/lang-VHDL-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> VHDL synthesis (based on ghdl)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 360 |
| 🍴 **Forks** | 32 |
| 💻 **Language** | VHDL |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-05-10 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **ghdl/ghdl‑yosys‑plugin** adds VHDL synthesis support to Yosys by leveraging the open‑source GHDL compiler. It enables designers to run Yosys’s powerful RTL optimisation and netlist generation directly on VHDL sources, closing the gap between VHDL design and modern open‑source FPGA/ASIC flows.

**Value Proposition**  
- **Unified open‑source flow:** Combines GHDL’s fully‑compliant VHDL front‑end with Yosys’s synthesis engine, eliminating the need for commercial VHDL synthesis tools.  
- **Rapid prototyping:** Allows teams already using Yosys for Verilog to experiment with VHDL designs without learning a new toolchain.  
- **Community‑backed:** With ~360 stars and regular commits (last update 2026‑05‑10), the project shows active interest and a growing ecosystem.

**Practical Adoption Path**  

| Step | Action | Goal |
|------|--------|------|
| 1️⃣  | **Read the README** – verify supported GHDL/Yosys versions and required dependencies (e.g., GHDL 2.x, Yosys 0.38+). | Ensure compatibility with your existing toolchain. |
| 2️⃣  | **Proof‑of‑concept build** – clone the repo, compile the plugin, and run `yosys -m ghdl` on a small VHDL testbench. | Validate that the plugin loads and produces a netlist. |
| 3️⃣  | **Integrate into CI** – add a lightweight job that runs synthesis on a representative VHDL module and checks for successful elaboration and netlist generation. | Detect integration issues early and lock down versions. |
| 4️⃣  | **Expand to full design** – replace the commercial synthesis step with `yosys -m ghdl -p "ghdl ...; synth ..."` in your build scripts. | Transition to the open‑source flow for all VHDL sources. |
| 5️⃣  | **Performance & verification** – compare resource utilisation and timing reports against the previous tool; add regression tests. | Confirm that the open‑source flow meets design goals. |

**Production‑Readiness Assessment**  

- **Maturity:** Medium. The plugin is functional and actively maintained, but it is still a niche component (32 forks) and not yet a “battle‑tested” production staple.  
- **Stability:** Recent commits (as of 2026‑05‑10) indicate ongoing maintenance, yet you should lock the version you ship and monitor upstream changes.  
- **Dependencies:** Relies on GHDL and Yosys versions; both are well‑known open‑source projects, but you must verify binary compatibility on your target OS/architecture.  
- **Risk Mitigation:**  
  - Perform a security scan of the plugin source and its build artifacts.  
  - Review the license (BSD‑3‑Clause) for compliance with your organization’s policies.  
  - Keep a fallback path to a commercial synthesiser in case edge‑case VHDL constructs are not yet supported.  

**Conclusion**  
The ghdl‑yosys‑plugin offers a compelling, cost‑free route to synthesize VHDL with Yosys, making it attractive for prototypes, internal toolchains, or organizations moving toward an all‑open‑source hardware flow. With a small, well‑scoped proof‑of‑concept and careful version pinning, it can be safely introduced into production pipelines, provided you maintain vigilance on updates, licensing, and any synthesis‑specific limitations.

### Русский

**g​hdl‑yosys‑plugin** — это открытый плагин, позволяющий использовать возможности GHDL для синтеза VHDL‑кода в рамках Yosys. Он подходит для быстрого прототипирования и внутренних потоков разработки, где требуется собрать VHDL‑модуль в бит‑строку без перехода к коммерческим синтезаторам; типичный сценарий — подключить плагин к существующей цепочке Yosys, запустить `yosys -m ghdl` и получить netlist. Готовность к продакшну — средняя: проект имеет активные коммиты, 360 звёзд и 32 форка, но перед вводом в производство следует проверить лицензию, безопасность зависимостей и наличие поддерживающих мейнтейнеров.

### 中文

**简短介绍**  
ghdl‑yosys‑plugin 是一个将 GHDL（开源 VHDL 编译器）与 Yosys 逻辑综合工具相结合的插件，能够直接对 VHDL 代码进行综合生成可用于 FPGA/ASIC 的网表。它为使用 VHDL 的硬件设计团队提供了一个完整的开源综合流水线，省去商业综合器的许可成本。

**价值**  
- **统一工具链**：在同一套开源工具（GHDL + Yosys）中完成 VHDL 编译、语义检查、综合和网表生成，降低学习成本和工具链维护成本。  
- **成本优势**：完全免费、源码可审计，适合预算有限的科研、教学或初创公司。  
- **可定制性**：插件代码开放，可根据项目需求自行扩展或调优合成策略。  

**典型接入方式**  
1. **准备环境**：在 Linux/macOS 上安装 GHDL（>=2.0）和 Yosys（>=0.35）。  
2. **获取插件**：`git clone https://github.com/ghdl/ghdl-yosys-plugin.git && cd ghdl-yosys-plugin`。  
3. **编译插件**：`make`（会生成 `ghdl.so`），随后在 Yosys 中通过 `plugin -i ghdl.so` 加载。  
4. **运行合成**：在 Yosys 脚本中使用 `ghdl` 前端读取 VHDL 源，例如  
   ```tcl
   read_ghdl -e top_entity
   synth_xilinx -top top_entity
   write_edif top.edif
   ```  
   这一步即可完成从 VHDL 到目标厂商网表的全链路合成。  

**生产可用性**  
- **成熟度**：项目已有 360+ stars、32 forks，最近一次提交在 2026‑05‑10，活跃度尚可。  
- **适用场景**：非常适合作为原型验证、教学实验或内部研发的合成工具；在对可靠性、长期维护有严格要求的商业生产线上使用前，建议进行以下检查：  
  - **依赖管理**：确认 GHDL、Yosys 以及插件的版本兼容性，并在 CI 中锁定具体版本。  
  - **安全审计**：检查源码许可证（BSD‑3‑Clause）是否符合公司合规，进行基本的静态代码审计。  
  - **维护计划**：评估社区活跃度，若关键功能出现 bug，可自行维护分支或考虑商业支持。  

总体而言，ghdl‑yosys‑plugin 在原型和内部工作流中已具备“中等”生产可用性；在完成上述依赖、合规和维护准备后，可安全用于生产环境的 VHDL 综合任务。

## 🧭 Practical evaluation

**Value:** ghdl/ghdl-yosys-plugin may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 360 GitHub stars
- 32 forks
- updated 2026-05-10
- primary language: VHDL

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 54/100 |
| topics | 0/100 |
| outlook | 66/100 |
| quality | 62/100 |
| recency | 100/100 |
| adoption | 50/100 |
| production | 70/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-10 · [View on GitHub](https://github.com/ghdl/ghdl-yosys-plugin) · [← Back to Misc](./README.md)</sub>
