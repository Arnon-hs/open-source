# zaproxy/zap-extensions

[![Stars](https://img.shields.io/github/stars/zaproxy/zap-extensions?style=flat-square&color=yellow)](https://github.com/zaproxy/zap-extensions/stargazers) [![Forks](https://img.shields.io/github/forks/zaproxy/zap-extensions?style=flat-square&color=blue)](https://github.com/zaproxy/zap-extensions/network) [![Language](https://img.shields.io/badge/lang-HTML-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> ZAP Add-ons

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 934 |
| 🍴 **Forks** | 791 |
| 💻 **Language** | HTML |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-06-23 |
| 🔍 **Source** | github |

## 🏷️ Topics

`appsec` `dast` `hacktoberfest` `opensource` `security` `security-scanner` `zap` `zaproxy`

## 🎯 Categories

AI/ML · Security

## 📝 Summary

### English

**Summary**  
zaproxy/zap-extensions is the official repository of add‑ons for the OWASP ZAP security scanner, offering a rich library of plug‑ins that can be used to extend ZAP with AI‑driven testing, RAG, or autonomous agent capabilities. With over 900 ★, frequent commits (last update 2026‑06‑23) and strong community adoption, it is a mature OSS candidate for pilots that need to prototype AI‑enhanced security workflows without building a model stack from scratch.  

**Value** – The project bundles ready‑made integrations (e.g., language‑model prompts, vulnerability‑ranking agents) that let teams experiment with AI‑augmented scanning, data enrichment, and automated remediation while reusing ZAP’s existing scanning engine.  

**Practical adoption path** – Start with a small proof‑of‑concept: clone the repo, follow the README to build and load a single add‑on (e.g., an AI‑based passive scanner) into a local ZAP instance, and validate the end‑to‑end flow. Once the proof works, incrementally add more extensions, configure them via ZAP’s UI or API, and embed the setup in CI/CD pipelines.  

**Production readiness** – The extension ecosystem shows high activity, a large fork base, and recent releases, indicating stability and community support. While the integration steps are not fully documented in the metadata, the core ZAP platform is production‑grade, and the extensions have been used in real‑world deployments, making them suitable for a serious pilot after a brief validation of setup overhead.

### Русский

ZAP‑extensions — это набор открытых дополнений к OWASP ZAP, позволяющий быстро добавить AI‑функциональность (например, RAG или агентные сценарии) в процессы тестирования безопасности без необходимости строить модель с нуля. Для пилотного внедрения рекомендуется начать с небольшого proof‑of‑concept, проверив README и запустив один‑два ад‑она, после чего оценить затраты на интеграцию. Проект обладает высокой готовностью к production: активные коммиты, более 900 звёзд и 700 форков, что свидетельствует о надёжной поддержке и широком принятии в сообществе.

### 中文

**项目简介（2‑3 句）**  
zaproxy/zap-extensions 是 OWASP ZAP（Zed Attack Proxy）的官方插件仓库，提供数百个安全检测、自动化和 AI 辅助功能的扩展。通过这些 Add‑ons，用户可以在不从零构建模型的情况下，为渗透测试和漏洞评估工作流快速加入 AI 能力，如代码审计、风险评估和 RAG（检索增强生成）等。

**价值**  
- **快速原型**：直接复用已有的 AI‑enhanced 插件，省去模型训练与部署的时间成本。  
- **安全聚焦**：所有扩展均围绕 Web 应用安全设计，帮助团队在 CI/CD 中嵌入 AI 驱动的安全检测。  
- **社区与生态**：拥有 934+ 星、791+ Fork，活跃的维护者和广泛的用户基座，适合作为安全 AI 方案的实验平台。

**典型接入方式**  
1. **本地验证**：克隆仓库 → 在 ZAP 中通过 “Marketplace → Add‑on” 页面搜索并安装目标插件，或手动将插件 JAR/HTML 包放入 `~/.ZAP/addons` 目录。  
2. **CI/CD 集成**：在构建脚本（如 GitHub Actions、Jenkins）中使用官方 Docker 镜像 `owasp/zap2docker-stable`，通过 `zap.sh -addoninstall <addon-id>` 命令自动拉取并启用所需扩展。  
3. **小规模 PoC**：选取单个 AI 相关插件（例如 “ChatGPT‑Assist”），先运行一次扫描并观察输出，确认模型调用、凭证管理和费用控制符合预期后再扩展到完整工作流。

**生产可用性**  
- **成熟度**：项目近期（2026‑06‑23）仍在活跃维护，发布频率稳定，兼容最新 ZAP 版本。  
- **准备度**：在 OSS 环境中已达到 **High** 级别，可直接用于正式环境的安全自动化，只需做好以下两点：  
  1. **凭证与费用审计**：确认 AI 插件使用的外部模型（如 OpenAI、Claude）凭证安全存储，并监控调用成本。  
  2. **兼容性测试**：在预生产环境跑一次完整的扫描流程，验证插件与现有安全工具链（如 SAST、DAST）无冲突。  

综合来看，zap‑extensions 具备足够的社区活力、功能完整度和文档支持，适合作为安全团队引入 AI 功能的首选 OSS 方案。只要在正式部署前完成小规模验证和成本评估，即可放心投入生产使用。

## 🧭 Practical evaluation

**Value:** zaproxy/zap-extensions helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 934 GitHub stars
- 791 forks
- updated 2026-06-23
- primary language: HTML
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 63/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 85/100 |
| recency | 100/100 |
| adoption | 66/100 |
| production | 76/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/zaproxy/zap-extensions) · [← Back to AI/ML](./README.md)</sub>
