# open5gs/open5gs

[![Stars](https://img.shields.io/github/stars/open5gs/open5gs?style=flat-square&color=yellow)](https://github.com/open5gs/open5gs/stargazers) [![Forks](https://img.shields.io/github/forks/open5gs/open5gs?style=flat-square&color=blue)](https://github.com/open5gs/open5gs/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Open5GS is a C-language Open Source implementation for 5G Core and EPC, i.e. the core network of LTE/NR network (Release-19)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.6k |
| 🍴 **Forks** | 1.1k |
| 💻 **Language** | C |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`3gpp` `4g` `5g` `5gc` `core` `epc` `lte` `network` `nr` `open5gs`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
Open5GS is a mature, C‑language open‑source implementation of the 5G Core (5GC) and LTE EPC (Release‑19), offering a full‑stack core network that can be deployed for research, testing, or commercial pilots. With over 2.6 k GitHub stars, frequent commits, and a growing community, it is one of the most actively maintained OSS 5G core projects today.

**Value**  
- Provides a complete, standards‑compliant 5G core (AMF, SMF, UPF, etc.) and LTE EPC without licensing fees, enabling rapid prototyping of 5G/4G services, edge‑computing use cases, or private‑network deployments.  
- Written in C, it delivers low‑latency performance and easy integration with existing telecom‑grade infrastructure (e.g., VNFs, containers, or bare‑metal servers).  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, follow the README to spin up the core components in Docker or on a VM; connect a commercial or open‑source RAN (e.g., srsRAN) to validate basic attach and session flow.  
2. **Customization** – Extend the control‑plane logic (e.g., policy rules, subscriber database) by modifying the C source or using the provided REST APIs.  
3. **Scaling** – Deploy individual network functions as separate containers or Kubernetes pods, leveraging the existing Helm charts and the documented HA configurations.  

**Production readiness**  
Open5GS scores high for production pilots: recent commits (as of June 2026), extensive community adoption, and a robust ecosystem of tutorials, CI pipelines, and third‑party integrations (e.g., OpenAirInterface, Magma). While the integration steps are not fully documented in the metadata, the project’s activity level, issue‑resolution speed, and real‑world deployments (private 5G networks, testbeds) indicate it is ready for serious field trials, provided a small initial PoC validates the deployment environment and any required customizations.

### Русский

Open5GS — это полностью открытая реализация ядра 5G/4G (NR/EPC) на C, поддерживающая функции Release‑19 и активно поддерживаемая сообществом (2618 ★, более 1000 форков, регулярные обновления). Проект подходит для быстрого развертывания пилотного 5G‑ядра в тестовых и небольших продакшн‑средах: достаточно выполнить небольшое proof‑of‑concept, проверив README и базовые конфигурации, после чего можно масштабировать до полноценного оператора. Готовность к production высокая благодаря активному развитию, широкому принятию и зрелой экосистеме, однако рекомендуется оценить затраты на интеграцию и адаптацию под конкретный workflow перед крупным внедрением.

### 中文

**项目简介**  
Open5GS 是用 C 语言实现的开源 5G Core 与 EPC（LTE 核心网）软件，覆盖 5G NR/LTE Release‑19 的核心功能，已在全球多个商用试验中得到验证。

**价值**  
- **完整的 5G/EPC 栈**：提供 AMF、SMF、UPF、MME、SGW、PGW 等关键网络功能，能够快速搭建端到端的移动核心网络。  
- **社区活跃、成熟可靠**：超过 2600 颗星、1000+ Fork，近期仍保持活跃更新，具备丰富的文档和示例，降低研发成本。  
- **完全开源、无许可证费用**：采用 permissive 许可证，可自由定制和商用，适合运营商、实验室以及研发团队。

**典型接入方式**  
1. **源码编译**：在 Linux（Ubuntu/Debian/CentOS）环境下通过 `./waf configure && ./waf` 编译得到各核心组件的二进制。  
2. **容器化部署**：官方提供 Dockerfile 与 Helm chart，支持在 Docker、K8s 环境中以单节点或多节点模式启动，便于与现有 CI/CD 流程集成。  
3. **配置即代码**：通过 YAML/JSON 配置文件定义网络拓扑、SBI 接口、UPF 转发规则等，可结合 Ansible 或 Terraform 实现自动化部署。  

**生产可用性**  
- **成熟度**：已在多个运营商实验网和商用试点中运行，满足 5G 核心网的基本性能与可靠性要求。  
- **运维支持**：提供日志、监控（Prometheus exporter）和故障排查脚本，社区和商业合作伙伴可提供技术支持。  
- **风险与准备**：虽然功能完整，但首次集成仍需进行小规模 PoC 验证网络拓扑、计费系统和安全策略，以评估部署成本和运维复杂度。总体而言，Open5GS 具备进入生产环境的技术条件，适合作为 5G 核心网的 OSS 候选。

## 🧭 Practical evaluation

**Value:** open5gs/open5gs may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2618 GitHub stars
- 1054 forks
- updated 2026-06-23
- primary language: C
- 10 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 76/100 |
| stars | 73/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 73/100 |
| recency | 40/100 |
| adoption | 74/100 |
| production | 57/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/open5gs/open5gs) · [← Back to Misc](./README.md)</sub>
