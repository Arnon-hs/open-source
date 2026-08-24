# kroxylicious/kroxylicious

[![Stars](https://img.shields.io/github/stars/kroxylicious/kroxylicious?style=flat-square&color=yellow)](https://github.com/kroxylicious/kroxylicious/stargazers) [![Forks](https://img.shields.io/github/forks/kroxylicious/kroxylicious?style=flat-square&color=blue)](https://github.com/kroxylicious/kroxylicious/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-46%2F100-brightgreen?style=flat-square)](#)

> Kroxylicious, the snappy open source proxy for Apache Kafka®

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 288 |
| 🍴 **Forks** | 111 |
| 💻 **Language** | Java |
| 📈 **Score** | 46/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apache-kafka` `java` `kafka` `proxy`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Kroxylicious is an open‑source, high‑performance proxy for Apache Kafka written in Java. It sits between Kafka clients and brokers, allowing you to inject custom logic (e.g., protocol translation, request filtering, or testing hooks) without modifying the broker itself. With a modest star count (≈ 300) and recent activity, it is positioned as a developer‑focused tool for prototyping and internal workflows.

**Value Proposition**  
- **Flexibility:** By externalising cross‑cutting concerns (metrics, security, testing, protocol upgrades) into a proxy layer, teams can evolve client‑side behavior without touching the Kafka cluster.  
- **Speed of Experimentation:** The “snappy” design means low latency overhead, making it suitable for rapid proof‑of‑concepts, CI pipelines, or temporary test environments.  
- **Language Compatibility:** Being Java‑based, it integrates naturally with existing Kafka client libraries and can be packaged alongside other JVM services.

**Practical Adoption Path**  
1. **Read the README & Quick‑Start** – Verify that the provided Docker image or binary matches your deployment model (Kubernetes, bare‑metal, etc.).  
2. **Proof‑of‑Concept (PoC)** – Deploy Kroxylicious in a sandbox cluster, point a single test client at the proxy, and confirm basic request/response flow.  
3. **Feature Validation** – Implement the specific interceptor or filter you need (e.g., request logging, header injection) and run integration tests.  
4. **Incremental Rollout** – Route a subset of production traffic through the proxy using a load‑balancer or DNS split, monitor latency and error rates, and iterate.  

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑06‑29) and has a modest community (≈ 300 ★, 100 forks), but it lacks the extensive ecosystem and long‑term stability guarantees of more mature Kafka tooling.  
- **Risk Areas:** Integration steps are not fully documented; you’ll need to invest time in understanding the interceptor API and ensuring compatibility with your Kafka version. Dependency management (Java runtime, logging frameworks) should be audited.  
- **Recommendation:** Suitable for prototypes, internal tooling, or environments where you can afford a controlled rollout and monitor the proxy’s impact. For mission‑critical production workloads, perform a thorough PoC, add health‑checks, and consider fallback paths (direct broker access) before full adoption.

### Русский

Kroxylicious — это лёгкий open‑source прокси для Apache Kafka, который упрощает доступ к топикам и позволяет быстро подключать клиентские приложения без изменения их кода. Типовой сценарий внедрения — развертывание прокси в качестве промежуточного слоя между существующими сервисами и кластером Kafka для тестирования, внутренних workflow‑ов или прототипов. Проект пока имеет среднюю готовность к production (подходит для пилотов и внутренних задач, но требует проверки зависимостей и небольшого PoC перед полноценным использованием в продакшене).

### 中文

Kroxylicious 是一个基于 Java 的轻量级 Apache Kafka 代理，能够快速拦截、转发和监控 Kafka 流量，适用于需要在不修改应用代码的情况下进行协议调试、流量治理或安全审计的场景。典型的接入方式是先阅读项目的 README，搭建一个小规模的证明概念（PoC）来验证其配置和依赖，随后再逐步扩展到实际工作流中。虽然目前有 288 颗星和活跃的更新记录，但其生产可用性仅处于中等水平，建议在正式投入生产前

## 🧭 Practical evaluation

**Value:** kroxylicious/kroxylicious may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 288 GitHub stars
- 111 forks
- updated 2026-06-29
- primary language: Java
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 52/100 |
| topics | 50/100 |
| outlook | 50/100 |
| quality | 56/100 |
| recency | 40/100 |
| adoption | 52/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/kroxylicious/kroxylicious) · [← Back to Misc](./README.md)</sub>
