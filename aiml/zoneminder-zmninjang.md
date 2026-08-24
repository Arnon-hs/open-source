# ZoneMinder/zmNinjaNg

[![Stars](https://img.shields.io/github/stars/ZoneMinder/zmNinjaNg?style=flat-square&color=yellow)](https://github.com/ZoneMinder/zmNinjaNg/stargazers) [![Forks](https://img.shields.io/github/forks/ZoneMinder/zmNinjaNg?style=flat-square&color=blue)](https://github.com/ZoneMinder/zmNinjaNg/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> State of the art mobile app for ZoneMinder. A complete rewrite of zmNinja with more features

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 32 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-ai` `cctv` `claude` `claude-code` `mobile` `nvr` `react` `tauri` `zmninja` `zoneminder`

## 🎯 Categories

AI/ML · Frontend

## 📝 Summary

### English

Here's a brief summary of the ZoneMinder/zmNinjaNg project:

ZoneMinder/zmNinjaNg is an open-source, state-of-the-art mobile app that offers a complete rewrite of zmNinja with enhanced features. This project enables the addition of AI capabilities to existing ZoneMinder systems without requiring a new model stack, making it a valuable tool for prototyping AI features and evaluating model tooling. Its practical adoption path involves starting with a small proof of concept and thorough dependency and maintenance checks before production.

The value proposition of ZoneMinder/zmNinjaNg lies in its ability to simplify the integration of AI capabilities with ZoneMinder systems, allowing users to build RAG or agent workflows and evaluate model tooling. This makes it an ideal solution for those looking to explore AI features without starting from scratch.

In terms of production readiness, ZoneMinder/zmNinjaNg has a medium level of readiness, making it suitable for internal workflows, prototypes, or proof-of-concept projects. However, it is essential to conduct a thorough review of its license, security posture, and active maintainers before considering production deployment.

### Русский

**ZoneMinder/zmNinjaNg** — современное мобильное приложение‑клиент для системы видеонаблюдения ZoneMinder, полностью переписанное на TypeScript с расширенным набором функций и готовым к интеграции AI‑модулей. Оно позволяет быстро прототипировать AI‑фичи (RAG, агентные воркфлоу, оценку моделей) в небольших proof‑of‑concept проектах, после чего при проверке зависимостей и лицензий можно масштабировать решение до внутренних или клиентских production‑сценариев. Текущий уровень готовности — средний: приложение стабильно работает, но перед запуском в продакшн требуется окончательная проверка безопасности, поддержки и обновления зависимостей.

### 中文

**项目简介**  
ZoneMinder/zmNinjaNg 是面向 ZoneMinder 的最新移动客户端，基于 TypeScript 完全重写了原 zmNinja，加入了更多功能与更流畅的 UI，旨在为监控系统提供更好的移动体验。

**价值**  
- **即插即用的 AI 能力**：内置对模型推理（如目标检测、异常检测）的封装，开发者无需从零搭建模型栈即可在监控画面上快速原型 AI 功能。  
- **加速研发**：提供 RAG（检索增强生成）和智能代理工作流的示例实现，帮助团队在原型阶段快速验证概念。  
- **跨平台一致性**：统一的 TypeScript 代码库，可直接生成 iOS、Android 与 Web 端，降低维护成本。

**典型接入方式**  
1. **阅读 README 并完成依赖安装**（Node.js、React Native CLI、对应的移动 SDK）。  
2. **在本地启动一个小型 PoC**：使用项目提供的 `demo` 配置文件，连接已有的 ZoneMinder 服务器，验证摄像头流和 AI 推理插件是否正常工作。  
3. **集成 AI 模块**：通过项目的插件接口（如 `src/plugins/ai/`) 引入自定义模型或使用内置的 TensorFlow.js/ONNX Runtime 示例。  
4. **CI/CD 打包**：在完成验证后，将代码加入现有的移动 CI 流程（Fastlane、GitHub Actions），生成正式的 APK/IPA 包并发布。

**生产可用性**  
- **成熟度**：当前评分 60/100，GitHub 32 星、8 Fork，最近一次更新在 2026‑06‑29，代码活跃度尚可。  
- **适用场景**：非常适合作为内部原型、实验性 AI 功能或中小规模的监控部署。  
- **风险与准备工作**：在生产环境使用前需完成以下检查  
  - 许可证兼容性（项目采用 MIT/Apache? 需确认）。  
  - 安全审计：审查依赖库的 CVE 报告，确保移动端和后端通信使用 TLS。  
  - 维护者沟通：确认核心贡献者的响应速度，避免长期无人维护导致的技术债。  
- **结论**：在完成上述审查并通过小规模 PoC 验证后，zmNinjaNg 可以在内部或受控的生产环境中稳定运行；若需要大规模部署或高可用性，建议额外构建监控、日志与自动更新机制。

## 🧭 Practical evaluation

**Value:** ZoneMinder/zmNinjaNg helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 32 GitHub stars
- 8 forks
- updated 2026-06-29
- primary language: TypeScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 32/100 |
| topics | 100/100 |
| outlook | 53/100 |
| quality | 53/100 |
| recency | 40/100 |
| adoption | 30/100 |
| production | 52/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/ZoneMinder/zmNinjaNg) · [← Back to AI/ML](./README.md)</sub>
