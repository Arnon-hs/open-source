# dapr/java-sdk

[![Stars](https://img.shields.io/github/stars/dapr/java-sdk?style=flat-square&color=yellow)](https://github.com/dapr/java-sdk/stargazers) [![Forks](https://img.shields.io/github/forks/dapr/java-sdk?style=flat-square&color=blue)](https://github.com/dapr/java-sdk/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Dapr SDK for Java

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 298 |
| 🍴 **Forks** | 227 |
| 💻 **Language** | Java |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Libraries & SDKs

## 📝 Summary

### English

**Project Summary:**

The Dapr Java SDK is an open-source project that provides a Java implementation for the Distributed Application Runtime (Dapr). It enables developers to build cloud-native applications with ease, leveraging Dapr's features such as state management, pub-sub messaging, and service invocation.

**Value:**

The value proposition of the Dapr Java SDK lies in its ability to simplify the development of cloud-native applications. It provides a concrete workflow for developers to integrate Dapr's features into their Java applications, making it a useful tool for those who need to build scalable and fault-tolerant systems.

**Practical Adoption Path:**

For practical adoption, it is recommended to start with a small proof of concept to evaluate the feasibility of integrating the Dapr Java SDK into your project. Before production, it is essential to perform dependency and maintenance checks to ensure the stability and security of the SDK. This will involve reviewing the README, checking the activity, and verifying the security posture and active maintainers of the project.

**Production Readiness:**

The production readiness of the Dapr Java SDK is rated as medium. It is suitable for prototypes or internal workflows, where the risks associated with its adoption can be mitigated. However, before deploying it in production, it is crucial to perform thorough checks

### Русский

Резюме проекта dapr/java-sdk:

Данный проект представляет собой Java-SDK для Dapr, который может быть полезен при конкретном рабочем процессе, если его README и активность соответствуют этому процессу. Он подходит для прототипирования или внутренних рабочих процессов, но требует проверки зависимостей и обслуживания перед внедрением в производство. Проект готов примерно на средний уровень, что позволяет использовать его в небольших проектах или прототипах.

### 中文

**项目简介**  
`dapr/java-sdk` 是 Dapr（Distributed Application Runtime）的官方 Java 客户端库，提供了对 Dapr 各种 building‑block（状态管理、发布/订阅、绑定、服务调用、密钥/机密等）的简洁、类型安全的 Java 接口，帮助开发者在不关心底层实现细节的前提下快速构建微服务应用。

**价值**  
- **统一抽象**：一次性封装 Dapr 的全部功能，避免在业务代码中硬编码 HTTP/gRPC 调用。  
- **语言友好**：基于 Java 8+，使用 Maven/Gradle 即可引入，符合企业现有技术栈。  
- **跨平台**：配合 Dapr sidecar，可在本地、K8s、云原生环境无缝迁移，降低运维成本。  

**典型接入方式**  
1. **引入依赖**（Maven 示例）  
   ```xml
   <dependency>
       <groupId>io.dapr</groupId>
       <artifactId>dapr-sdk</artifactId>
       <version>1.12.0</version>
   </dependency>
   ```  
2. **启动 Dapr sidecar**（本地）  
   ```bash
   dapr run --app-id my-java-app --app-port 8080 java -jar target/my-app.jar
   ```  
3. **在代码中使用 SDK**（示例：调用另一个服务）  
   ```java
   DaprClient client = new DaprClientBuilder().build();
   String result = client.invokeMethod("order-service", "create", "application/json", orderJson).block();
   ```  
4. **完成后关闭客户端**  
   ```java
   client.close();
   ```  

**生产可用性**  
- **成熟度**：已有 298+ ⭐、227+ 🍴，活跃维护，最近一次提交在 2026‑06‑30，基本满足生产需求。  
- **适用场景**：原型、内部业务系统、以及已经在使用 Dapr 的微服务架构。  
- **注意事项**：  
  - 评估依赖的安全漏洞（通过 Dependabot / Snyk 等工具）。  
  - 确认项目的许可证（Apache‑2.0）与内部合规要求匹配。  
  - 在正式环境部署前，建议先做一个小范围的 PoC，验证 sidecar 与 SDK 的兼容性以及监控、日志的集成。  

总体而言，`dapr/java-sdk` 是在 Java 生态中使用 Dapr 的首选入口，具备中等到高的生产就绪度，只要做好安全审计和小规模验证，即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** dapr/java-sdk may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 298 GitHub stars
- 227 forks
- updated 2026-06-30
- primary language: Java

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 53/100 |
| topics | 0/100 |
| outlook | 63/100 |
| quality | 59/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 64/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/dapr/java-sdk) · [← Back to Libraries--sdks](./README.md)</sub>
