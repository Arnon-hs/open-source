# hadashiA/VitalRouter

[![Stars](https://img.shields.io/github/stars/hadashiA/VitalRouter?style=flat-square&color=yellow)](https://github.com/hadashiA/VitalRouter/stargazers) [![Forks](https://img.shields.io/github/forks/hadashiA/VitalRouter?style=flat-square&color=blue)](https://github.com/hadashiA/VitalRouter/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> A fast, zero-allocation, in-memory messaging library. Declarative async pipeline with source generator for Unity and .NET.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 347 |
| 🍴 **Forks** | 22 |
| 💻 **Language** | C# |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-05-10 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dependency-injection` `eventbus` `mruby` `pubsub` `unity` `unity3d`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
VitalRouter is a high‑performance, zero‑allocation in‑memory messaging library for Unity and .NET that lets you declare asynchronous pipelines using a source‑generator‑driven API. It aims to provide fast, type‑safe event routing with minimal runtime overhead, making it attractive for games or real‑time applications that need tight control over memory and latency.

**Value**  
- **Speed & low GC pressure** – By avoiding allocations and using compile‑time code generation, VitalRouter can deliver message dispatch at frame‑rate speeds without triggering garbage‑collector spikes.  
- **Declarative pipelines** – The source generator creates strongly‑typed handlers from simple attribute‑based declarations, reducing boilerplate and improving readability.  
- **Unity‑focused** – The library integrates cleanly with Unity’s mono‑behaviour lifecycle while remaining usable in plain .NET projects, giving teams a single solution for both editor tools and runtime code.

**Practical adoption path**  
1. **Read the README and run the sample project** to verify that the source‑generator setup works with your Unity version and .NET SDK.  
2. **Create a small proof‑of‑concept** (e.g., a UI event or a gameplay message) to confirm that the generated code compiles, that handlers are invoked correctly, and that allocation profiling shows the expected zero‑allocation behavior.  
3. **Incrementally replace existing event systems** with VitalRouter in low‑risk areas, monitoring performance and ensuring that the generated code does not interfere with hot‑reload or build pipelines.  
4. **Lock down the version** (e.g., via a Git submodule or a specific NuGet tag) and add it to your CI to catch breaking changes early.

**Production readiness**  
VitalRouter shows medium readiness: it is actively maintained (last commit 2026‑05‑10), has a modest community (≈350 stars, 22 forks), and its core concepts are stable. It is suitable for prototypes, internal tools, or non‑critical gameplay features, but before using it in a shipped product you should:  

- Verify compatibility with your Unity version and any custom build pipelines.  
- Perform thorough allocation and latency profiling in the target platform(s).  
- Establish a maintenance plan (e.g., pin a specific commit or tag) to guard against future breaking changes.  

With those checks in place, VitalRouter can be a reliable component for high‑performance messaging in Unity/.NET projects.

### Русский

**VitalRouter** — это быстрая, zero‑allocation библиотека обмена сообщениями в памяти с декларативным асинхронным пайплайном и генератором кода для Unity и .NET. Она подходит для прототипов и внутренних систем, где важна минимальная нагрузка и простота построения потоков данных; типичный сценарий — подключить небольшую «router‑ядро» к существующей игре/приложению, описать обработчики через атрибуты и позволить генератору создать типобезопасный код. Готовность к production — средняя: проект активно поддерживается (обновления, 347★), но интеграция требует проверки настроек и зависимостей, поэтому рекомендуется начать с небольшого proof‑of‑concept и убедиться в совместимости с текущей кодовой базой.

### 中文

**项目简介**  
VitalRouter（hadashiA/VitalRouter）是面向 Unity 与 .NET 的高性能、零分配的内存内消息路由库。它通过声明式的异步流水线和 Source Generator，帮助开发者以极低的 GC 开销实现事件、指令或数据流的解耦与调度。

**价值点**  
- **极低 GC 开销**：在运行时不产生额外的对象分配，适合对帧率和内存敏感的 Unity 项目。  
- **声明式异步管线**：使用属性标记和代码生成，业务逻辑可以像写普通方法一样声明消息处理器，代码简洁且易维护。  
- **跨平台**：既支持 Unity（包括 IL2CPP）也支持纯 .NET（如服务器端服务），可在客户端/服务端统一使用同一套消息系统。  
- **社区活跃**：已有 347+ stars、22+ forks，最近一次提交在 2026‑05‑10，说明项目仍在维护。

**典型接入方式**  

| 步骤 | 操作 | 说明 |
|------|------|------|
| 1️⃣ 安装 | `dotnet add package VitalRouter`（或在 Unity Package Manager 中添加 Git URL） | 自动拉取源码并包含生成器。 |
| 2️⃣ 启动 Router | 在游戏入口或服务启动时调用 `Router.Initialize()`（或自行创建 `Router` 实例） | 完成内部缓存、生成的路由表初始化。 |
| 3️⃣ 定义消息 | ```csharp public struct EnemyHit { public int Damage; }``` | 消息体通常是 **struct**，避免装箱。 |
| 4️⃣ 编写处理器 | ```csharp [RouterMessageHandler] public async UniTask Handle(EnemyHit msg) { /* 业务逻辑 */ }``` | 使用 `[RouterMessageHandler]`（或对应的属性）标记，Source Generator 会自动生成注册代码。 |
| 5️⃣ 发送消息 | `await Router.PublishAsync(new EnemyHit{ Damage = 10 });` | 支持同步 `Publish` 与异步 `PublishAsync`，可在任意线程调用。 |
| 6️⃣ 可选：管线扩展 | 实现 `IPipelineStep` 并在 `RouterOptions` 中注册，以加入日志、异常捕获、过滤等统一处理。 | 通过管线实现横切关注点，保持业务代码干净。 |

> **小技巧**：在 Unity 中，最好把 `Router.Initialize()` 放在 `Awake`（或 `InitializeOnLoad`）里，并在 `OnApplicationQuit` 中调用 `Router.Dispose()`，防止泄漏。

**生产可用性评估**  

| 维度 | 评估 | 备注 |
|------|------|------|
| **性能** | ★★★★★ | 零分配、基于结构体的消息体，GC 影响可忽略。 |
| **稳定性** | ★★★★☆ | 最近活跃，Issue 处理及时，但仍需自行写单元测试验证关键路径。 |
| **易用性** | ★★★★☆ | Source Generator 简化注册，但首次使用需了解属性与生成代码的工作原理。 |
| **生态兼容** | ★★★★☆ | 与 Unity 2021+、.NET 6+ 完全兼容；IL2CPP 编译通过。 |
| **维护成本** | ★★★☆☆ | 依赖源码生成器，升级时需检查生成器兼容性；项目规模适中，适合内部或原型项目。 |

**结论**  
VitalRouter 适合作为 **Unity 客户端** 或 **.NET 微服务** 的内部事件总线，尤其在对性能（零 GC）有严格要求的场景（如实时游戏、AR/VR）中能够显著降低帧时抖动。生产环境使用时，建议先在一个小模块（如 UI 事件或子系统）做 PoC，确认生成器配置、异常处理管线以及与现有框架的兼容性后，再逐步推广到全局。只要做好版本锁定和单元测试，项目的 **中等** 生产就绪度是可以接受的。

## 🧭 Practical evaluation

**Value:** hadashiA/VitalRouter may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 347 GitHub stars
- 22 forks
- updated 2026-05-10
- primary language: C#
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 54/100 |
| topics | 75/100 |
| outlook | 73/100 |
| quality | 73/100 |
| recency | 100/100 |
| adoption | 48/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/hadashiA/VitalRouter) · [← Back to Misc](./README.md)</sub>
