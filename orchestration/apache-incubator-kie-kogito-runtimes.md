# apache/incubator-kie-kogito-runtimes

[![Stars](https://img.shields.io/github/stars/apache/incubator-kie-kogito-runtimes?style=flat-square&color=yellow)](https://github.com/apache/incubator-kie-kogito-runtimes/stargazers) [![Forks](https://img.shields.io/github/forks/apache/incubator-kie-kogito-runtimes?style=flat-square&color=blue)](https://github.com/apache/incubator-kie-kogito-runtimes/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Kogito Runtimes is a cloud-native business automation technology for building cloud-ready business applications

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 611 |
| 🍴 **Forks** | 252 |
| 💻 **Language** | Java |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apache` `bpm` `cloud-native` `dmn` `java` `jbpm` `knative` `kogito` `pmml` `quarkus` `rule-engine` `spring-boot`

## 🎯 Categories

Orchestration · Automation

## 📝 Summary

### English

**Project Summary:**

Apache Incubator Kie Kogito Runtimes is an open-source, cloud-native business automation technology that enables developers to build cloud-ready business applications by automating repetitive manual operations and workflows. This project offers a value proposition of removing manual work, connecting tools into repeatable flows, and scheduling operational tasks. With a medium production readiness score, it is suitable for prototypes or internal workflows, requiring careful dependency and maintenance checks before production.

**Value:**
The project's primary value lies in automating repetitive tasks and workflows, reducing manual labor and increasing efficiency. It helps developers build cloud-ready business applications by integrating tools and scheduling operational tasks, making it an attractive solution for businesses looking to streamline their processes.

**Practical Adoption Path:**
For practical adoption, we recommend starting with a small proof of concept to evaluate the project's feasibility. It is essential to check the README documentation and consider the integration path before committing to the project. This will help developers understand the project's architecture, dependencies, and potential challenges. Once the proof of concept is successful, developers can scale up the adoption by integrating the project into their production workflows after conducting thorough dependency and maintenance checks.

**Production Readiness:**
The project has a medium production readiness score, indicating that it is suitable for

### Русский

Резюме:

Apache Kogito Runtimes - это облачная технология автоматизации бизнес-процессов, которая позволяет создавать облачные приложения для автоматизации бизнеса. Этот проект может помочь удалить повторяющиеся ручные операции из рабочего процесса, автоматизируя таким образом рутинные задачи и повышая эффективность. Уровень готовности к production - средний, что означает, что проект может быть полезен для прототипов или внутренних рабочих процессов, но требует тщательного проверки зависимостей и поддержки перед выпуском в производство.

### 中文

**项目简介（2‑3 句）**  
Kogito Runtimes 是 Apache Incubator 中的云原生业务自动化运行时，基于 Java 构建，旨在帮助开发者快速创建可在 Kubernetes、OpenShift 等云平台上直接部署的业务流程应用。它将业务规则、流程和决策模型统一为可编排的微服务，天然支持事件驱动和无服务器（Knative）运行模式。

**价值**  
- **消除重复人工操作**：通过将业务流程、规则和决策模型以代码形式托管，所有步骤均可自动执行、监控和回滚。  
- **加速业务创新**：业务人员可在 BPMN、DMN、Drools 等标准模型上建模，开发者只需生成微服务即可投入使用，显著缩短从需求到上线的周期。  
- **云原生弹性**：原生支持容器编排、水平扩缩、自动恢复，能够在高并发或突发负载下保持稳定。

**典型接入方式**  
1. **模型驱动开发**：在 Kogito Designer、VS Code 插件或任何支持 BPMN/DMN 的建模工具中创建业务模型。  
2. **代码生成**：使用 `kogito-maven-plugin`（或 Gradle 插件）将模型编译为 Spring Boot 或 Quarkus 微服务。  
3. **容器化部署**：将生成的 JAR 打包为 Docker 镜像，推送至容器仓库后通过 Kubernetes/Helm、OpenShift Operator 或 Knative Service 部署。  
4. **与现有系统集成**：通过 REST、gRPC、Kafka、AMQP 等标准协议调用微服务，亦可使用 Kogito 的事件桥接（Event‑Driven Architecture）将业务事件与外部系统（如数据库、消息队列、第三方 API）联通。  
5. **小范围 PoC**：先在本地或 Minikube 中运行 `kogito-quarkus-example`，验证模型、CI/CD 流程和运维脚本，再逐步推广到正式集群。

**生产可用性**  
- **成熟度**：项目仍处于 Apache Incubator 阶段，社区活跃（>600 星、250+ Fork），但缺少正式的 Apache 2.0 认证。适合作为 **原型/内部业务流程** 或 **逐步迁移** 的平台。  
- **依赖与运维**：主要依赖 Java 11+、Quarkus 或 Spring Boot、Kubernetes 环境；需要自行管理容器镜像、监控（Prometheus/Grafana）和日志（ELK）等运维组件。  
- **风险**：文档和集成示例相对分散，首次接入的学习曲线较陡；在大型企业生产环境使用前建议完成 **完整的 CI/CD、灾备、性能基准** 测试。  

**结论**：Kogito Runtimes 能显著降低业务流程自动化的开发和运维成本，适合作为 **云原生微服务化** 的业务流程引擎进行小规模验证后，再根据业务规模与运维能力决定是否进入正式生产。

## 🧭 Practical evaluation

**Value:** apache/incubator-kie-kogito-runtimes helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 611 GitHub stars
- 252 forks
- updated 2026-07-03
- primary language: Java
- 14 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 60/100 |
| stars | 59/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 67/100 |
| recency | 40/100 |
| adoption | 60/100 |
| production | 55/100 |
| usefulness | 74/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/apache/incubator-kie-kogito-runtimes) · [← Back to Orchestration](./README.md)</sub>
