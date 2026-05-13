# wazuh/wazuh

[![Stars](https://img.shields.io/github/stars/wazuh/wazuh?style=flat-square&color=yellow)](https://github.com/wazuh/wazuh/stargazers) [![Forks](https://img.shields.io/github/forks/wazuh/wazuh?style=flat-square&color=blue)](https://github.com/wazuh/wazuh/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-79%2F100-brightgreen?style=flat-square)](#)

> Wazuh - The Open Source Security Platform. Unified XDR and SIEM protection for endpoints and cloud workloads.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 15.6k |
| 🍴 **Forks** | 2.3k |
| 💻 **Language** | C++ |
| 📈 **Score** | 79/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cloud-security` `compliance` `configuration-assessement` `container-security` `cybersecurity` `file-integrity-monitoring` `incident-response` `infosec` `log-analysis` `malware-detection` `pci-dss` `security`

## 🎯 Categories

Automation · AI/ML · Database · Observability · Security

## 📝 Summary

### English

**Brief Summary**  
Wazuh is an open‑source security platform that delivers unified XDR and SIEM capabilities for endpoints, containers, and cloud workloads. It automates repetitive security operations—such as log collection, threat detection, and compliance reporting—so teams can focus on response rather than manual data handling. With a large, active community (15 k+ stars, 2 k+ forks) and recent C++‑based development, it is ready for serious pilot projects.

**Value**  
Wazuh removes the need for hand‑crafted scripts and ad‑hoc tooling by providing a single, extensible framework that ingests data, correlates events, and triggers automated actions. This lets security teams build repeatable, observable workflows (e.g., “when a suspicious process is detected on an endpoint, quarantine it and open a ticket”) and integrate with existing tools such as Elastic, Splunk, or cloud security services.

**Practical Adoption Path**  
1. **Proof‑of‑concept:** Deploy the official Docker or quick‑start package in a sandbox environment and follow the README to connect a few test agents.  
2. **Integration:** Use the built‑in APIs and pre‑made integrations (Elastic, Kibana, AWS, Azure, GCP, etc.) to feed data from your existing log sources and orchestrate response actions.  
3. **Scale:** Gradually roll out agents to production endpoints, configure rule sets for your specific compliance and threat‑model needs, and automate routine tasks via the Wazuh API or external orchestration tools (Ansible, Terraform, etc.).  

**Production Readiness**  
Wazuh scores high on production readiness: it has continuous releases (latest update 2026‑05‑13), strong community adoption, and a mature ecosystem of plugins and documentation. While the integration steps are not fully exposed in the metadata, the extensive README, community forums, and reference architectures make it feasible to start with a small pilot and expand once the setup cost is validated. The project’s activity, fork count, and broad language support indicate it is a reliable OSS candidate for enterprise‑grade security automation.

### Русский

Wazuh — это открытая платформа XDR/SIEM, позволяющая автоматизировать рутинные операции по мониторингу и защите конечных точек и облачных нагрузок, объединяя сбор данных, корреляцию событий и реагирование в едином конвейере. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept, подключение существующих инструментов через готовые интеграции и планирование повторяющихся задач (например, сканирование уязвимостей или корреляцию логов). Проект демонстрирует высокий уровень готовности к продакшн: активные обновления, более 15 000 звёзд на GitHub, широкое сообщество и проверенная экосистема, однако перед масштабным развертыванием следует уточнить детали интеграции и оценить затраты на первоначальную настройку.

### 中文

**项目简介**  
Wazuh（wazuh/wazuh）是一个开源安全平台，提供统一的 XDR 与 SIEM 能力，能够对终端、容器及云工作负载进行持续监控、威胁检测和合规审计。  

**价值**  
- **自动化安全运营**：通过统一的代理和规则引擎，消除大量手工日志收集、事件关联和响应的重复工作。  
- **可编排的安全流水线**：支持将 Wazuh 与 CI/CD、Ticket 系统、SOAR 等工具链路化，实现告警自动分发、工单创建和补救脚本的调度执行。  
- **跨环境统一视图**：一次部署即可覆盖本地服务器、容器平台以及公有云，实现统一的安全姿态管理。  

**典型接入方式**  
1. **部署代理**：在目标主机（Linux、Windows、macOS）上安装 Wazuh‑Agent，自动将日志、文件完整性、系统调用等数据推送至管理服务器。  
2. **部署服务器**：使用 Docker‑Compose、Kubernetes Helm Chart 或传统包管理方式（RPM/DEB）搭建 Wazuh‑Manager + Elasticsearch + Kibana（或 OpenSearch）组合，形成完整的 SIEM 后端。  
3. **集成外部工具**：通过官方提供的 API、Webhook 或预置的集成插件（如 Slack、Jira、ServiceNow、PagerDuty），将告警流转至已有的运维/响应平台。  
4. **自动化任务**：利用 Wazuh 的 **Active Response** 功能，编写自定义脚本或使用内置脚本（如阻断 IP、杀死进程），在检测到威胁时自动执行修复操作。  

**生产可用性**  
- **成熟度高**：GitHub ★15.5k、Fork ★2.3k，最近一次提交在 2026‑05‑13，活跃的社区和商业支持（Wazuh Inc.）保证了持续迭代和安全补丁。  
- **部署稳定**：官方提供完整的 Helm Chart、Docker‑Compose 示例以及详细的 README，适合直接在生产环境做 POC，随后扩展至全量部署。  
- **风险提示**：元数据中未明确标注完整的集成路径，建议在小规模 PoC 中验证与现有 SIEM/SOAR 的对接成本，并评估网络、存储和 Elasticsearch/Opensearch 的资源需求。  

总体而言，Wazuh 已具备在企业级生产环境中作为核心 XDR/SIEM 平台使用的条件，只要做好前期的规模评估与集成测试，即可投入长期运营。

## 🧭 Practical evaluation

**Value:** wazuh/wazuh helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 15569 GitHub stars
- 2298 forks
- updated 2026-05-13
- primary language: C++
- 20 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 84/100 |
| stars | 89/100 |
| topics | 100/100 |
| outlook | 95/100 |
| quality | 94/100 |
| recency | 100/100 |
| adoption | 88/100 |
| production | 79/100 |
| usefulness | 90/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/wazuh/wazuh) · [← Back to Automation](./README.md)</sub>
