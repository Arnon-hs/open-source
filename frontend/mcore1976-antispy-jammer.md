# mcore1976/antispy-jammer

[![Stars](https://img.shields.io/github/stars/mcore1976/antispy-jammer?style=flat-square&color=yellow)](https://github.com/mcore1976/antispy-jammer/stargazers) [![Forks](https://img.shields.io/github/forks/mcore1976/antispy-jammer?style=flat-square&color=blue)](https://github.com/mcore1976/antispy-jammer/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Simplest ultrasonic ANTISPY voice recording jammer based on ARDUINO module with PWM (optionally AD8933 signal generator) with output MOSFET stage (or  H-bridge+MOSFETs)  driving piezo ultrasonic transducers + coils

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 413 |
| 🍴 **Forks** | 71 |
| 💻 **Language** | C++ |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-07-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`25khz` `ad8933` `ad9833` `arduino` `attiny13` `attiny85` `digispark` `ir2103` `ir2104` `jammer` `microphone-jammer` `pam8403`

## 🎯 Categories

Frontend

## 📝 Summary

### English

**Project Summary:**

The mcore1976/antispy-jammer is an open-source project that provides a simple ultrasonic voice recording jammer based on an Arduino module. This project is useful for building product UI faster, reusing interface components, and improving frontend delivery. It is primarily written in C++ and has a moderate level of production readiness.

**Value:**

The mcore1976/antispy-jammer project offers several values, including:

1. **Faster product UI development**: By providing a simple and reusable UI component, developers can quickly integrate the jammer into their product.
2. **Improved frontend delivery**: The project's modular design allows for easy integration and customization of the UI component.

**Practical Adoption Path:**

To adopt this project, follow these steps:

1. **Evaluate the project**: Review the project's README, GitHub stars, and forks to understand its popularity and community support.
2. **Build a small proof of concept**: Create a simple prototype to test the project's functionality and integration with your product.
3. **Validate setup cost**: Assess the time and resources required to set up and maintain the project.
4. **Integrate with your product**: Once you have validated the project's feasibility, integrate it with your product's UI.

### Русский

**mcore1976/antispy-jammer** — это простейший ультразвуковой глушитель записи голоса, реализованный на Arduino с ШИМ‑выходом (опционально генератором AD8933) и MOSFET‑усилителем (или H‑мостом) для привода ультразвуковых пьезо‑трансдьюсеров и катушек. Проект позволяет быстро собрать прототип устройства защиты от подслушивания, используя готовые аппаратные блоки и открытый код, что ускоряет разработку пользовательского интерфейса и интеграцию в небольшие системы. Готовность к production — средняя: подходит для прототипов и внутренних процессов, но требует проверки зависимостей, настройки аппаратуры и небольшого proof‑of‑concept перед масштабным внедрением.

### 中文

**项目价值**  
- **硬件防窃听利器**：通过 Arduino PWM（或 AD8933）驱动 MOSFET/H‑bridge，产生超声波信号干扰窃听麦克风，实现最简易的“声波防窃听”功能。  
- **成本低、实现快**：仅需普通 Arduino 开发板、功率 MOSFET 与压电或线圈式超声换能器，几块元件即可搭建原型，适合安全实验、教学演示或小批量产品。  
- **开源可定制**：代码全部公开，硬件原理图、PCB（若有）和调参脚本均可自行修改，满足不同频段、功率或驱动方式的特定需求。

**典型接入方式**  
1. **硬件准备**  
   - Arduino（UNO、Mega、Nano 等均可）  
   - PWM 输出端接 MOSFET（或 H‑bridge）驱动压电/线圈式超声换能器  
   - 可选：AD8933 作为更精确的信号源  
2. **软件集成**  
   - 克隆仓库 `git clone https://github.com/mcore1976/antispy-jammer.git`  
   - 使用 Arduino IDE 打开 `antispy_jammer.ino`（或对应的 .cpp/.h），根据实际硬件更改 PWM 引脚、频率、占空比等参数。  
   - 编译并烧录到 Arduino。  
3. **验证与调试**  
   - 通过示波器或声谱仪确认输出频率在 20 kHz 以上且功率足以覆盖目标麦克风的灵敏度范围。  
   - 根据实际环境（房间大小、目标设备距离）微调占空比或使用多路 MOSFET 并联提升功率。  

**生产可用性评估**  
| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | ★★☆☆☆（中等） | 项目已有 413 星、71 Fork，代码更新至 2026‑07‑12，功能基本完整，但缺少正式的硬件 BOM、生产测试报告和认证文档。 |
| **集成难度** | 中等 | 需要自行搭建电路板并调试 PWM/功率驱动，文档仅提供基础示例，建议先做小规模原型验证。 |
| **可靠性** | ★★☆☆☆ | 超声干扰效果受环境、换能器质量和目标麦克风特性影响大，需在目标使用场景中进行充分实验。 |
| **维护成本** | 中等 | 代码基于 Arduino C++，社区活跃度一般，后续可能需要自行适配新 MCU 或更高功率驱动方案。 |
| **适用场景** | 原型、内部安全工具、教学演示、低批量防窃听产品 | 不建议直接用于大规模商业出货，除非完成硬件可靠性、EMC、法规（如 FCC/CE）等合规认证。 |

**结论**  
`antispy-jammer` 是一个成本低、实现快速的超声波防窃听原型平台，适合安全研究、内部工具或小批量产品的快速验证。若要在生产环境中使用，建议：  

1. **做小规模 PoC**：先在实验室验证干扰效果与安全性。  
2. **完善硬件 BOM 与 PCB**：加入过流、过热保护，确保长期运行可靠。  
3. **进行合规测试**：确认超声输出符合当地电磁兼容和声学安全标准。  

完成以上步骤后，可将其作为防窃听模块嵌入更大的安全系统或产品中。

## 🧭 Practical evaluation

**Value:** mcore1976/antispy-jammer helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 413 GitHub stars
- 71 forks
- updated 2026-07-12
- primary language: C++
- 20 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 79/100 |
| recency | 100/100 |
| adoption | 53/100 |
| production | 74/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/mcore1976/antispy-jammer) · [← Back to Frontend](./README.md)</sub>
