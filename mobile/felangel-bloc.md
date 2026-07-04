# felangel/bloc

[![Stars](https://img.shields.io/github/stars/felangel/bloc?style=flat-square&color=yellow)](https://github.com/felangel/bloc/stargazers) [![Forks](https://img.shields.io/github/forks/felangel/bloc?style=flat-square&color=blue)](https://github.com/felangel/bloc/network) [![Language](https://img.shields.io/badge/lang-Dart-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> A predictable state management library that helps implement the BLoC design pattern

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 12.5k |
| 🍴 **Forks** | 3.4k |
| 💻 **Language** | Dart |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-07-04 |
| 🔍 **Source** | github |

## 🏷️ Topics

`angulardart` `bloc` `concurrency` `dart` `dart-library` `dart-web` `dartlang` `flutter` `flutter-package` `library` `state-management`

## 🎯 Categories

Mobile · Design

## 📝 Summary

### English

**Summary**  
`felangel/bloc` is a widely‑adopted, open‑source Dart library that provides a predictable, testable way to implement the BLoC (Business Logic Component) design pattern for mobile apps. With over 12 k stars, active maintenance, and strong ecosystem support, it is ready for production use, though the integration steps are not fully described in the metadata and should be validated with a small proof‑of‑concept.

**Value**  
The library abstracts state management into streams and events, making UI code declarative and business logic reusable across Flutter projects. Its popularity and extensive community resources (samples, tutorials, and third‑party extensions) reduce the learning curve and help teams enforce a clean separation of concerns, leading to more maintainable codebases.

**Practical adoption path**  

1. **Read the README and official example** – confirm that the library’s API matches the app’s current architecture (e.g., event‑driven state updates).  
2. **Create a tiny proof‑of‑concept** – implement a single feature (e.g., a counter or login flow) using `BlocProvider`, `BlocBuilder`, and `BlocListener` to verify wiring, code generation, and testing workflow.  
3. **Evaluate setup cost** – check required dependencies (flutter_bloc, equatable, etc.), CI configuration, and any platform‑specific considerations.  
4. **Gradually migrate** – replace existing state‑management code module‑by‑module, keeping both old and new implementations during the transition to avoid regressions.  

**Production readiness**  
The project scores high on production readiness: it is actively maintained (last commit today), has a large user base, numerous forks, and is part of the Flutter ecosystem’s core recommendations. The only caution is the lack of explicit integration documentation in the repository metadata, so teams should allocate time for the initial proof‑of‑concept and verify that the build pipeline can accommodate the required code‑generation steps before a full rollout.

### Русский

**felangel/bloc** — это популярная библиотека на Dart для предсказуемого управления состоянием, реализующая паттерн BLoC и позволяющая чисто отделять бизнес‑логику от UI в мобильных приложениях. Типичное внедрение начинается с небольшого proof‑of‑concept: изучаете README, подключаете пакет к небольшому модулю и проверяете, как удобно описывать события и состояния; при положительном результате масштабируете на весь проект. По метрикам готовности (12469 звёзд, активные коммиты, широкое принятие в сообществе) библиотека считается production‑ready, однако стоит уточнить детали интеграции и оценить затраты на настройку перед масштабным rollout.

### 中文

**项目价值**  
`felangel/bloc` 是 Flutter 生态中最流行的状态管理库之一，提供可预测、可测试的 BLoC（Business Logic Component）实现。它通过将 UI 与业务逻辑彻底解耦，使代码更易维护、复用和单元测试，特别适合中大型移动应用以及需要严格状态管理的团队。

**典型接入方式**  

1. **阅读官方 README**：确认项目的最低 Flutter/Dart 版本要求，了解 `BlocProvider`、`BlocBuilder`、`BlocListener` 等核心 API。  
2. **在 `pubspec.yaml` 中添加依赖**  
   ```yaml
   dependencies:
     flutter:
       sdk: flutter
     flutter_bloc: ^8.1.0   # 包含 felangel/bloc 的实现
   ```
3. **创建 Bloc**  
   ```dart
   class CounterEvent {}
   class Increment extends CounterEvent {}

   class CounterState {
     final int count;
     const CounterState(this.count);
   }

   class CounterBloc extends Bloc<CounterEvent, CounterState> {
     CounterBloc() : super(const CounterState(0)) {
       on<Increment>((event, emit) => emit(CounterState(state.count + 1)));
     }
   }
   ```
4. **在 UI 中提供 Bloc**  
   ```dart
   BlocProvider(
     create: (_) => CounterBloc(),
     child: MyHomePage(),
   );
   ```
5. **在页面里消费状态**  
   ```dart
   BlocBuilder<CounterBloc, CounterState>(
     builder: (context, state) => Text('Count: ${state.count}'),
   );

   ElevatedButton(
     onPressed: () => context.read<CounterBloc>().add(Increment()),
     child: const Text('Add'),
   );
   ```
6. **小范围验证**：先在一个独立的 feature 或 demo 页面实现上述流程，确认编译、热重载、单元测试均正常后，再逐步迁移到业务模块。

**生产可用性**  

- **活跃度**：截至 2026‑07‑04 最近一次提交，拥有 12 469 ⭐、3 415 🍴，社区活跃，官方文档、示例和 FAQ 完备。  
- **生态兼容**：`flutter_bloc` 与 `bloc_concurrency`、`hydrated_bloc`、`bloc_test` 等配套库协同工作，已被多数主流 Flutter 项目（包括 Google 官方示例）采用。  
- **成熟度**：库已历经多个大版本迭代，API 稳定，向后兼容性好，且提供完整的单元/集成测试支持。  
- **风险**：唯一需要关注的是项目的初始化配置（如 `BlocObserver`、日志/错误上报）以及与现有状态管理方案的迁移成本，建议在正式上线前完成一次端到端的集成验证（包括 CI 流水线中的 `bloc_test`）。

**结论**：`felangel/bloc` 具备高生产就绪度，适合作为 Flutter 项目的核心状态管理方案。推荐先在一个小模块做 PoC，确认与现有代码库的集成方式后，再在全局范围推广。

## 🧭 Practical evaluation

**Value:** felangel/bloc may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 12469 GitHub stars
- 3415 forks
- updated 2026-07-04
- primary language: Dart
- 11 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 88/100 |
| stars | 87/100 |
| topics | 100/100 |
| outlook | 85/100 |
| quality | 94/100 |
| recency | 100/100 |
| adoption | 87/100 |
| production | 79/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/felangel/bloc) · [← Back to Mobile](./README.md)</sub>
