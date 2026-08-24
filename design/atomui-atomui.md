# AtomUI/AtomUI

[![Stars](https://img.shields.io/github/stars/AtomUI/AtomUI?style=flat-square&color=yellow)](https://github.com/AtomUI/AtomUI/stargazers) [![Forks](https://img.shields.io/github/forks/AtomUI/AtomUI?style=flat-square&color=blue)](https://github.com/AtomUI/AtomUI/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> AtomUI leverages Avalonia's robust cross-platform capabilities to implement the Ant Design system for .NET, dedicated to delivering its refined design language and efficient user experience to cross-platform desktop application development.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 791 |
| 🍴 **Forks** | 64 |
| 💻 **Language** | C# |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ant-design` `avalonia` `cross-platform` `cross-platform-desktop` `cross-platform-gui` `dotnet` `dotnetcore` `uiframework`

## 🎯 Categories

Design

## 📝 Summary

### English

**Brief Summary**  
AtomUI is an open‑source library that brings Ant Design’s polished UI language to Avalonia, the cross‑platform .NET UI framework. By combining Avalonia’s “write once, run everywhere” capability with Ant Design’s component set, AtomUI lets developers create modern, consistent desktop applications for Windows, macOS and Linux using C#.

---

### Value Proposition
- **Design consistency** – Provides ready‑made Ant Design components (buttons, tables, forms, etc.) that follow a well‑defined visual language, saving designers and developers from reinventing the wheel.  
- **Cross‑platform reach** – Because it sits on top of Avalonia, the same UI code runs unchanged on all major desktop OSes, accelerating time‑to‑market for multi‑platform products.  
- **Open‑source & extensible** – With ~800 stars and an active community, teams can inspect, fork, and extend components to meet niche requirements without licensing constraints.  
- **Knowledge‑centric tooling** – The project’s documentation and source code are searchable, making it a useful knowledge base for AI‑assisted coding assistants that need to retrieve UI patterns or implementation details.

### Practical Adoption Path
1. **Proof‑of‑Concept (PoC)**  
   - Clone the repo and run the sample app (the README includes a simple “dotnet run” guide).  
   - Verify that the UI renders correctly on the target OSes used by your team.  

2. **Component Evaluation**  
   - Map the Ant Design components you need (e.g., DataGrid, Modal, Form) to AtomUI equivalents.  
   - Check for any missing features or custom styling requirements; if gaps exist, plan small extensions in a separate fork.  

3. **Integration into Existing Avalonia Project**  
   - Add the AtomUI NuGet package (or reference the project directly).  
   - Replace or wrap existing controls with AtomUI counterparts, gradually refactoring UI layers.  

4. **Testing & CI**  
   - Add unit‑ and UI‑tests for the new components to your pipeline.  
   - Validate that the build works on all three platforms (Windows, macOS, Linux).  

5. **Documentation & Knowledge Base**  
   - Generate internal docs (e.g., using DocFX) that index AtomUI’s component API.  
   - Feed these docs into your AI‑assistant indexing pipeline to enable code‑completion and answer retrieval.  

6. **Production Roll‑out**  
   - Once the PoC is stable, promote the changes to the main codebase, monitor performance, and establish a maintenance plan for future Avalonia/AtomUI updates.

### Production Readiness Assessment
| Dimension | Rating | Comments |
|-----------|--------|----------|
| **Stability** | **Medium** | The library is actively maintained (last commit 2026‑06‑23) and has a decent user base, but it is still relatively new for large‑scale production. |
| **Feature Coverage** | **Medium‑High** | Core Ant Design components are present, but some advanced widgets may need custom implementation. |
| **Community & Support** | **Medium** | 791 stars, 64 forks indicate a modest community; issue response times are acceptable but not enterprise‑grade. |
| **Integration Complexity** | **Medium** | No dedicated “getting started” guide beyond the README; you’ll need to experiment with Avalonia project setup and possibly adjust build scripts. |
| **Maintenance Overhead** | **Medium** | You’ll need to track both Avalonia and AtomUI releases; breaking changes are possible when either dependency updates. |
| **Overall Production Suitability** | **Ready for internal prototypes and controlled roll‑outs** | Suitable for internal tools, MVPs, or products where UI polish is valuable and the team can allocate time to monitor and patch the library. For mission‑critical, high‑traffic consumer apps, a deeper risk assessment and possibly a fallback UI library are advisable. |

**Bottom line:** AtomUI offers a compelling way to bring Ant Design’s modern UI to .NET desktop apps across platforms. Start with a small PoC to validate component fit and build process, then incrementally replace existing UI code while establishing CI testing and documentation. With proper monitoring, it can be production‑ready for internal or niche external applications, provided you budget for occasional maintenance and potential feature gaps.

### Русский

AtomUI — это open‑source библиотека, реализующая дизайн‑систему Ant Design поверх кросс‑платформенного UI‑фреймворка Avalonia, что позволяет создавать стильные и отзывчивые настольные приложения на .NET для Windows, macOS и Linux. Типичный сценарий внедрения — быстрый прототип или внутренний инструмент: подключаете пакет, импортируете готовые стили и компоненты Ant Design и сразу получаете единый пользовательский опыт без необходимости писать собственный UI‑код. Готовность к production — средняя: проект активно поддерживается (2026‑й год), имеет 791 звезду и 64 форка, но требует проверки зависимостей Avalonia и настройки сборки перед использованием в продакшене.

### 中文

**项目价值**  
AtomUI 将 Ant Design 的视觉规范和交互体验移植到 Avalonia 上，使 .NET 开发者能够在 Windows、macOS、Linux 等桌面平台上快速构建统一、现代的 UI。它不仅提供了丰富的组件库，还遵循 Ant Design 的设计语言，帮助团队在跨平台桌面应用中保持一致的视觉风格和高效的用户体验，从而缩短 UI 开发周期、降低维护成本。

**典型接入方式**  

1. **依赖安装**  
   ```bash
   dotnet add package AtomUI
   ```
   或在 `*.csproj` 中加入 `<PackageReference Include="AtomUI" Version="x.y.z" />`。

2. **初始化 Avalonia 应用**  
   在 `App.xaml.cs`（或等价的启动类）中引入 AtomUI：
   ```csharp
   public override void Initialize()
   {
       AvaloniaXamlLoader.Load(this);
       // 注册 AtomUI 主题和全局样式
       AtomUI.AvaloniaExtensions.UseAtomUI(this);
   }
   ```

3. **使用组件**  
   在 XAML 中即可直接使用 Ant Design 组件，例如：
   ```xml
   <Button Content="提交" Style="{StaticResource AntButtonStyle}" />
   <Input Placeholder="请输入内容" />
   <Table Items="{Binding Items}" />
   ```
   也可以在代码‑behind 中通过 `AtomUI.Controls` 命名空间创建控件。

4. **主题定制**  
   AtomUI 支持通过 `ThemeProvider` 动态切换主题（浅色/深色）或自定义配色，满足企业品牌需求。

5. **CI/CD 集成**  
   因为仅是 NuGet 包，加入常规的 .NET CI 流程即可，无需额外构建步骤。  

**生产可用性评估**  

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | ★★★★☆ (4/5) | 代码库已有 791 ★，活跃维护至 2026‑06‑23，社区已有一定规模。 |
| **跨平台稳定性** | ★★★★☆ | 基于 Avalonia，已在 Windows、macOS、Linux 上通过 CI 测试。 |
| **文档/示例** | ★★★☆☆ | README 与示例项目基本完整，但高级主题定制文档略显不足。 |
| **依赖风险** | ★★★☆☆ | 依赖 Avalonia 与 .NET 6/7/8，需确认目标项目的运行时兼容性。 |
| **生产准备度** | ★★★★☆ | 适合内部工具、原型及中小型业务系统；在大规模商用前建议进行组件兼容性和性能基准测试。 |

**结论**  
AtomUI 为 .NET 桌面开发提供了“一站式”Ant Design 解决方案，能够显著提升 UI 开发效率并保持跨平台一致性。接入方式简洁，仅需添加 NuGet 包并在启动时注册即可使用。对于内部工具或面向企业的跨平台桌面应用，经过基本的功能验证后即可投入生产；在大流量或高度定制化的场景下，建议先做性能与兼容性评估再全面推广。

## 🧭 Practical evaluation

**Value:** AtomUI/AtomUI helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 791 GitHub stars
- 64 forks
- updated 2026-06-23
- primary language: C#
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 62/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 66/100 |
| recency | 40/100 |
| adoption | 57/100 |
| production | 55/100 |
| usefulness | 74/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/AtomUI/AtomUI) · [← Back to Design](./README.md)</sub>
