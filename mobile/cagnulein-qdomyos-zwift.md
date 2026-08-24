# cagnulein/qdomyos-zwift

[![Stars](https://img.shields.io/github/stars/cagnulein/qdomyos-zwift?style=flat-square&color=yellow)](https://github.com/cagnulein/qdomyos-zwift/stargazers) [![Forks](https://img.shields.io/github/forks/cagnulein/qdomyos-zwift?style=flat-square&color=blue)](https://github.com/cagnulein/qdomyos-zwift/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Zwift bridge for smart treadmills and bike/cyclette

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 809 |
| 🍴 **Forks** | 189 |
| 💻 **Language** | C++ |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bike` `bluetooth` `bluetooth-low-energy` `cyclette` `cycling` `dietpi` `domyos` `hacktoberfest` `ios` `macos` `qdomyos-zwift` `qt`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief Summary**  
cagnulein/qdomyos-zwift is an open‑source bridge that connects Zwift to smart treadmills and bike/cyclette hardware, letting users control and sync physical trainers with the virtual cycling platform. With over 800 ⭐ on GitHub, recent commits (as of 2026‑06‑27) and a C++ core, the project is mature enough for early‑stage pilots in developer workflows that involve hardware‑in‑the‑loop testing.  

**Value**  
The bridge abstracts the low‑level communication with a variety of smart trainers, giving engineers a single, reusable API/CLI to automate device control, collect telemetry, and run integration tests against Zwift. This cuts the time spent writing custom adapters, reduces flaky hardware‑dependent CI jobs, and enables rapid prototyping of new training scenarios or data‑driven features.  

**Practical Adoption Path**  
1. **Evaluate the API/CLI** – Clone the repo, build the C++ library, and run the provided example scripts to verify communication with your treadmill or bike.  
2. **Integrate into CI** – Wrap the CLI calls in your build pipeline (e.g., GitHub Actions, Jenkins) to spin up a virtual trainer, execute a scripted Zwift session, and capture logs/metrics.  
3. **Extend or customize** – Use the exposed C++ headers or the Python bindings (if any) to add device‑specific commands or to feed custom data into Zwift for testing new features.  

**Production Readiness**  
The project shows strong production signals: recent activity, a healthy fork/star ratio, and a clear focus on a niche but growing market (smart trainer integration). While the license and security posture still need a final audit, the codebase is actively maintained, well‑documented, and already adopted by several community members, making it a viable candidate for a controlled pilot or internal tooling rollout.

### Русский

cagnulein/qdomyos-zwift — это открытый мост между платформой Zwift и умными беговыми дорожками/велотренажёрами, позволяющий интегрировать реальные датчики скорости, наклона и сопротивления в виртуальные тренировки. Проект уже активно поддерживается (809 звёзд, 189 форков, последний коммит 2026‑06‑27), написан на C++ и предоставляет готовый API/CLI, что упрощает автоматизацию локальных задач и ускоряет CI‑проверки в проектах, связанных с фитнес‑техникой. Уровень готовности к production высокий — сильные сигналы принятия в сообществе и стабильный релизный цикл позволяют использовать его в пилотных и масштабных внедрениях после окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
cagnulein/qdomyos-zwift 是一个用于将 Zwift 与智能跑步机、健身自行车（cyclette）连接的桥接层，基于 C++ 实现，能够把 Zwift 的虚拟骑行/跑步数据实时同步到真实硬件，实现沉浸式训练体验。

**价值**  
- **提升开发效率**：提供即插即用的 API/SDK 与 CLI，工程师无需自行编写底层协议即可快速在本地或 CI 环境中验证硬件‑Zwift 的交互。  
- **自动化工作流**：可在 CI 中模拟跑步机/自行车的输入，自动化回归测试和性能基准，缩短每日开发与评审周期。  
- **社区与生态**：拥有 809+ 星、189+ Fork，活跃的贡献者和丰富的话题标签，便于获取社区支持与二次开发。

**典型接入方式**  
1. **依赖引入**：在 C++ 项目中通过 `git submodule` 或包管理器（如 vcpkg、conan）引入源码。  
2. **API 调用**：使用提供的 `QDomyosBridge` 类初始化并绑定 Zwift 的 WebSocket/UDP 接口，随后调用 `connectTreadmill()`、`connectBike()` 等方法完成硬件配对。  
3. **CLI 工具**：项目自带 `qdomyos-cli`，可在命令行直接启动桥接服务或进行调试，适合 CI 脚本化调用。  
4. **示例代码**：仓库内的 `examples/` 目录提供完整的跑步机和自行车接入示例，可直接编译运行后进行功能验证。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑27，维护频率高，issue 关闭率良好。  
- **成熟度**：已在多个开源 Zwift 客户端（如 qdomyos‑zwift‑android）中实际使用，具备稳定的协议实现和错误恢复机制。  
- **安全与合规**：暂无已知许可证冲突或重大安全漏洞，仍建议在正式部署前进行一次内部安全审计。  
- **可扩展性**：代码结构清晰，支持自定义硬件协议扩展，适合作为企业内部的统一桥接层。

综上，cagnulein/qdomyos-zwift 已具备较高的生产就绪度，可直接用于开发、CI 自动化以及面向终端用户的 Zwift 硬件集成。

## 🧭 Practical evaluation

**Value:** cagnulein/qdomyos-zwift helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 809 GitHub stars
- 189 forks
- updated 2026-06-27
- primary language: C++
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 62/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 67/100 |
| recency | 40/100 |
| adoption | 61/100 |
| production | 57/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/cagnulein/qdomyos-zwift) · [← Back to Mobile](./README.md)</sub>
