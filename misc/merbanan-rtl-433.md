# merbanan/rtl_433

[![Stars](https://img.shields.io/github/stars/merbanan/rtl_433?style=flat-square&color=yellow)](https://github.com/merbanan/rtl_433/stargazers) [![Forks](https://img.shields.io/github/forks/merbanan/rtl_433?style=flat-square&color=blue)](https://github.com/merbanan/rtl_433/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Program to decode radio transmissions from devices on the ISM bands (and other frequencies)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 7.5k |
| 🍴 **Forks** | 1.5k |
| 💻 **Language** | C |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`433mhz` `rf` `rtl-sdr` `sdr` `sensors` `signal-processing`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
`rtl_433` is an open‑source C program that demodulates and decodes a wide variety of radio signals transmitted by consumer sensors and devices on ISM and other frequencies, turning raw RF data into readable JSON or CSV. With more than 7 500 GitHub stars, active maintenance (last commit 2026‑07‑06) and a large fork base, it is a mature, community‑driven toolkit for building low‑cost, software‑defined radio (SDR) monitoring solutions.

**Value**  
- **Broad device support** – out‑of‑the‑box decoders for weather stations, power meters, garage door controllers, and many other cheap IoT sensors, eliminating the need to write custom demodulators.  
- **Lightweight, language‑agnostic output** – JSON/CSV streams can be piped directly into home‑automation platforms (Home Assistant, Node‑RED), time‑series databases, or cloud services.  
- **Cost‑effective hardware** – works with inexpensive RTL‑SDR dongles, enabling large‑scale deployments at a fraction of commercial gateway prices.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, connect an RTL‑SDR dongle, and run `rtl_433 -R 0` to verify that nearby devices are being detected.  
2. **Validate against the README** – Follow the documented steps for installing dependencies (libusb, libtool, etc.) and for configuring output plugins (MQTT, InfluxDB, etc.).  
3. **Integrate** – Wrap the binary in a Docker container or systemd service, configure the desired output format, and connect it to the target automation or analytics pipeline.  
4. **Scale** – Deploy additional dongles on edge nodes, using the same container image; centralize data ingestion with a message broker or time‑series DB.

**Production readiness**  
The project scores high on production criteria: recent commits, a vibrant fork community, extensive real‑world usage, and mature C codebase. While the integration steps are not fully described in the metadata, the comprehensive README and abundant community examples make the setup cost predictable. Starting with a small pilot (one dongle feeding a test MQTT topic) is advisable; once the pipeline is validated, the solution can be rolled out to production with confidence.

### Русский

**merbanan/rtl_433** — это открытый C‑инструмент, который принимает сигналы с радиочастотных приёмников RTL‑SDR и декодирует данные от широкого спектра датчиков и устройств в ISM‑диапазонах (например, погодные станции, датчики движения, умный дом). Типичное внедрение — подключить RTL‑SDR к серверу/контейнеру, запустить rtl_433 с нужными параметрами и направить полученные JSON‑сообщения в систему мониторинга, брокер MQTT или базу данных; такой PoC занимает несколько минут и позволяет быстро собрать телеметрию от существующего оборудования. По метрикам активности (7549 звёзд, 1536 форков, последние коммиты — июль 2026) проект считается готовым к продакшн‑использованию, однако перед масштабным rollout стоит проверить совместимость конкретных приёмников и настроить процесс автоматической сборки/развёртывания.

### 中文

**项目简介（2‑3 句）**  
`merbanan/rtl_433` 是一款开源 C 程序，能够使用 RTL‑SDR（或其他兼容的 SDR）接收并解码 ISM 频段以及其他频率上常见的无线传感器、遥控器等设备的无线电报文，输出结构化的 JSON/CSV 等格式，便于后续数据聚合和可视化。

**价值**  
- **低成本物联网数据采集**：利用廉价的 USB RTL‑SDR（约 20 USD）即可捕获多种厂商的温湿度、功率、门磁、气象站等传感器数据，省去专有网关费用。  
- **协议兼容广**：内置数百种已实现的协议（Acurite、Ecowitt、Fine Offset、Xiaomi、RF‑Code 等），并提供插件式解析框架，能够快速适配新设备。  
- **可直接对接主流平台**：支持 MQTT、InfluxDB、Home Assistant、Node‑RED 等常用后端，方便在监控、自动化或大数据平台上使用。

**典型接入方式**  
1. **硬件准备**：在服务器或边缘节点上插入 RTL‑SDR 接收器（或兼容的 HackRF、Airspy 等）。  
2. **软件部署**：  
   - 使用系统包管理器或源码编译 `rtl_433`（`apt install rtl-433` / `make && sudo make install`）。  
   - 编写或使用已有的配置文件（`-C <config>.conf`），指定要监听的频段、协议过滤以及输出方式（如 `-F json -M utc -M protocol`）。  
3. **数据输出**：  
   - **本地文件**：`-F csv:output.csv`、`-F json:output.json`。  
   - **实时流**：`-F mqtt://broker:1883,topic=rtl_433`、`-F influxdb://host/db`、`-F syslog`。  
   - **集成**：在 Home Assistant 中添加 `mqtt` 传感器或在 Node‑RED 中使用 `mqtt in` 节点消费数据。  
4. **监控与管理**：通过 systemd 服务或 Docker 容器运行 `rtl_433`，并结合 Prometheus exporter（`rtl_433 -F prometheus`）实现运行状态监控。

**生产可用性**  
- **活跃度**：截至 2026‑07‑06，项目仍在持续更新，拥有 7 549 星、1 536 Fork，社区贡献活跃。  
- **成熟度**：核心功能已在众多开源家庭自动化、气象站和工业监控项目中验证，错误率低，支持多平台（Linux、macOS、Windows）。  
- **部署成熟度**：官方提供 Docker 镜像、systemd 示例以及完整的 MQTT/InfluxDB 集成指南，适合直接在生产环境中以容器或守护进程方式运行。  
- **风险**：集成路径主要取决于目标数据流（MQTT、数据库等），需要在部署前确认硬件天线布局、频段许可以及本地无线干扰情况；但整体技术门槛低，验证成本可通过一个小规模的 PoC（如捕获单个温湿度传感器）快速完成。

**结论**：`rtl_433` 具备高性价比的无线数据采集能力，集成方式成熟且文档齐全，完全可以在生产环境中作为可靠的 ISM 频段数据入口，建议先在测试环境跑通 MQTT/InfluxDB 输出后，再推广至全链路监控与自动化系统。

## 🧭 Practical evaluation

**Value:** merbanan/rtl_433 may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 7549 GitHub stars
- 1536 forks
- updated 2026-07-06
- primary language: C
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 80/100 |
| stars | 83/100 |
| topics | 75/100 |
| outlook | 60/100 |
| quality | 73/100 |
| recency | 40/100 |
| adoption | 82/100 |
| production | 57/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/merbanan/rtl_433) · [← Back to Misc](./README.md)</sub>
