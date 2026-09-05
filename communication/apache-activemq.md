# apache/activemq

[![Stars](https://img.shields.io/github/stars/apache/activemq?style=flat-square&color=yellow)](https://github.com/apache/activemq/stargazers) [![Forks](https://img.shields.io/github/forks/apache/activemq?style=flat-square&color=blue)](https://github.com/apache/activemq/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Apache ActiveMQ

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.4k |
| 🍴 **Forks** | 1.5k |
| 💻 **Language** | Java |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`activemq` `amqp` `amqps` `apache` `broker` `java` `jms` `messaging` `mqtt` `openwire` `stomp`

## 🎯 Categories

Communication

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Apache ActiveMQ is a mature, Java‑based open‑source message broker that provides reliable, asynchronous communication between distributed applications. With over 2,400 stars, 1,500 forks, and recent commits, it is a well‑maintained candidate for projects that need a proven messaging layer. A small proof‑of‑concept that follows the README can quickly verify that its APIs and configuration fit your workflow before scaling to production.

**Value**  
ActiveMQ offers a full‑featured JMS implementation, support for multiple protocols (AMQP, MQTT, STOMP, OpenWire), and built‑in clustering and high‑availability options, making it suitable for both microservice architectures and legacy enterprise systems. Its extensive ecosystem (client libraries, Spring integration, monitoring tools) reduces the need to build custom messaging infrastructure.

**Practical Adoption Path**  
1. **Proof of Concept** – Clone the repo, run the provided Docker image or the default broker, and send/receive a test message using the sample Java client.  
2. **Integration Check** – Review the README and configuration files to map required features (e.g., persistence, security, clustering) to your environment; adjust `activemq.xml` accordingly.  
3. **Pilot Deployment** – Deploy the broker in a staging environment (Docker/Kubernetes), enable persistence (KahaDB or external DB), and integrate with your application’s messaging layer (JMS, Spring JMS, or any supported protocol).  
4. **Scale & Harden** – Add network of brokers, configure master‑slave or replicated stores, and set up monitoring (JMX, Prometheus exporters) before moving to production.

**Production Readiness**  
ActiveMQ scores high on production readiness: it is actively maintained (last commit 2026‑06‑23), widely adopted in enterprise projects, and backed by the Apache Foundation. The large user base and mature tooling provide confidence for a serious pilot, though the integration steps are not fully documented in the metadata, so a modest upfront effort is needed to validate configuration, security, and operational overhead. Once the proof of concept validates the setup cost, the broker can be considered production‑grade for most messaging workloads.

### Русский

Apache ActiveMQ — это зрелый Java‑ориентированный брокер сообщений с поддержкой многочисленных протоколов (JMS, AMQP, MQTT и др.), который подходит для построения надёжных систем обмена данными между микросервисами, приложениями и IoT‑устройствами. Благодаря активному развитию (обновления до 2026 г., более 2400 звёзд и 1500 форков) и широкой экосистеме, проект готов к production‑использованию, однако рекомендуется начать с небольшого proof‑of‑concept и проверить детали установки по README, чтобы уточнить интеграционные затраты.

### 中文

**项目简介（2‑3 句）**  
Apache ActiveMQ 是一款成熟的开源消息中间件，基于 Java 实现，提供 JMS、AMQP、STOMP、MQTT 等多协议支持，适用于企业级的异步通信、事件驱动和微服务解耦场景。凭借活跃的社区、持续更新以及在金融、电商等行业的广泛采用，已成为企业级消息传递的可靠选项。

**价值**  
- **多协议兼容**：一次部署即可同时提供 JMS、AMQP、STOMP、MQTT 等多种协议，满足不同系统的接入需求。  
- **高可靠性**：支持持久化、事务、消息回溯、死信队列和集群 HA，确保关键业务数据不丢失。  
- **生态丰富**：与 Spring、Spring Boot、Camel、Kafka Connect 等主流框架深度集成，降低开发和运维成本。  

**典型接入方式**  
1. **直接使用 JMS API**（Java 项目）  
   ```java
   ConnectionFactory cf = new ActiveMQConnectionFactory("tcp://broker-host:61616");
   Connection conn = cf.createConnection();
   Session session = conn.createSession(false, Session.AUTO_ACKNOWLEDGE);
   Destination queue = session.createQueue("example.queue");
   MessageProducer producer = session.createProducer(queue);
   TextMessage msg = session.createTextMessage("Hello ActiveMQ");
   producer.send(msg);
   ```
2. **Spring Boot Starter**（推荐）  
   - 在 `pom.xml` 中加入 `spring-boot-starter-activemq`。  
   - 在 `application.yml` 配置 broker URL、用户名密码等。  
   - 使用 `JmsTemplate` 发送/接收消息，Spring 自动管理连接和事务。  
3. **容器化部署**  
   - 官方提供 Docker 镜像 `apache/activemq`，可直接在 Kubernetes 中以 Deployment/StatefulSet 方式运行。  
   - 通过 Helm Chart（社区维护）实现快速集群化部署，配合 PersistentVolume 保障持久化。  

**生产可用性**  
- **成熟度**：项目活跃（最近一次提交 2026‑06‑23），GitHub ★2439、Fork ★1488，拥有完整的文档、示例和社区支持。  
- **可靠性**：支持持久化存储、主从复制、网络分区容错以及消息事务，已在金融、电商等高并发场景验证。  
- **运维**：提供 JMX、Web Console、Prometheus Exporter 等监控手段，便于指标收集和告警。  
- **风险**：虽然功能完整，但首次集成时需要评估网络拓扑、持久化存储方案以及与现有系统的协议匹配度，建议先在测试环境完成 PoC，确认连接配置、性能基准和运维流程后再投入生产。  

综上，Apache ActiveMQ 具备高可靠性、丰富的协议与框架集成能力，适合在需要可靠异步通信的企业级系统中快速落地，经过适当的 PoC 验证后即可进入生产环境使用。

## 🧭 Practical evaluation

**Value:** apache/activemq may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2439 GitHub stars
- 1488 forks
- updated 2026-06-23
- primary language: Java
- 11 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 79/100 |
| stars | 72/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 83/100 |
| recency | 80/100 |
| adoption | 74/100 |
| production | 71/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/apache/activemq) · [← Back to Communication](./README.md)</sub>
