# DSheirer/sdrtrunk

[![Stars](https://img.shields.io/github/stars/DSheirer/sdrtrunk?style=flat-square&color=yellow)](https://github.com/DSheirer/sdrtrunk/stargazers) [![Forks](https://img.shields.io/github/forks/DSheirer/sdrtrunk?style=flat-square&color=blue)](https://github.com/DSheirer/sdrtrunk/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> A cross-platform java application for decoding, monitoring, recording and streaming trunked mobile and related radio protocols using Software Defined Radios (SDR).  Website:

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.1k |
| 🍴 **Forks** | 353 |
| 💻 **Language** | Java |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Observability

## 📝 Summary

### English

**Brief summary**  
SDRTrunk is a cross‑platform Java application that uses Software Defined Radios to decode, monitor, record and stream a wide range of trunked mobile and other radio protocols. It is widely used by hobbyists and professionals for spectrum analysis, emergency‑services listening, and radio‑network research.  

**Value proposition**  
Although the project is listed under “Crypto, Database, Observability, Mobile,” its real strength lies in providing an open, fully‑documented reference implementation for handling complex, real‑time radio data streams. For teams building Web3 or blockchain‑based services that need to ingest or verify radio‑derived telemetry (e.g., proof‑of‑location, asset‑tracking, or decentralized emergency‑response networks), SDRTrunk offers a ready‑made pipeline for capturing raw RF data and converting it into structured messages that can be fed into smart contracts or off‑chain analytics.  

**Practical adoption path**  

| Step | Action | Reason |
|------|--------|--------|
| 1. **Evaluate fit** | Clone the repo, run the demo with a supported SDR (e.g., RTL‑SDR, HackRF) and verify that the required protocols (P25, DMR, APCO‑25, etc.) are decoded correctly. | Confirms that the radio environment and protocol set match your use case. |
| 2. **Integrate data export** | Enable the built‑in streaming options (HTTP, WebSocket, MQTT, or custom UDP) to push decoded messages to your blockchain‑ingestion service. | Provides a low‑friction bridge from SDRTrunk to your backend. |
| 3. **Wrap with a service layer** | Containerise the Java app (Docker) and expose a thin API that translates SDRTrunk’s JSON payloads into the format expected by your smart‑contract or off‑chain processor. | Simplifies deployment and isolates the heavy SDR dependencies. |
| 4. **Prototype workflow** | Use the streamed data to simulate blockchain events (e.g., “device X reported location Y at time Z”) and test end‑to‑end handling in a testnet. | Validates the end‑to‑end data path before committing to production. |
| 5. **Hardening & monitoring** | Add health checks, log rotation, and observability (Prometheus metrics, Grafana dashboards) around the Java process and SDR hardware. | Addresses the “Medium” production readiness rating and reduces runtime risk. |
| 6. **Production rollout** | Deploy on dedicated hardware (or cloud‑hosted SDR instances) with redundancy (multiple SDRs, fail‑over scripts) and lock down the Java runtime to a known version. | Ensures reliability for long‑running monitoring or audit‑grade data collection. |

**Production readiness**  
- **Maturity**: 2 k+ stars, 350+ forks, active maintenance (last commit 2026‑07‑13) indicate a healthy community, but the project is primarily a desktop tool, not an out‑of‑the‑box microservice.  
- **Readiness level**: *Medium*. It is solid for prototypes, internal tools, or as a data‑ingestion component, but you must perform due‑diligence on:  
  1. **Hardware dependencies** – ensure compatible SDRs and drivers are available in your environment.  
  2. **Integration effort** – the metadata does not expose a ready‑made API for blockchain use cases; you’ll need to configure streaming/export and possibly write adapters.  
  3. **Operational concerns** – Java process stability, memory usage, and real‑time latency need monitoring and tuning for production workloads.  

In short, SDRTrunk offers a powerful, open‑source radio‑decoding engine that can be repurposed to feed blockchain‑oriented pipelines, but it requires a modest amount of engineering (hardware setup, streaming integration, and operational hardening) before it can be considered production‑ready.

### Русский

DSheerer /sdrtrunk — это кросс‑платформенное Java‑приложение, позволяющее с помощью SDR декодировать, мониторить, записывать и транслировать протоколы trunked‑мобильных и смежных радиосетей; благодаря открытой реализации оно может быть использовано для прототипирования и анализа блокчейн‑интеграций, связанных с Web3‑сервисами (например, проверка передачи данных в децентрализованных приложениях). Типичный сценарий внедрения — внутренний прототип или исследовательский стенд, где инженеры подключают SDR‑приёмник, настраивают нужные протоколы и используют полученные потоки в цепочках Web3‑workflow. Готовность к продакшн — средняя: проект стабилен (2129 звёзд, 353 форка, активные обновления), но требует ручной проверки интеграции и оценки затрат на поддержку перед выводом в боевую эксплуатацию.

### 中文

**项目简介（2‑3 句）**  
DSheirer/sdrtrunk 是一款基于 Java 的跨平台开源工具，能够利用软件定义无线电（SDR）对 trunked 移动通信及相关无线协议进行解码、监控、录音和流媒体推送。它支持多种协议（如 APCO‑25、DMR、P25、TETRA 等），并提供图形化界面和丰富的插件体系，方便用户快速搭建无线电监测与分析环境。

**价值**  
- **快速原型与调试**：提供完整的协议实现和可视化调试信息，帮助安全研究员、业余无线电爱好者以及通信工程师在没有专用硬件的情况下快速验证和实验无线电系统。  
- **数据获取与分析**：能够实时捕获并保存原始 I/Q 数据和解码后的文字/语音流，为后续的信号处理、机器学习或取证分析提供可靠数据源。  
- **跨平台与可扩展**：基于 Java，支持 Windows、macOS、Linux，且插件化设计便于二次开发和集成到更大的监控平台或自动化工作流中。

**典型接入方式**  
1. **本地部署**：下载源码或发行版，安装 JDK（≥11）和对应的 SDR 驱动（如 RTL‑SDR、HackRF、SDRplay），启动 GUI 进行手动配置。  
2. **脚本化/自动化**：利用 `sdrtrunk.jar` 的命令行模式，结合配置文件（JSON/XML）实现批量启动、自动录制和流媒体推送（RTMP/HTTP）。  
3. **系统集成**：通过其 REST‑like 控制接口或直接调用内部 Java API，将解码结果写入数据库、消息队列（Kafka、RabbitMQ）或实时监控平台（Grafana、Prometheus）进行统一管理。  

**生产可用性**  
- **成熟度**：项目已有 2 k+ 星、350+ 分叉，活跃维护至 2026‑07‑13，代码质量和社区支持较好。  
- **准备度**：适合作为内部原型或监控系统的组成部分；在生产环境使用前需要完成以下工作：  
  - **依赖审计**：确认所使用的 SDR 硬件驱动、Java 运行时以及第三方库的许可证和安全补丁。  
  - **性能验证**：在目标硬件上进行负载测试，确保解码、录制和流媒体推送的实时性满足业务需求。  
  - **运维集成**：为关键组件（如录音存储、流媒体服务器）配置监控、日志和自动重启机制。  
- **风险**：项目的集成文档相对分散，部分高级功能（如自定义协议插件）需要自行阅读源码或社区讨论后实现；因此在正式投产前建议进行一次完整的 PoC 验证。  

总体而言，sdrtrunk 在需要快速获取、解码和处理 SDR 数据的场景下具备很高的性价比，只要做好前期的依赖审查和性能调优，即可在内部生产环境中稳定运行。

## 🧭 Practical evaluation

**Value:** DSheirer/sdrtrunk helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2129 GitHub stars
- 353 forks
- updated 2026-07-13
- primary language: Java

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 71/100 |
| topics | 0/100 |
| outlook | 53/100 |
| quality | 56/100 |
| recency | 40/100 |
| adoption | 69/100 |
| production | 51/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/DSheirer/sdrtrunk) · [← Back to Observability](./README.md)</sub>
