# rrousselGit/freezed

[![Stars](https://img.shields.io/github/stars/rrousselGit/freezed?style=flat-square&color=yellow)](https://github.com/rrousselGit/freezed/stargazers) [![Forks](https://img.shields.io/github/forks/rrousselGit/freezed?style=flat-square&color=blue)](https://github.com/rrousselGit/freezed/network) [![Language](https://img.shields.io/badge/lang-Dart-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Code generation for immutable classes that has a simple syntax/API without compromising on the features.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.2k |
| 🍴 **Forks** | 301 |
| 💻 **Language** | Dart |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`code-generator` `dart` `flutter` `hacktoberfest` `union-types`

## 🎯 Categories

Mobile

## 📝 Summary

### English

rrousselGit/freezed lets teams generate immutable Dart classes with a simple syntax, letting them reuse backend

### Русский

**rrousselGit/freezed** — это генератор кода для создания неизменяемых классов в Dart с лаконичным API, сохраняющий весь набор возможностей (copy‑with, equality, serialization и т.д.). Команда может быстро стандартизировать модели данных и ускорить выпуск API‑сервисов, переиспользуя готовую инфраструктуру вместо написания собственного кода. Проект считается готовым к production: активные коммиты, более 2000 звёзд, широкое принятие в сообществе и стабильный набор функций, требующих лишь финального подтверждения лицензии и безопасности.

### 中文

**项目简介**  
rrousselGit/freezed 是一款基于 Dart 的代码生成库，能够以极简的语法/API 创建不可变类，同时不牺牲功能丰富性。它通过注解驱动的生成器，让开发者在编写业务逻辑时免去手动实现 `copyWith`、`==`、`hashCode`、序列化等样板代码。

**价值**  
- **提升研发效率**：一次注解即可生成完整的不可变模型，显著缩短 API 服务和数据层的开发周期。  
- **统一代码规范**：所有生成的类遵循相同的不可变约束和序列化约定，帮助团队在后端/移动端保持一致的模型定义。  
- **降低错误风险**：自动生成的 `==`、`hashCode` 与 `copyWith` 等实现避免了手写时的疏漏和逻辑错误。

**典型接入方式**  
1. 在 `pubspec.yaml` 中添加 `freezed` 与 `build_runner` 依赖。  
2. 使用 `@freezed` 注解定义抽象类，并在同目录下创建对应的 `.freezed.dart` 文件。  
3. 运行 `flutter pub run build_runner build`（或 `watch`）生成代码。  
4. 在业务代码中直接使用生成的不可变类、`copyWith`、`toJson/fromJson` 等 API。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑28，项目仍在持续更新，拥有 2 178 粉丝、301 个 Fork，社区活跃。  
- **生态兼容**：原生支持 Dart/Flutter，配合 `build_runner` 可无缝集成到现有 CI/CD 流程。  
- **成熟度**：已被多个公开项目采用，具备完善的文档与示例，适合作为正式生产环境的依赖。  
- **风险**：暂无重大元数据风险，但仍需在正式使用前确认许可证（BSD‑3‑Clause）符合企业合规要求，并进行安全审计。  

综上，freezed 是一款高质量、易集成且已在生产环境验证的不可变类生成工具，适合希望快速构建统一模型并提升代码可靠性的团队使用。

## 🧭 Practical evaluation

**Value:** rrousselGit/freezed helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2178 GitHub stars
- 301 forks
- updated 2026-06-28
- primary language: Dart
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 71/100 |
| topics | 63/100 |
| outlook | 73/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 69/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/rrousselGit/freezed) · [← Back to Mobile](./README.md)</sub>
