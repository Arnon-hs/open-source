# apache/plc4x

[![Stars](https://img.shields.io/github/stars/apache/plc4x?style=flat-square&color=yellow)](https://github.com/apache/plc4x/stargazers) [![Forks](https://img.shields.io/github/forks/apache/plc4x?style=flat-square&color=blue)](https://github.com/apache/plc4x/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> PLC4X The Industrial IoT adapter

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.6k |
| 🍴 **Forks** | 484 |
| 💻 **Language** | Java |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ab` `ads` `bacnet` `c` `can` `cpp` `ethernetip` `firmata` `go` `iot` `java` `knx`

## 🎯 Categories

Marketing

## 📝 Summary

### English

**Summary**  
Apache PLC4X is an open‑source Industrial IoT adapter that provides a unified, protocol‑agnostic API for communicating with a wide range of PLCs and field devices. With over 1.6 k stars, active commits (last updated 2026‑06‑29), and a Java‑centric codebase, it is mature enough for a serious pilot but still warrants a short proof‑of‑concept to verify fit with your specific workflow.

**Value**  
PLC4X abstracts the myriad native PLC protocols (e.g., Modbus, OPC UA, S7, EtherNet/IP) behind a single, type‑safe API, dramatically reducing the amount of custom driver code developers must write and simplifying integration into existing Java, Go, C# or Node.js services.

**Practical adoption path**  
1. **Read the README & quick‑start guides** to spin up a minimal PLC4X client against a test PLC or a simulator.  
2. **Run a proof‑of‑concept** that exercises the required protocol(s) and validates latency, error handling, and data mapping for your use case.  
3. **Integrate** the generated driver code into your application stack, leveraging the provided Maven/Gradle artifacts and optional code‑generation tooling.  
4. **Extend** or contribute custom protocol support if needed, following the project's contribution guidelines.

**Production readiness**  
The project shows strong production signals: recent releases, a healthy fork/star count, multiple language bindings, and adoption in several Apache and commercial IoT solutions. While the license (Apache 2.0) and security posture appear sound, a final review of maintainers’ activity and any disclosed CVEs is recommended before committing to a full‑scale deployment.

### Русский

Apache PLC4X — это открытый адаптер для Industrial IoT, позволяющий унифицировать доступ к широкому спектру программируемых логических контроллеров (PLC) через единый API на Java (и других языках). Типичный сценарий внедрения — небольшое proof‑of‑concept, в котором из README берётся пример подключения к конкретному типу PLC, после чего система масштабируется до полноценного сбора и обработки данных в производственной среде. По уровню готовности проект считается «production‑ready»: активные коммиты, более 1600 звёзд, сотни форков и стабильный релизный цикл, что делает его надёжным кандидатом для пилотных и коммерческих проектов.

### 中文

**项目简介（2‑3 句）**  
Apache PLC4X 是 Apache 基金会的开源工业物联网适配器，提供统一的 API 将 PLC（可编程逻辑控制器）以及其他工业现场设备无缝连接到 Java、C#、Python 等主流语言的应用中。它支持多种工业协议（如 Modbus、OPC UA、S7、BACnet 等），帮助开发者快速构建跨厂区的 IoT 数据采集与控制系统。

**价值**  
- **统一协议层**：一次开发即可访问数十种工业协议，避免为每种设备单独编写驱动。  
- **跨语言、跨平台**：提供 Java、C#、Python、Go 等多语言 SDK，适配云端、边缘和本地部署。  
- **开源且活跃**：拥有 1.6k+ Stars、近 500 Fork，社区和 Apache 基金会双重保障，适合长期维护的工业项目。

**典型接入方式**  
1. **选定协议**：在 `plc4j`（Java）或对应语言的子项目中引用对应协议的驱动（如 `plc4j-driver-modbus`）。  
2. **创建连接**：使用统一的 `PlcConnection` 接口，传入协议 URI（例如 `modbus:tcp://192.168.0.10:502`）。  
3. **读写数据**：通过 `PlcReadRequest` / `PlcWriteRequest` 构造查询或控制指令，返回的 `PlcReadResponse` / `PlcWriteResponse` 提供强类型的结果。  
4. **集成到业务**：将读取到的实时数据推送至 Kafka、Prometheus、InfluxDB 等后端，或在边缘网关上直接执行控制逻辑。

**生产可用性**  
- **活跃维护**：截至 2026‑06‑29 最近一次提交，社区活跃，且已通过 Apache 顶级项目审查。  
- **成熟生态**：多家工业自动化厂商和云平台已在内部或公开项目中使用 PLC4X，具备实际生产案例。  
- **安全与合规**：采用 Apache 2.0 许可证，代码审计和 CVE 监控在 Apache 基金会统一管理下，风险可控。  
- **推荐实践**：在正式投产前，先在测试环境完成协议兼容性验证和小规模 POC；随后在预生产环境进行高可用部署（如多实例负载均衡）并监控连接健康状态。

综上，Apache PLC4X 具备统一协议、跨语言、活跃社区等优势，是工业 IoT 项目实现设备接入的可靠 OSS 选型。

## 🧭 Practical evaluation

**Value:** apache/plc4x may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1610 GitHub stars
- 484 forks
- updated 2026-06-29
- primary language: Java
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 67/100 |
| stars | 68/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 71/100 |
| recency | 40/100 |
| adoption | 68/100 |
| production | 61/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/apache/plc4x) · [← Back to Marketing](./README.md)</sub>
