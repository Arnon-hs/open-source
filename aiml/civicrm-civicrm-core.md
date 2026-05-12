# civicrm/civicrm-core

[![Stars](https://img.shields.io/github/stars/civicrm/civicrm-core?style=flat-square&color=yellow)](https://github.com/civicrm/civicrm-core/stargazers) [![Forks](https://img.shields.io/github/forks/civicrm/civicrm-core?style=flat-square&color=blue)](https://github.com/civicrm/civicrm-core/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> CiviCRM (Core Application and Framework)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 739 |
| 🍴 **Forks** | 875 |
| 💻 **Language** | PHP |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`crm-platform` `dcode-2025` `fundraising` `nonprofit` `open-source`

## 🎯 Categories

AI/ML · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
CiviCRM Core is the open‑source PHP‑based engine that powers the CiviCRM suite, providing a flexible framework for managing constituents, donations, events, and communications. Its modular architecture now includes hooks and APIs that make it straightforward to plug in AI/ML capabilities—such as retrieval‑augmented generation or autonomous agents—without rebuilding a model stack from scratch. The project is actively maintained (last update 2026‑05‑12) and enjoys a sizable community (≈ 740 ★, 875 forks), making it a solid foundation for prototyping AI‑enhanced civic‑tech solutions.

**Value**  
- **Accelerated AI prototyping** – Existing CiviCRM data models and REST/JSON‑API endpoints let you surface constituent records to LLMs for personalized outreach, recommendation, or decision‑support workflows.  
- **Reuse of a proven CRM stack** – You inherit robust contact management, permission handling, and reporting, so the AI layer can focus on inference rather than data plumbing.  
- **Community‑driven extensions** – A large ecosystem of extensions and documentation reduces the effort to integrate third‑party AI services (e.g., OpenAI, Anthropic, or self‑hosted models).

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Fork the repo, run the Docker‑compose dev environment, and verify the README installation steps.  
2. **Expose the API** – Enable the CiviCRM REST API (or use the built‑in “CiviCRM APIv4”) to retrieve contact data.  
3. **Add an AI microservice** – Deploy a lightweight wrapper (e.g., FastAPI or Node) that calls your chosen LLM and consumes the CiviCRM API.  
4. **Create a simple extension** – Use CiviCRM’s hook system (`hook_civicrm_alterAPIs`, `hook_civicrm_pageRun`) to trigger AI calls from a custom UI or scheduled job.  
5. **Iterate & test** – Validate output, monitor token usage, and refine prompts before scaling.

**Production Readiness**  
- **Maturity:** Medium. The core CRM is battle‑tested, but AI integration points are not native; they require custom extensions or middleware.  
- **Dependencies:** PHP 8+, MySQL/PostgreSQL, and a web server; adding an AI service introduces additional runtime (Docker, cloud LLM endpoint, or self‑hosted model).  
- **Operational considerations:** Ensure proper authentication (OAuth2 or API keys), data privacy (PII handling), and rate‑limiting for the LLM. Conduct a security review of any custom extension before deploying to production.  
- **Risk mitigation:** Start with a small, isolated proof‑of‑concept, monitor performance and cost, and only promote to production after the integration path is fully documented and automated (CI/CD, health checks).  

Overall, CiviCRM Core offers a reliable base for building AI‑augmented civic applications, provided you allocate time for a modest integration effort and perform the usual production‑grade hardening.

### Русский

CiviCRM Core — это открытая PHP‑платформа для управления взаимоотношениями с клиентами, предоставляющая готовый набор API, схемы БД и модульную архитектуру, благодаря которым можно быстро добавить AI‑функциональность (например, RAG‑поиск или агентные сценарии) без построения стека с нуля. Типичный путь внедрения — создать небольшой proof‑of‑concept, изучить README и подключить нужные AI‑модули к существующим сущностям CiviCRM, а затем масштабировать решение внутри организации. Готовность к продакшн — средняя: проект стабилен и активно поддерживается (739 ⭐, 875 forks, последние коммиты), но требует предварительной проверки зависимостей и интеграционных точек перед запуском в продуктиве.

### 中文

**项目简介（2‑3 句）**  
civicrm/civicrm-core 是 CiviCRM 的核心应用与框架，提供面向非营利组织的会员、捐赠、活动和通讯管理功能。它基于 PHP 开发，拥有活跃的社区和丰富的扩展生态。

**价值**  
- 为已有的 CRM 系统快速添入 AI 能力（如智能客服、文档检索、RAG/Agent 工作流），无需从零搭建模型堆栈。  
- 丰富的 API 与插件机制让原型开发和功能验证成本极低，适合作为内部实验平台或业务原型。

**典型接入方式**  
1. **本地或容器化部署**：使用官方 Docker 镜像或 `docker‑compose` 快速启动一个 CiviCRM 实例。  
2. **API 调用**：通过 REST/JSON‑API 与外部 AI 服务（如 OpenAI、Claude）交互，或在 CiviCRM 内部编写自定义 PHP 扩展/Hook。  
3. **插件/Extension**：在 CiviCRM Extension Directory 中创建或安装专门的 AI 插件（例如基于向量数据库的文档检索），利用现有的 Hook 系统实现 RAG 或自动化工作流。  
4. **小规模 PoC**：先在 README 指南中完成 “Hello World” 示例，确认环境、依赖和权限后，再逐步扩展到业务场景。

**生产可用性**  
- **成熟度**：社区活跃（739 ⭐、875 🍴），最近更新至 2026‑05‑12，核心代码稳定，适合作为内部原型或面向特定业务的生产系统。  
- **准备度**：属于 **中等**。在正式上线前需要完成：  
  - 依赖审计（PHP 版本、数据库、扩展兼容性）  
  - 安全加固（HTTPS、OAuth、角色权限）  
  - 性能评估（缓存、负载均衡）  
  - 监控与备份方案  
- **风险**：AI 相关的集成路径在官方元数据中不够明确，建议先做小规模概念验证（PoC），评估集成成本与维护开销后再决定大规模部署。

## 🧭 Practical evaluation

**Value:** civicrm/civicrm-core helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 739 GitHub stars
- 875 forks
- updated 2026-05-12
- primary language: PHP
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 74/100 |
| stars | 61/100 |
| topics | 63/100 |
| outlook | 79/100 |
| quality | 78/100 |
| recency | 100/100 |
| adoption | 65/100 |
| production | 74/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/civicrm/civicrm-core) · [← Back to AI/ML](./README.md)</sub>
