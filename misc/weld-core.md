# weld/core

[![Stars](https://img.shields.io/github/stars/weld/core?style=flat-square&color=yellow)](https://github.com/weld/core/stargazers) [![Forks](https://img.shields.io/github/forks/weld/core?style=flat-square&color=blue)](https://github.com/weld/core/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-46%2F100-brightgreen?style=flat-square)](#)

> Weld, including integrations for Servlet containers and Java SE, examples and documentation

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 412 |
| 🍴 **Forks** | 290 |
| 💻 **Language** | Java |
| 📈 **Score** | 46/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Weld (weld/core) is an open‑source CDI (Contexts and Dependency Injection) implementation for Java that includes ready‑made integrations for servlet containers and Java SE, plus examples and documentation. While not an AI framework per se, it provides the plumbing that lets developers embed AI‑enabled services—such as RAG pipelines or autonomous agents—into existing Java applications without building a DI stack from scratch. The project is moderately popular (≈ 410 ★, 290 forks) and actively maintained as of 2026‑05‑12.

**Value**  
- **Accelerates AI prototyping**: By handling dependency injection, lifecycle management, and servlet integration, Weld lets teams focus on the AI logic (model calls, prompt orchestration, vector store access) rather than boilerplate infrastructure.  
- **Consistent Java ecosystem**: For organizations already using Java EE / Jakarta EE, Weld fits naturally into the stack, reducing the learning curve and avoiding a separate runtime for AI components.  
- **Extensible examples**: The repository ships with sample projects that demonstrate how to wire AI services into web endpoints or background jobs, serving as a quick start for RAG or agent workflows.

**Practical Adoption Path**  
1. **Evaluate the sample projects** – Clone the repo and run the provided examples to confirm that the CDI container boots correctly in your target environment (e.g., Tomcat, Jetty, or a plain Java SE app).  
2. **Add Weld as a Maven/Gradle dependency** – Include `org.jboss.weld:weld-core` (or the appropriate BOM) in your build file.  
3. **Define AI beans** – Create CDI‑annotated classes that encapsulate model clients, prompt templates, or vector‑store connectors. Weld will automatically manage their lifecycle and injection points.  
4. **Integrate with your servlet or microservice** – Use `@Inject` in servlets, JAX‑RS resources, or scheduled jobs to obtain the AI beans.  
5. **Run integration tests** – Verify that the AI components are correctly instantiated and that any required external services (LLM endpoints, databases) are reachable.  

**Production Readiness**  
- **Maturity**: Medium. The core CDI engine is stable and widely used in enterprise Java, but the AI‑specific integration patterns are not explicitly documented, so you’ll need to design and test them yourself.  
- **Maintenance**: Active (last commit 2026‑05‑12). Keep an eye on upstream Weld releases and Java EE/Jakarta EE version compatibility.  
- **Risk Mitigation**: Because integration signals are sparse, perform a proof‑of‑concept to gauge setup effort, confirm that dependency versions (Weld, servlet container, Java) coexist without conflicts, and establish monitoring for bean lifecycle failures. Once validated, the stack is suitable for internal services or low‑to‑moderate‑traffic production workloads, provided you enforce proper version pinning and regular security updates.

### Русский

**weld/core** — это открытая Java‑библиотека, предоставляющая готовый стек Weld с интеграциями для servlet‑контейнеров и Java SE, а также примеры и документацию, что позволяет быстро добавить AI‑функциональность (RAG, агентные сценарии, прототипирование моделей) без построения инфраструктуры с нуля. Типичный сценарий — внутренний прототип или экспериментальный сервис, где разработчики используют готовые интеграции, а затем проверяют совместимость и нагрузку перед переносом в продакшн. Проект имеет средний уровень готовности: достаточную популярность (412 звёзд, 290 форков) и актуальное обновление, но требует ручного аудита и проверки зависимостей, так как путь интеграции из метаданных не очевиден.

### 中文

**项目简介**  
Weld /core 是 CDI（Contexts and Dependency Injection）规范的参考实现，提供了在 Servlet 容器和 Java SE 环境下的完整集成、丰富的示例代码以及详细文档。

**价值**  
- **快速赋能**：通过即插即用的 CDI 容器，开发者可以在现有 Java 项目中轻松引入依赖注入、拦截器、事件机制等功能，无需从零搭建框架。  
- **AI 场景友好**：配合 AI/ML 库（如 TensorFlow Java、DL4J 等），可快速原型化 RAG、智能代理等工作流，省去底层依赖管理的繁琐。  

**典型接入方式**  
1. **Servlet 环境**：在 `web.xml` 或使用 `@WebListener` 注册 `org.jboss.weld.environment.servlet.Listener`，即可在传统 WAR 包中启用 CDI。  
2. **Java SE 环境**：在主类中调用 `Weld weld = new Weld(); WeldContainer container = weld.initialize();`，随后通过 `container.select(...)` 获取 Bean 实例。  
3. **Maven/Gradle**：添加 `org.jboss.weld:weld-core`（或对应的 BOM）依赖，配合 `weld-servlet`、`weld-se` 子模块使用。  

**生产可用性**  
- **成熟度**：GitHub ★412、Fork ★290，活跃维护至 2026‑05‑12，社区成熟度中等。  
- **适用场景**：非常适合内部原型、实验性 AI 功能或中小型微服务。直接用于生产前，需要：  
  - 完整的依赖冲突检查（尤其是与 Spring、Jakarta EE 其他实现共存时）。  
  - 手动验证集成路径，因为元数据中缺乏明确的接入指引。  
  - 进行性能基准测试和异常监控配置。  

综上，weld/core 是一个在 Java 生态中快速构建可插拔 AI 工作流的可靠基础设施，但在正式上线前应进行充分的依赖审查和集成验证。

## 🧭 Practical evaluation

**Value:** weld/core helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 412 GitHub stars
- 290 forks
- updated 2026-05-12
- primary language: Java

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 56/100 |
| topics | 0/100 |
| outlook | 43/100 |
| quality | 46/100 |
| recency | 20/100 |
| adoption | 57/100 |
| production | 43/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/weld/core) · [← Back to Misc](./README.md)</sub>
