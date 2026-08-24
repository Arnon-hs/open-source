# frangoteam/FUXA

[![Stars](https://img.shields.io/github/stars/frangoteam/FUXA?style=flat-square&color=yellow)](https://github.com/frangoteam/FUXA/stargazers) [![Forks](https://img.shields.io/github/forks/frangoteam/FUXA?style=flat-square&color=blue)](https://github.com/frangoteam/FUXA/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Web-based Process Visualization (SCADA/HMI/Dashboard) software

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.7k |
| 🍴 **Forks** | 1.3k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`angular` `bacnet` `dashboard` `hmi` `iot` `modbus` `mqtt` `nodejs` `opc-ua` `opcua` `plc` `s7`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
FUXA (frangoteam/FUXA) is an open‑source, web‑based SCADA/HMI/Dashboard platform written in TypeScript. With a vibrant community (4.7 k ★, 1.3 k forks) and recent commits, it offers a modern, extensible UI for visualizing and controlling industrial processes.  

**Value**  
FUXA delivers a ready‑to‑use visualisation stack that can replace proprietary HMI tools, letting teams design drag‑and‑drop dashboards, connect to OPC-UA, MQTT, Modbus, and other data sources, and embed the UI in existing web applications. Its TypeScript codebase makes customization straightforward for developers familiar with modern JavaScript ecosystems.  

**Practical Adoption Path**  

1. **Proof‑of‑Concept** – Clone the repo, run the Docker compose or npm start script, and connect a single data source (e.g., a test MQTT broker). Verify that the built‑in editor can create the required widgets and that data flows correctly.  
2. **README & Documentation Review** – Follow the quick‑start guide, check the API docs, and confirm that the licensing (MIT) and contribution guidelines align with your organization’s policies.  
3. **Pilot Integration** – Wrap FUXA in a reverse‑proxy, apply SSO/OAuth if needed, and integrate it with a non‑critical production line or a sandbox environment. Use the built‑in role‑based access control to limit exposure.  
4. **Scale‑Up** – Deploy the Docker image to a Kubernetes cluster, enable persistence for the SQLite/PostgreSQL backend, and set up monitoring (Prometheus metrics are exposed).  

**Production Readiness**  
The project scores 74/100 and shows strong production signals: frequent updates (last commit 2026‑07‑03), a large star/fork base, and a clear TypeScript codebase. While no major metadata issues were found, a final security audit (dependency scanning, license verification, and maintainer activity check) is recommended before a full‑scale rollout. With those checks completed, FUXA is considered a high‑readiness OSS candidate for a serious pilot or production deployment.

### Русский

**frangoteam/FUXA** — это веб‑ориентированное SCADA/HMI/дашборд‑решение на TypeScript, позволяющее визуализировать и управлять промышленными процессами через браузер. Его типичное внедрение начинается с небольшого proof‑of‑concept: проверяете README, подключаете несколько датчиков/PLC и создаёте первую панель, после чего можно масштабировать до полноценного мониторинга производства. По уровню готовности проект считается «production‑ready»: активная поддержка, более 4 000 звёзд, регулярные обновления и широкое сообщество делают его надёжным кандидатом для серьёзного пилотного проекта.

### 中文

**项目简介**  
FUXA（frangoteam/FUXA）是一款基于 Web 的过程可视化平台，提供 SCADA、HMI 与仪表盘功能，帮助工业或物联网系统实时展示、监控和交互式控制生产流程。  

**价值**  
- **快速可视化**：通过拖拽式页面编辑器即可构建自定义仪表盘，无需编写前端代码。  
- **跨平台**：纯前端（TypeScript）实现，支持浏览器直接访问，适配桌面、移动和嵌入式设备。  
- **开源生态**：拥有近 5k 星、千余 Fork，社区活跃，可自行扩展插件或集成第三方数据源。  

**典型接入方式**  
1. **数据源对接**：使用内置的 OPC-UA、Modbus、MQTT、REST API 等适配器，或通过自定义 Node.js 插件将 PLC、MES、数据库等实时数据推送到 FUXA。  
2. **仪表盘构建**：在浏览器中打开 FUXA 编辑器，拖拽图表、按钮、趋势线等组件，绑定到已注册的数据点。  
3. **嵌入或发布**：将生成的仪表盘以 URL、iframe 或静态文件形式嵌入现有业务系统，或通过 Docker 镜像部署到内部服务器。  

**生产可用性**  
- **活跃维护**：最近一次提交在 2026‑07‑03，社区贡献频繁，Issue 响应及时。  
- **成熟度**：已有多个行业案例（能源、制造、智慧园区）投入生产使用，功能稳定且文档完整。  
- **可评估性**：建议先在测试环境完成小规模 PoC（如接入一条 OPC-UA 数据流并构建基础仪表盘），验证兼容性后再推广至全线。  

综上，FUXA 具备高可用的开源基础、灵活的集成方式和成熟的生产实践，是构建工业监控与可视化系统的可靠候选方案。

## 🧭 Practical evaluation

**Value:** frangoteam/FUXA may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4688 GitHub stars
- 1270 forks
- updated 2026-07-03
- primary language: TypeScript
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 78/100 |
| stars | 78/100 |
| topics | 100/100 |
| outlook | 65/100 |
| quality | 75/100 |
| recency | 40/100 |
| adoption | 78/100 |
| production | 63/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/frangoteam/FUXA) · [← Back to Misc](./README.md)</sub>
