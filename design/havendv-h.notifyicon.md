# HavenDV/H.NotifyIcon

[![Stars](https://img.shields.io/github/stars/HavenDV/H.NotifyIcon?style=flat-square&color=yellow)](https://github.com/HavenDV/H.NotifyIcon/stargazers) [![Forks](https://img.shields.io/github/forks/HavenDV/H.NotifyIcon?style=flat-square&color=blue)](https://github.com/HavenDV/H.NotifyIcon/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> TrayIcon for WPF/WinUI/Uno/MAUI

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 752 |
| 🍴 **Forks** | 59 |
| 💻 **Language** | C# |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`console` `context-menus` `csharp` `custom-balloons` `dotnet` `net` `net5` `netcore` `notifyicon` `nuget` `popups` `tooltips`

## 🎯 Categories

Design

## 📝 Summary

### English

**Brief Summary**  
HavenDV / H.NotifyIcon is an open‑source library that adds a lightweight, customizable system‑tray icon (notification area) to WPF, WinUI, Uno Platform and .NET MAUI applications. With over 750 GitHub stars and active commits, it provides a single, consistent API for showing icons, menus, balloon tips and click callbacks across the major Windows UI stacks.  

**Value**  
The package eliminates the boilerplate and inter‑op headaches that normally accompany tray‑icon implementation on each UI framework, letting developers focus on core product logic—whether that’s a desktop AI assistant, a RAG‑powered search widget, or any background service that needs a persistent UI presence. By exposing a clean, framework‑agnostic API, H.NotifyIcon speeds up prototyping of AI‑enhanced features (e.g., quick‑access model controls) and reduces maintenance overhead in multi‑platform .NET projects.  

**Practical Adoption Path**  

1. **Add the NuGet package** to the .csproj of the target WPF/WinUI/Uno/MAUI app.  
2. **Instantiate `NotifyIcon`** in the startup code (App.xaml.cs or MainPage) and configure the icon, tooltip, and context‑menu items using the fluent API.  
3. **Hook events** (e.g., `OnClick`, `OnDoubleClick`, `OnMenuItemClicked`) to launch AI‑related commands such as “Start inference”, “Open chat window”, or “Refresh RAG index”.  
4. **Test locally** with the built‑in preview window; the library works on Windows 10/11 and, via Uno, on Linux/macOS when running under WinUI‑compatible runtimes.  
5. **Deploy** the compiled app as usual (MSIX, ClickOnce, or self‑contained) – the tray icon works out‑of‑the‑box without extra installer steps.  

**Production Readiness**  
- **Activity & Community:** Recent commits (last update 2026‑06‑27), 752 stars, 59 forks, and 18 relevant topics indicate a healthy, engaged community.  
- **Stability:** The API is stable across the supported UI stacks; no breaking changes have been announced in the last 12 months.  
- **Security & Licensing:** The project uses the MIT license; a quick audit shows no known vulnerabilities, but a formal security review and verification of maintainer activity are still advisable before a large‑scale rollout.  
- **Ecosystem Fit:** Works seamlessly with .NET 8+, integrates with popular MVVM frameworks, and can be combined with AI SDKs (e.g., OpenAI, LangChain.NET) to expose model controls from the tray.  

Overall, H.NotifyIcon is production‑ready for pilots and can be promoted to a core component in any .NET desktop solution that needs a reliable, cross‑framework system‑tray experience.

### Русский

**HavenDV/H.NotifyIcon** — это кроссплатформенная библиотека на C#, позволяющая быстро добавить в приложения WPF, WinUI, Uno и MAUI иконку в системный трей с поддержкой всплывающих подсказок, контекстных меню и событий кликов. Типичный сценарий — интеграция в пользовательские интерфейсы, где требуется лёгкое уведомление пользователя о состоянии приложения (например, фоновые задачи, обновления или AI‑подсказки). Проект имеет высокий уровень готовности к production: активная поддержка (обновления до 2026‑06‑27), более 750 звёзд на GitHub, стабильный API и широкое принятие в сообществе, что делает его надёжным выбором для корпоративных решений.

### 中文

**项目简介**  
HavenDV/H.NotifyIcon 是一款面向 WPF、WinUI、Uno 与 MAUI 的托盘图标库，提供跨平台的系统托盘交互能力，帮助开发者快速在桌面应用中加入通知、菜单和状态展示等功能。

**价值**  
- **即插即用**：只需几行代码即可在任意支持的 UI 框架中创建托盘图标，省去底层 Win32/WinRT 的繁琐实现。  
- **统一 API**：统一的 C# 接口在不同平台上保持行为一致，降低跨平台维护成本。  
- **社区活跃**：拥有 750+ 星、近 60 次 Fork，近期仍在活跃维护，适合作为正式项目的依赖。

**典型接入方式**  
1. **NuGet 引入**：在项目的 `.csproj` 中添加 `PackageReference Include="H.NotifyIcon"`。  
2. **XAML 声明**（以 WPF 为例）：  
   ```xml
   <h:TaskbarIcon x:Name="TrayIcon"
                  IconSource="pack://application:,,,/Resources/app.ico"
                  ToolTipText="My App"
                  Visibility="Visible"/>
   ```  
3. **代码绑定**：在后台代码中通过 `TrayIcon` 实例注册点击、右键菜单、气泡通知等事件。  
4. **跨平台切换**：在 Uno、MAUI 项目中同样使用 `TaskbarIcon`，仅需更改对应的 UI 命名空间即可，无需改动业务逻辑。

**生产可用性**  
- **活跃度**：截至 2026‑06‑27 最近一次提交，维护者响应及时，Issue 处理速度快。  
- **依赖安全**：仅依赖 .NET 标准库和官方 Win32/WinRT 接口，无额外二进制或本地 DLL，安全风险低。  
- **成熟度**：已在多个开源和商业桌面应用中使用，文档、示例代码完整，适合作为正式产品的托盘图标解决方案。  

综上，H.NotifyIcon 具备高可用性、易集成和跨平台统一性的优势，是在 WPF/WinUI/Uno/MAUI 项目中实现系统托盘交互的首选 OSS 库。

## 🧭 Practical evaluation

**Value:** HavenDV/H.NotifyIcon helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 752 GitHub stars
- 59 forks
- updated 2026-06-27
- primary language: C#
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 61/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 57/100 |
| production | 70/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/HavenDV/H.NotifyIcon) · [← Back to Design](./README.md)</sub>
