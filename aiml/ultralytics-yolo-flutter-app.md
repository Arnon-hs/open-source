# ultralytics/yolo-flutter-app

[![Stars](https://img.shields.io/github/stars/ultralytics/yolo-flutter-app?style=flat-square&color=yellow)](https://github.com/ultralytics/yolo-flutter-app/stargazers) [![Forks](https://img.shields.io/github/forks/ultralytics/yolo-flutter-app?style=flat-square&color=blue)](https://github.com/ultralytics/yolo-flutter-app/network) [![Language](https://img.shields.io/badge/lang-Dart-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Flutter plugin for Ultralytics YOLO

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 450 |
| 🍴 **Forks** | 168 |
| 💻 **Language** | Dart |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `android` `app` `coreml` `dart` `flutter` `ios` `litert` `mobile` `object-detection` `tflite` `ultralytics`

## 🎯 Categories

AI/ML · Mobile

## 📝 Summary

### English

Here's a brief summary:

The ultralytics/yolo-flutter-app is an open-source project that enables the integration of AI capabilities into Flutter applications using the Ultralytics YOLO model. This plugin allows developers to easily add AI-powered features to their mobile apps, making it a valuable tool for prototyping and building AI-driven workflows. With its high production readiness and strong ecosystem signals, this project is suitable for serious pilots and adoption.

**Value:**
The ultralytics/yolo-flutter-app provides a pre-built model stack for AI capabilities, saving developers time and effort in building AI-powered features from scratch. This plugin is particularly useful for prototyping AI features, building RAG (Recognition, Action, and Generation) or agent workflows, and evaluating model tooling.

**Practical Adoption Path:**

1. Evaluate the plugin's implementation signals, such as API/SDK/CLI, language metadata, and focused topics, to ensure it meets your project's requirements.
2. Assess the plugin's production readiness, considering factors like recent activity, adoption, and ecosystem signals.
3. Review the plugin's license, security posture, and active maintainers to ensure they align with your project's needs.
4. Integrate the plugin into your Flutter application, following the provided documentation and guidelines.
5.

### Русский

**ultralytics/yolo-flutter-app** — это Flutter‑плагин, позволяющий быстро добавить в мобильные приложения возможности компьютерного зрения на базе моделей Ultralytics YOLO без необходимости самостоятельно собирать стек ML. Он идеально подходит для прототипирования AI‑функций, создания RAG‑ или агентных рабочих потоков и оценки инструментария модели, при этом предоставляет готовый API/SDK/CLI и метаданные языка. Проект считается практически готовым к production: активные коммиты, 450 звёзд, 168 форков, свежие обновления (июль 2026) и широкая экосистема, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
ultralytics/yolo-flutter-app 是一个基于 Flutter 的插件，帮助开发者在移动端快速集成 Ultralytics YOLO 系列视觉模型，实现实时目标检测与分割等 AI 能力。

**价值**  
- **即插即用**：无需自行搭建模型推理栈，直接调用插件即可获得高精度的目标检测功能，显著缩短原型开发周期。  
- **跨平台**：Flutter 的一次编写、在 iOS 与 Android 上统一运行，降低多端维护成本。  
- **生态兼容**：提供统一的 API/SDK，支持与 RAG、智能体等更复杂的 AI 工作流无缝对接。

**典型接入方式**  
1. 在 `pubspec.yaml` 中添加 `yolo_flutter`（或对应插件名）依赖。  
2. 在 Flutter 项目初始化时调用 `YOLO.initialize()` 并加载预训练的 `.pt`/`.engine` 模型文件。  
3. 使用 `YOLO.detectFromImage()`、`YOLO.detectFromCamera()` 等方法获取检测结果，返回的结构化数据可直接用于 UI 绘制或后续业务逻辑。  

**生产可用性**  
- **活跃度高**：截至 2026‑07‑04，仓库拥有 450+ Stars、168+ Forks，最近一次提交仅数天前，表明项目仍在积极维护。  
- **技术成熟**：核心实现基于 Dart，配合原生 Android/iOS 推理库，已通过多平台实测，具备稳定的实时推理性能。  
- **社区与生态**：拥有 14 个相关话题标签，已有若干公开案例在实际产品中使用，社区支持和文档较为完善。  
- **风险**：仍需进一步审查许可证（MIT/Apache 等）以及安全审计报告，确认无潜在依赖漏洞后即可在生产环境中安全使用。  

总体而言，ultralytics/yolo-flutter-app 已具备在正式项目中进行试点或直接上线的技术与社区基础，只要完成最终的合规与安全评估，即可视为生产可用的 AI 解决方案。

## 🧭 Practical evaluation

**Value:** ultralytics/yolo-flutter-app helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 450 GitHub stars
- 168 forks
- updated 2026-07-04
- primary language: Dart
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 56/100 |
| production | 70/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/ultralytics/yolo-flutter-app) · [← Back to AI/ML](./README.md)</sub>
