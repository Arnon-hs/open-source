# kholia/xvc-pico

[![Stars](https://img.shields.io/github/stars/kholia/xvc-pico?style=flat-square&color=yellow)](https://github.com/kholia/xvc-pico/stargazers) [![Forks](https://img.shields.io/github/forks/kholia/xvc-pico?style=flat-square&color=blue)](https://github.com/kholia/xvc-pico/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-44%2F100-brightgreen?style=flat-square)](#)

> Raspberry Pico powered Xilinx Virtual Cable - Xilinx JTAG Cable! This is now quite fast, thanks to tom01h! We also support JTAG + serial terminal over a single cable now. Now with (slow) WiFi support for Pico W!

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 489 |
| 🍴 **Forks** | 66 |
| 💻 **Language** | C |
| 📈 **Score** | 44/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
kholia/xvc-pico turns a Raspberry Pi Pico (or Pico W) into a Xilinx Virtual Cable, providing a fast JTAG interface—now with optional serial‑terminal sharing and experimental Wi‑Fi support. The project is actively maintained (last update 2026‑06‑27), written in C, and has attracted a modest community (≈ 490 ★, 66 forks).  

**Value Proposition**  
- **Rapid UI prototyping** – By exposing a ready‑made hardware‑abstraction layer, developers can focus on the front‑end of their debugging/flash tools instead of writing low‑level JTAG drivers.  
- **Component reuse** – The same Pico‑based cable can be used across multiple Xilinx devices, letting teams standardise on a single, inexpensive hardware platform.  
- **Cost‑effective hardware** – A Pico costs a few dollars, so the overall bill of materials stays low while still delivering JTAG speeds comparable to commercial cables (thanks to the recent performance boost from tom01h).  

**Practical Adoption Path**  
1. **Prototype & evaluate** – Clone the repo, flash the provided firmware onto a Pico/Pico W, and connect it to a target Xilinx board. Verify JTAG operation with the upstream `xvc` client (e.g., OpenOCD or Vivado).  
2. **Integrate into the toolchain** – Add the Pico’s USB endpoint as a custom transport in your existing debugging UI. Because the repository’s metadata is sparse, you’ll need to read the `README` and source files to understand the command‑set and any required libusb wrappers.  
3. **Extend for serial‑terminal** – If you need the combined JTAG + UART feature, enable the `SERIAL` compile flag and map the Pico’s UART pins to the target board.  
4. **Optional Wi‑Fi** – For remote debugging, flash the `pico_w` branch, configure the SSID/password in `wifi_config.h`, and test the slower TCP‑based XVC stream.  

**Production Readiness**  
- **Maturity:** Medium. The core JTAG functionality is stable and fast; the serial‑over‑single‑cable and Wi‑Fi features are newer and less battle‑tested.  
- **Reliability:** Suitable for internal prototypes, test rigs, or low‑volume production where a cheap, replaceable cable is acceptable.  
- **Risk Mitigation:**  
  * Verify the firmware version matches your target Xilinx part (some devices need specific XVC packet sizes).  
  * Conduct a stress test (continuous JTAG reads/writes) to confirm the Pico’s thermal behaviour under load.  
  * Keep an eye on upstream updates; the project is actively maintained but does not yet provide a formal release schedule or CI‑validated binary artifacts.  

In short, kholia/xvc-pico offers a low‑cost, high‑performance JTAG bridge that can accelerate UI development for debugging tools, provided you allocate time for manual integration and validation before rolling it out to production environments.

### Русский

**kholia/xvc-pico** — это открытый драйвер для Raspberry Pico, превращающий его в быстрый Xilinx Virtual Cable (JTAG‑кабель) с поддержкой одновременного JTAG + serial‑терминала и (медленного) Wi‑Fi для Pico W. Проект удобно использовать при создании пользовательских интерфейсов и прототипов, когда требуется быстро подключить FPGA к ПК без отдельного оборудования, при этом можно переиспользовать готовые UI‑компоненты для ускорения разработки. Готовность к production — средняя: проект стабилен для прототипов и внутренних процессов, но требует ручной проверки интеграции и оценки затрат на настройку перед выпуском в продакшн.

### 中文

**项目简介（2‑3 句）**  
kholia/xvc-pico 将 Raspberry Pico（及 Pico W）打造成 Xilinx Virtual Cable，实现高速 JTAG 以及 JTAG+串口复用的单线调试方案，并加入了（慢速）Wi‑Fi 支持，方便在没有专用硬件的环境下进行 FPGA 调试和烧录。

**价值**  
- **降低硬件成本**：使用廉价的 Pico 即可替代商业 XVC 适配器，省去专用 JTAG 线缆和调试卡的开支。  
- **提升调试效率**：得益于 tom01h 的优化，JTAG 传输速度显著提升，配合单线 JTAG+Serial，能够在同一根线缆上完成调试和日志输出，简化现场布线。  
- **灵活扩展**：Pico W 版提供 Wi‑Fi 连接，适合远程调试或在空间受限的实验平台上使用。

**典型接入方式**  
1. **硬件准备**：将 Raspberry Pico（或 Pico W）通过 micro‑USB 连接到主机，使用两根跳线分别接到 FPGA 的 TCK、TMS、TDI、TDO、TRST（如有）以及可选的 UART 引脚。  
2. **固件烧录**：克隆仓库 → 使用 `picotool` 或 `openocd` 将 `xvc-pico.uf2` 烧录到 Pico。  
3. **软件配置**：在主机上安装 Xilinx 官方的 `xvc_server`（或直接使用仓库提供的 Python 客户端），指定 Pico 的串口（或 Wi‑Fi IP）作为 XVC 服务器地址。  
4. **集成到工具链**：在 Vivado/ISE 中添加 XVC 服务器地址，即可像使用标准 XVC 适配器一样进行 JTAG 编程、调试和串口交互。  

**生产可用性**  
- **成熟度**：GitHub 近 500 星、66 fork，最近一次更新在 2026‑06‑27，代码以 C 语言实现，核心功能已相对稳定。  
- **适用场景**：适合原型开发、内部测试平台或预算受限的项目；对生产线的高可靠性、长寿命和严格认证要求仍需额外评估。  
- **风险与注意事项**：  
  - 元数据中未提供完整的依赖图，接入前需手动检查 Pico 固件兼容性、主机驱动（USB‑CDC、Wi‑Fi）以及 Xilinx 工具的 XVC 插件版本。  
  - Wi‑Fi 版目前速率较慢，仅适合低带宽的调试/日志输出，不建议用于大规模批量烧录。  
  - 维护成本：如果项目长期使用，需自行跟进 Pico SDK 更新和 Xilinx 工具链的兼容性。  

**结论**  
kholia/xvc-pico 为前端（硬件调试）提供了低成本、高灵活性的 JTAG 解决方案，能够显著缩短原型开发周期。若在生产环境使用，建议在小批量验证后，建立完善的固件管理和兼容性测试流程，再决定是否正式投入。

## 🧭 Practical evaluation

**Value:** kholia/xvc-pico helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 489 GitHub stars
- 66 forks
- updated 2026-06-27
- primary language: C

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 57/100 |
| topics | 0/100 |
| outlook | 46/100 |
| quality | 49/100 |
| recency | 40/100 |
| adoption | 54/100 |
| production | 49/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/kholia/xvc-pico) · [← Back to Misc](./README.md)</sub>
