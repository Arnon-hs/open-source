# 0xflux/Hells-Hollow

[![Stars](https://img.shields.io/github/stars/0xflux/Hells-Hollow?style=flat-square&color=yellow)](https://github.com/0xflux/Hells-Hollow/stargazers) [![Forks](https://img.shields.io/github/forks/0xflux/Hells-Hollow?style=flat-square&color=blue)](https://github.com/0xflux/Hells-Hollow/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Hells Hollow Windows 11 Rootkit technique to Hook the SSDT via Alt Syscalls

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 238 |
| 🍴 **Forks** | 27 |
| 💻 **Language** | Rust |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-07-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`alt-syscalls` `alternative-syscalls` `exploit` `kernel` `kernel-exploit` `malware` `rootkit` `ssdt` `ssdt-hook` `ssdt-hooking` `ssdt-plug` `syscalls`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
Hells‑Hollow is a Rust‑based proof‑of‑concept rootkit for Windows 11 that demonstrates how to hijack the System Service Dispatch Table (SSDT) using “alternative syscalls.” The project showcases a low‑level hooking technique that can be useful for security research, red‑team exercises, or defensive tooling that needs to understand or detect SSDT manipulation.

**Value**  
- **Research & Teaching:** Provides a concrete, open‑source implementation of a rarely‑documented SSDT‑hooking method, helping analysts study kernel‑mode attack surfaces and develop detection signatures.  
- **Tool Building:** Serves as a building block for custom red‑team utilities or defensive agents that need to monitor or emulate kernel‑level behavior on Windows 11.  
- **Community Insight:** With 238 stars and active maintenance (last commit 2026‑07‑13), the codebase is relatively mature for a niche security technique.

**Practical Adoption Path**  
1. **Read the README & Verify Build Steps:** Clone the repo, follow the Rust toolchain setup, and compile the sample driver on a test Windows 11 VM.  
2. **Proof‑of‑Concept Test:** Deploy the built driver in a controlled environment to confirm the SSDT hook works as described (e.g., intercept a known syscall).  
3. **Integration Scaffold:** Wrap the driver logic in a minimal API or CLI that fits your workflow (e.g., a PowerShell module that loads/unloads the driver).  
4. **Extend or Harden:** Replace the demo payload with your own logic, add logging, and implement proper signing/driver‑package requirements for your target deployment scenario.

**Production Readiness**  
- **Maturity:** Medium. The code is functional and maintained, but it is still a research prototype; it lacks production‑grade features such as robust error handling, secure signing pipelines, and comprehensive testing.  
- **Dependencies:** Pure Rust with standard Windows driver toolchains, but you’ll need a signed driver or test‑signing mode for deployment on modern Windows 11 builds.  
- **Risk Mitigation:** Before moving to production, perform a security audit of the driver code, verify compatibility with the specific Windows 11 build you target, and establish a clear rollback/clean‑up procedure to avoid system instability.  

In short, Hells‑Hollow is a valuable starting point for teams that need to explore SSDT hooking on Windows 11, but it should be introduced via a small, isolated proof‑of‑concept and hardened before any production or internal‑tool use.

### Русский

**0xflux/Hells‑Hollow** — open‑source rootkit для Windows 11, реализующий перехват SSDT через альтернативные системные вызовы на Rust. Подойдёт для быстрого прототипа исследований безопасности или внутреннего тестирования, если README и текущая активность проекта совпадают с вашими задачами; рекомендуется начать с небольшого proof‑of‑concept, проверив процесс сборки и зависимости. Готовность к production — средняя: проект достаточно зрелый (238 звёзд, 27 форков, обновление 13 июля 2026), но путь интеграции не очевиден и требует предварительной оценки затрат на настройку и поддержку.

### 中文

**价值**  
0xflux/Hells‑Hollow 实现了在 Windows 11 上通过 “Alt Syscalls” Hook SSDT 的 rootkit 技术，能够在内核层面拦截、修改或隐藏系统调用。对安全研究、红队演练以及防御方案的逆向分析都有直接的参考价值；同时，它提供了一个基于 Rust 编写的现代化实现，可供学习和二次开发。

**典型接入方式**  
1. **阅读并验证 README**：先确认项目的编译说明、依赖（如 `rustc`、`cargo`、Windows SDK）以及所需的签名/驱动加载方式。  
2. **小规模 PoC**：在受控的测试机器或虚拟机中编译驱动（`cargo build --release`），使用 `sc create` / `sc start` 或 `pnputil` 加载，验证 SSDT 是否被成功 Hook（可通过 `WinDbg`、`Process Monitor` 等工具观察）。  
3. **与现有工具链集成**：如果已有自研的内核监控或防御框架，只需在加载阶段调用 Hells‑Hollow 的初始化函数，或在驱动入口处插入其 Hook 逻辑；代码层面保持 Rust‑C FFI 边界即可。  
4. **自动化测试**：编写 CI 脚本（GitHub Actions、Azure Pipelines）完成编译、签名、加载以及功能验证，确保每次代码改动不会破坏 Hook 行为。

**生产可用性**  
- **成熟度**：GitHub ★238、Fork 27，最近一次更新为 2026‑07‑13，说明社区仍在活跃维护。  
- **适用场景**：适合原型验证、内部红队工具或安全实验室的内部项目；不建议直接用于面向客户的生产环境。  
- **风险与准备工作**  
  - **集成成本**：项目文档较简略，需自行梳理驱动签名、加载权限（需要管理员或测试签名证书）以及与现有内核模块的兼容性。  
  - **维护负担**：依赖 Rust 编译链和 Windows SDK，升级时需同步检查兼容性。  
  - **合规性**：Rootkit 技术在多数企业环境属于高风险操作，需通过法律与安全合规审查后方可部署。  

**结论**：在经过充分的 PoC 验证并完成签名、权限、兼容性等前置工作后，Hells‑Hollow 可作为内部安全研发的强力原型工具使用；但在正式生产环境部署前，建议进行完整的安全评估、代码审计以及维护流程的建立。

## 🧭 Practical evaluation

**Value:** 0xflux/Hells-Hollow may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 238 GitHub stars
- 27 forks
- updated 2026-07-13
- primary language: Rust
- 14 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 36/100 |
| stars | 51/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 76/100 |
| recency | 100/100 |
| adoption | 47/100 |
| production | 73/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/0xflux/Hells-Hollow) · [← Back to Misc](./README.md)</sub>
