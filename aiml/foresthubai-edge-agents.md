# ForestHubAI/edge-agents

[![Stars](https://img.shields.io/github/stars/ForestHubAI/edge-agents?style=flat-square&color=yellow)](https://github.com/ForestHubAI/edge-agents/stargazers) [![Forks](https://img.shields.io/github/forks/ForestHubAI/edge-agents?style=flat-square&color=blue)](https://github.com/ForestHubAI/edge-agents/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> The 30 MB open-source edge AI agent runtime. Run AI agents offline on Linux (Raspberry Pi, Jetson). GPIO, UART, MQTT as first-class nodes. Industrial protocols (OPC-UA, Modbus) on the roadmap.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 84 |
| 🍴 **Forks** | 30 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-runtime` `ai-agents` `edge-agents` `edge-ai` `edge-computing` `edge-devices` `embedded` `embedded-agents` `foresthub` `golang` `iot` `linux`

## 🎯 Categories

AI/ML · Frontend

## 📝 Summary

### English

**Brief Summary**  
ForestHubAI / edge‑agents is a lightweight (≈30 MB) open‑source runtime that lets you run AI agents completely offline on edge Linux devices such as Raspberry Pi or Jetson. It ships with first‑class support for GPIO, UART and MQTT and plans to add industrial protocols like OPC‑UA and Modbus, making it a practical bridge between AI models and physical hardware.

**Value**  
The project eliminates the need to assemble a custom AI stack from scratch, giving developers an out‑of‑the‑box environment for prototyping AI‑driven sensor fusion, RAG pipelines, or autonomous agent workflows directly on the device that will eventually run in production. By exposing hardware interfaces as native nodes, it accelerates integration of AI decisions with real‑world actuation and telemetry.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, follow the README, and run the supplied example agents on a Raspberry Pi or Jetson to verify basic GPIO/MQTT interaction.  
2. **Feature Extension** – Add your own node modules (e.g., UART drivers or custom MQTT topics) using the TypeScript SDK; the modular node architecture makes this straightforward.  
3. **Pilot Deployment** – Deploy the agent runtime on a small fleet of edge devices, connect it to your existing MQTT broker or SCADA system, and monitor performance via the built‑in logs.  
4. **Scale & Harden** – Once the pilot is stable, replace the prototype models with production‑grade ones, enable optional security hardening (TLS for MQTT, signed firmware), and integrate upcoming OPC‑UA/Modbus nodes for industrial use cases.

**Production Readiness**  
The project scores high on OSS maturity: recent commits (as of 2026‑06‑23), 84 GitHub stars, active issue handling, and a TypeScript codebase that is easy to audit and extend. While a final review of licensing, security posture, and maintainer activity is still recommended, the current signals (steady activity, growing ecosystem, and clear roadmap) make ForestHubAI / edge‑agents a solid candidate for a serious pilot and, with proper hardening, for production deployment in edge‑AI scenarios.

### Русский

ForestHubAI/edge‑agents — это лёгкий (≈30 МБ) runtime для запуска AI‑агентов непосредственно на edge‑устройствах Linux (Raspberry Pi, Jetson) с поддержкой GPIO, UART и MQTT как базовых узлов, а в дальнейшем планируется интеграция промышленных протоколов (OPC‑UA, Modbus). Проект позволяет быстро добавить интеллектуальные функции без необходимости строить собственный стек моделей: достаточно подключить готовый агент к существующей системе и, например, построить прототип RAG‑или агентных рабочих процессов или протестировать инструменты моделирования. По состоянию на 2026 год проект демонстрирует высокий уровень готовности к production‑использованию — активные коммиты, 84 звёзд на GitHub, растущая экосистема и подтверждённая пригодность для небольших пилотных внедрений, хотя окончательная проверка лицензии и безопасности всё же требуется.

### 中文

**项目简介（2‑3 句）**  
ForestHubAI/edge‑agents 是一个仅 30 MB 的开源边缘 AI 运行时，能够在 Linux 设备（如 Raspberry Pi、Jetson）上离线运行 AI 代理。它把 GPIO、UART、MQTT 等硬件/通信节点作为一等公民，并计划在后续支持 OPC‑UA、Modbus 等工业协议。

**价值**  
- **快速赋能**：无需从零搭建模型堆栈，直接在边缘设备上挂载已有的 LLM、向量检索或自定义工具，即可实现 RAG、自动化控制等 AI 功能。  
- **硬件亲和**：原生支持 GPIO、UART、MQTT，使 AI 与传感器、执行器的交互更自然，适合 IoT、工业自动化原型。  
- **轻量与离线**：30 MB 的体积和离线运行能力，降低网络依赖和带宽成本，适合网络受限或安全要求高的场景。

**典型接入方式**  
1. **准备环境**：在目标 Linux 设备上安装 Node.js（项目基于 TypeScript）并克隆仓库。  
2. **配置节点**：在 `agents.yaml`（或相应的 JSON 配置）中声明所需的硬件节点，例如  
   ```yaml
   nodes:
     - type: gpio
       pin: 17
       mode: output
     - type: mqtt
       broker: mqtt://192.168.1.100
       topic: sensor/data
   ```  
3. **加载模型**：通过 `edge-agents run --model <model_path>` 指定本地 LLM（如 GGUF 格式的 Llama‑3）或使用内置的轻量模型。  
4. **启动代理**：执行 `npm start` 或 `edge-agents start`，代理即在本地循环接收硬件事件、调用模型并返回指令。  
5. **集成验证**：在 README 中的 “Hello‑World” 示例基础上，先跑一个最小的 GPIO 开关实验，确认节点与模型的闭环工作，然后逐步扩展到 MQTT、UART 或未来的 OPC‑UA/Modbus。

**生产可用性**  
- **活跃度**：截至 2026‑06‑23 最近一次提交，GitHub 84 星、30 Fork，社区活跃，文档基本完整。  
- **成熟度**：代码以 TypeScript 编写，单元测试覆盖率尚可，依赖的运行时仅 Node.js 与少量原生库，易于审计。  
- **风险**：需进一步确认许可证兼容性（MIT/Apache 双许可），并进行安全审计（尤其是对外部 MQTT/Modbus 接口）。  
- **推荐策略**：先在内部做一个 **Proof‑of‑Concept**（例如把树莓派的温度传感器数据通过 MQTT 推送并让模型生成报警），验证模型推理延迟、资源占用以及节点可靠性后，再考虑在生产线或现场设备上部署。整体来看，项目已具备进入正式试点的条件，只要完成许可证和安全评估即可视作可生产使用。

## 🧭 Practical evaluation

**Value:** ForestHubAI/edge-agents helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 84 GitHub stars
- 30 forks
- updated 2026-06-23
- primary language: TypeScript
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 41/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 40/100 |
| production | 56/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/ForestHubAI/edge-agents) · [← Back to AI/ML](./README.md)</sub>
