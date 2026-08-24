# emoncms/emoncms

[![Stars](https://img.shields.io/github/stars/emoncms/emoncms?style=flat-square&color=yellow)](https://github.com/emoncms/emoncms/stargazers) [![Forks](https://img.shields.io/github/forks/emoncms/emoncms?style=flat-square&color=blue)](https://github.com/emoncms/emoncms/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Web-app for processing, logging and visualising energy, temperature and other environmental data

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.3k |
| 🍴 **Forks** | 532 |
| 💻 **Language** | PHP |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dashboards` `emoncms` `energy-monitor` `openenergymonitor` `php` `sustainability`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
Emoncms is an open‑source web application for collecting, storing, and visualising energy, temperature and other environmental sensor data. It provides a ready‑made backend and dashboard framework that can be extended with AI/ML components, letting teams prototype intelligent analytics without building a data pipeline from scratch.  

**Value**  
- **Accelerated AI experimentation** – the platform already handles data ingestion, time‑series storage and charting, so developers can focus on adding machine‑learning models (e.g., anomaly detection, forecasting, or retrieval‑augmented generation) rather than recreating the data stack.  
- **Low‑cost prototyping** – with a mature PHP codebase, a large community (1.3 k ★), and extensive documentation, teams can quickly spin up a proof‑of‑concept environment to test AI‑driven features or agent workflows.  

**Practical adoption path**  
1. **Proof‑of‑concept** – clone the repo, follow the README to launch the Docker‑based development stack, and verify data ingestion from a sample sensor feed.  
2. **AI integration** – expose the stored time‑series via the built‑in REST API, then connect a Python or Node.js service that consumes the data, runs a model (e.g., Prophet, LLM‑based RAG), and writes results back as new feeds or alerts.  
3. **Iterate & harden** – add authentication, CI pipelines, and monitoring; evaluate dependency updates (PHP 8.x, MySQL/PostgreSQL) before moving beyond the prototype.  

**Production readiness**  
- **Maturity**: Medium – the project is actively maintained (last commit 2026‑05‑12) and widely used, but it is primarily a PHP web app, so production deployments require careful version‑pinning and security reviews.  
- **Fit for internal or edge use cases**: Ideal for internal dashboards, pilot AI features, or edge gateways where the existing stack can be leveraged.  
- **Risks**: Integration steps are not explicitly documented for AI pipelines; setting up the environment and ensuring compatibility with existing model tooling may incur additional engineering effort. A small‑scale PoC and a checklist of dependency/maintenance concerns are recommended before committing to a full production rollout.

### Русский

**Эмонт CMS (emoncms/emoncms)** – открытая веб‑приложение на PHP для сбора, обработки и визуализации энергетических, температурных и других экологических данных, которое уже содержит базовые возможности агрегации и аналитики и может быть расширено AI‑модулями без необходимости писать стек с нуля. Типичный сценарий: в рамках небольшого proof‑of‑concept подключить готовый модуль машинного обучения (например, предсказание потребления энергии) к существующим API и построить RAG‑или агентный workflow, проверив результаты в интерактивных дашбордах. Готовность к production – средняя: проект стабилен и активно поддерживается (1313 ★, обновления в 2026 г.), но требует предварительной проверки зависимостей, настройки окружения и небольших доработок интеграции перед масштабным внедрением.

### 中文

**项目简介（2‑3 句）**  
Emoncms 是一款基于 Web 的开源平台，用于采集、记录和可视化能源、温度及其他环境传感器数据。它提供丰富的仪表盘、实时图表和 API，便于在本地或云端快速搭建监测系统。

**价值**  
- **快速原型**：无需从零实现数据采集、存储和可视化，直接利用现成的插件和仪表盘即可构建原型。  
- **AI/ML 友好**：通过内置或自定义的 API，能够把历史数据导出给机器学习模型进行预测、异常检测或 RAG（检索增强生成）等高级功能。  
- **低成本扩展**：基于 PHP 与 MySQL，部署成本低，社区活跃（>1300 星），有大量现成的模块和文档。

**典型接入方式**  
1. **数据写入**：在设备端使用 HTTP POST/GET 或 MQTT 将传感器读数推送到 Emoncms 的输入 API（`/input/post`）。  
2. **数据读取**：通过 RESTful API（`/feed/value`、`/feed/data`）或 WebSocket 读取实时或历史数据，供 AI 模型或业务系统使用。  
3. **可视化**：在 Emoncms UI 中创建仪表盘或使用嵌入式 iframe 将图表嵌入到其他系统。  
4. **插件/扩展**：如需 AI 功能，可编写自定义 PHP 插件或使用外部微服务（Python、Node.js）定时拉取数据、训练模型并把预测结果回写至 Emoncms。

**生产可用性**  
- **成熟度**：项目已有多年维护，近期仍在更新（2026‑05‑12），社区活跃，适合作为内部原型或面向特定业务的生产系统。  
- **准备度**：中等。对核心功能（数据采集、存储、可视化）已相对稳定，但在大规模部署时需注意：  
  - **依赖管理**：PHP 版本、MySQL/ MariaDB 配置以及可能的 Redis 缓存需要提前验证。  
  - **扩展性**：高并发写入场景可能需要水平分片或使用外部队列（如 Kafka）做缓冲。  
  - **安全**：默认 API 没有细粒度权限控制，建议在前置网关或反向代理层加入鉴权/速率限制。  
- **上线建议**：先在测试环境完成一个“小型 PoC”，验证数据接入、API 调用和模型回写的完整链路，再评估运维成本后再推广至生产。  

总体而言，Emoncms 适合作为 AI/ML 项目的数据中枢，能够快速搭建原型并在经过适当的运维和安全加固后投入生产使用。

## 🧭 Practical evaluation

**Value:** emoncms/emoncms helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1313 GitHub stars
- 532 forks
- updated 2026-05-12
- primary language: PHP
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 66/100 |
| topics | 75/100 |
| outlook | 56/100 |
| quality | 61/100 |
| recency | 20/100 |
| adoption | 67/100 |
| production | 48/100 |
| usefulness | 74/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/emoncms/emoncms) · [← Back to Misc](./README.md)</sub>
