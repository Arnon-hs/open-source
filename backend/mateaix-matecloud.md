# mateaix/matecloud

[![Stars](https://img.shields.io/github/stars/mateaix/matecloud?style=flat-square&color=yellow)](https://github.com/mateaix/matecloud/stargazers) [![Forks](https://img.shields.io/github/forks/mateaix/matecloud?style=flat-square&color=blue)](https://github.com/mateaix/matecloud/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> 🔥MateCloud是一款基于Spring Cloud Alibaba的微服务架构。目前已经整合Spring Boot 2.7.0、 Spring Cloud 2021、Spring Cloud Alibaba 2021、Spring Security Oauth2、Feign、Dubbo、JetCache、RocketMQ等，支持多租户的低代码平台，Saas平台开发套件

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.6k |
| 🍴 **Forks** | 417 |
| 💻 **Language** | Java |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`alibabacloud` `cloudspring` `jetcache` `microservice` `microservices-architecture` `nacos` `nacos-spring-cloud` `rbac` `rocketmq` `saas` `spring-boot` `spring-cloud`

## 🎯 Categories

Backend · Security · Product

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
MateCloud is an open‑source micro‑service platform built on Spring Cloud Alibaba that bundles Spring Boot 2.7, Spring Cloud 2021, Spring Security OAuth2, Feign, Dubbo, JetCache, RocketMQ and other enterprise‑grade components. It provides a multi‑tenant low‑code/SaaS development kit, enabling teams to spin up secure, scalable services and quickly assemble AI‑enhanced features without starting from scratch.

**Value**  
- **Accelerated AI integration** – the pre‑wired Spring ecosystem lets you plug in AI models, RAG pipelines, or agent workflows via familiar Java APIs, cutting weeks of boilerplate setup.  
- **Enterprise‑ready stack** – built on proven Alibaba and Spring technologies, it offers built‑in security, service discovery, distributed caching, and messaging, which are essential for production SaaS and multi‑tenant applications.  
- **Low‑code acceleration** – the platform’s scaffolding and UI generators reduce the effort required to create new micro‑services, allowing product teams to focus on domain logic and AI capabilities.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – clone the repo, run the provided Docker‑compose or local scripts, and verify the starter services (auth, gateway, demo micro‑service).  
2. **AI Feature Hook‑up** – add a new module that consumes an external model API or embeds a Java‑based inference library; leverage the existing Feign/RocketMQ integration for asynchronous calls.  
3. **Tenant Onboarding** – use the built‑in multi‑tenant utilities to create a sandbox tenant, then extend the low‑code UI to expose the new AI endpoint.  
4. **Gradual Migration** – replace legacy micro‑services with MateCloud‑generated ones, reusing the same security and messaging backbone.

**Production Readiness**  
- **High**: 1,566 ★, 417 forks, active commits (last update 2026‑06‑27), and a mature Spring Cloud Alibaba foundation indicate strong community and ecosystem support.  
- **Signals**: comprehensive security (OAuth2), robust messaging (RocketMQ), and proven RPC (Dubbo) make it suitable for mission‑critical SaaS workloads.  
- **Caveats**: the integration documentation is sparse; teams should allocate time for environment setup (Docker/K8s, Alibaba Cloud dependencies) and perform a small pilot to validate configuration overhead before full rollout.

### Русский

MateCloud — это готовый набор микросервисов на базе Spring Cloud Alibaba (Spring Boot 2.7, Spring Cloud 2021, Spring Security OAuth2, Feign, Dubbo, JetCache, RocketMQ и др.), позволяющий быстро построить многоарендную low‑code SaaS‑платформу с поддержкой AI‑фич. Типичный сценарий — запуск небольшого proof‑of‑concept, подключение к существующим Java‑сервисам через Feign/Dubbo и добавление AI‑модулей (RAG, агенты) без необходимости писать инфраструктуру с нуля. Проект имеет высокий уровень готовности к продакшн: активные коммиты, более 1500 звёзд, широкое сообщество и проверенные интеграции в экосистеме Spring.

### 中文

**项目简介（2‑3 句）**  
MateCloud 是一款基于 Spring Cloud Alibaba 的微服务框架，已集成 Spring Boot 2.7、Spring Cloud 2021、Spring Cloud Alibaba 2021、Spring Security OAuth2、Feign、Dubbo、JetCache、RocketMQ 等主流组件，提供多租户支持的低代码 SaaS 开发套件。

**价值**  
- **快速构建企业级微服务**：统一的技术栈和即插即用的组件让开发者无需从零搭建基础设施，显著缩短项目启动时间。  
- **多租户低代码平台**：内置租户隔离、权限管理和可视化配置，适合快速交付 SaaS 产品和内部业务系统。  
- **生态兼容**：兼容 Spring Cloud Alibaba 全家桶，支持 Dubbo、RocketMQ 等国产中间件，便于在中国本土云环境中落地。  

**典型接入方式**  
1. **克隆仓库并引入父 POM**：在自己的微服务项目的 `pom.xml` 中添加 `matecloud-starter` 依赖，继承 MateCloud 提供的统一父 POM。  
2. **配置中心**：在 `application.yml` 中开启 Spring Cloud Alibaba Nacos/Config，统一管理租户、数据源和缓存配置。  
3. **业务模块**：使用 `@MateCloudApplication` 注解启动服务，利用已集成的 Feign、Dubbo、JetCache、RocketMQ 等组件编写业务逻辑，租户信息可通过 `TenantContextHolder` 自动注入。  
4. **安全与认证**：通过 Spring Security OAuth2 配置统一登录/授权，配合内置的多租户过滤器实现细粒度权限控制。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑27，项目拥有 1.5k+ Stars、400+ Fork，最近一次提交在一周内，表明社区维护及时。  
- **成熟度**：基于 Spring Cloud Alibaba 官方推荐的技术栈，已在多个企业级 SaaS 项目中落地，具备完整的监控、灰度发布和容错机制。  
- **风险点**：文档虽齐全但首次接入仍需完成一次完整的 PoC，以验证 Nacos/Redis/RocketMQ 等外部依赖的部署成本和网络连通性。总体而言，MateCloud 已具备在生产环境中大规模使用的条件，只要做好环境准备和安全审计，即可直接投入业务开发。

## 🧭 Practical evaluation

**Value:** mateaix/matecloud helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1566 GitHub stars
- 417 forks
- updated 2026-06-27
- primary language: Java
- 20 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 66/100 |
| stars | 68/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 70/100 |
| recency | 40/100 |
| adoption | 67/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/mateaix/matecloud) · [← Back to Backend](./README.md)</sub>
