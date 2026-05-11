# multipath-tcp/mptcp_net-next

[![Stars](https://img.shields.io/github/stars/multipath-tcp/mptcp_net-next?style=flat-square&color=yellow)](https://github.com/multipath-tcp/mptcp_net-next/stargazers) [![Forks](https://img.shields.io/github/forks/multipath-tcp/mptcp_net-next?style=flat-square&color=blue)](https://github.com/multipath-tcp/mptcp_net-next/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Development version of the Upstream MultiPath TCP Linux kernel 🐧

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 400 |
| 🍴 **Forks** | 56 |
| 💻 **Language** | C |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`c` `linux` `linux-kernel` `mptcp` `upstream`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *multipath‑tcp/mptcp_net‑next* repository hosts the development branch of the upstream MultiPath TCP (MPTCP) implementation for the Linux kernel. It provides the latest kernel‑level code and patches needed to enable MPTCP support, allowing a single connection to use multiple network paths for higher throughput and resilience. The project is actively maintained (last update 2026‑05‑11) and written in C, with modest community traction (≈ 400 stars).

**Value Proposition**  
MPTCP extends standard TCP by transparently splitting traffic across several interfaces (e.g., Wi‑Fi + cellular), which can improve performance for mobile devices, data‑center servers, and IoT gateways. By integrating the *mptcp_net‑next* source tree into a custom kernel build, teams can experiment with path‑aware load balancing, fail‑over, and bandwidth aggregation without modifying applications.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1. **Read the README & docs** | Verify build instructions, kernel version compatibility, and required kernel config flags (`CONFIG_MPTCP`). | Guarantees you can compile the kernel with MPTCP enabled. |
| 2. **Create a small PoC** | Build a custom kernel (or kernel module) for a test node, enable `CONFIG_MPTCP=y`, and run `mptcpize` on a simple client/server pair. | Confirms the integration workflow and isolates any build‑time dependencies. |
| 3. **Validate with real interfaces** | Attach two network interfaces (e.g., Ethernet + LTE) and use `ip mptcp` utilities to monitor subflows. | Demonstrates the core benefit—multi‑path usage—in a controlled environment. |
| 4. **Automate in CI** | Add the kernel build and a basic MPTCP test suite to your CI pipeline. | Ensures future kernel updates don’t break the integration. |
| 5. **Scale to staging** | Deploy the custom kernel on a subset of production servers or edge devices and run workload‑level benchmarks. | Provides performance and reliability data before full rollout. |

**Production‑Readiness Assessment**  
- **Maturity**: Development branch (‑next) – contains the newest features but may also include experimental changes.  
- **Stability**: Medium; suitable for prototypes, internal services, or environments where you control the kernel upgrade cycle.  
- **Dependencies**: Requires a custom‑compiled Linux kernel and appropriate user‑space tools (`mptcp-tools`). No external libraries, but careful version matching with the base kernel is essential.  
- **Maintenance**: Active commits and a modest community suggest reasonable long‑term support, yet you’ll need to track upstream merges and test each kernel release.  

**Conclusion**  
*mptcp_net‑next* offers a concrete way to bring cutting‑edge MPTCP capabilities into Linux‑based systems, making it valuable for teams exploring multi‑path networking. Start with a minimal proof‑of‑concept kernel build, validate the multi‑path behavior, and automate testing before considering broader deployment; with proper validation, it can be used in production for internal or edge workloads, though a full production rollout should include ongoing monitoring of upstream changes and a clear upgrade strategy.

### Русский

**multipath-tcp/mptcp_net-next** — это актуальная ветка разработки ядра Linux с поддержкой MultiPath TCP, позволяющая использовать несколько сетевых путей одновременно для повышения пропускной способности и отказоустойчивости. Подходит для прототипов и внутренних сервисов, где требуется экспериментировать с MPTCP: рекомендуется начать с небольшого proof‑of‑concept, проверив README и собрать ядро в тестовой среде. Готовность к production — средняя: код стабилен, но требуется оценить затраты на интеграцию, зависимости и последующее обслуживание.

### 中文

**项目简介（2‑3 句话）**  
`multipath-tcp/mptcp_net-next` 是 MultiPath TCP（MPTCP）在 Linux 内核的开发分支，提供最新的协议实现和内核补丁，适用于需要同时使用多条网络路径提升吞吐和可靠性的场景。  

**价值**  
- **性能提升**：通过聚合多条链路，实现更高的带宽和更好的容错能力，适合高并发、移动或跨域业务。  
- **前沿特性**：紧跟上游 MPTCP 开发进度，能够在实验或原型阶段快速尝试最新协议改进。  
- **社区支撑**：已有 400+ Stars、56 Forks，活跃的维护者和 issue 反馈，便于获取帮助和贡献代码。  

**典型接入方式**  
1. **克隆源码**：`git clone https://github.com/multipath-tcp/mptcp_net-next.git`。  
2. **编译内核**  
   - 在现有内核源码树中使用 `make menuconfig` 启用 `CONFIG_MPTCP`（或直接将 `net/mptcp/` 目录拷贝进内核源码）。  
   - 编译并安装新内核或内核模块（`make -j$(nproc) && make modules_install && make install`）。  
3. **验证**  
   - 通过 `sysctl -w net.mptcp.mptcp_enabled=1` 开启 MPTCP。  
   - 使用 `mptcpize` 或 `iperf3 -M mptcp` 等工具在两端创建多路径连接进行功能和性能验证。  
4. **小范围 PoC**：在测试环境或内部 CI 中先跑一次完整的编译‑部署‑验证流程，确认与现有网络栈兼容后再推广。  

**生产可用性**  
- **成熟度**：属于开发分支（`net-next`），功能相对完整但仍可能出现 API 变动或未完全回归的 bug。适合 **原型、内部平台或对 MPTCP 有明确需求的业务**，不建议直接在面向外部用户的生产环境中全量使用。  
- **准备工作**：在投入生产前，需要  
  - 完整的回归测试（包括链路切换、拥塞控制等场景）。  
  - 与现有网络设备、负载均衡和防火墙的兼容性验证。  
  - 制定回滚方案（保留可用的传统内核）。  
- **维护成本**：需要持续跟进上游更新并在每次内核升级时重新编译、验证。若团队具备 Linux 内核维护经验，维护成本可接受；否则建议使用已发布的稳定内核或社区提供的二进制包。  

综上，`multipath-tcp/mptcp_net-next` 对于想要在内部实验或构建高可靠性网络服务的团队价值明显，接入方式以源码编译为主，生产使用需做好充分的测试和回滚准备，适合作为 **原型/内部业务** 的加速器，而非直接面向客户的生产环境。

## 🧭 Practical evaluation

**Value:** multipath-tcp/mptcp_net-next may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 400 GitHub stars
- 56 forks
- updated 2026-05-11
- primary language: C
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 55/100 |
| topics | 63/100 |
| outlook | 73/100 |
| quality | 73/100 |
| recency | 100/100 |
| adoption | 52/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/multipath-tcp/mptcp_net-next) · [← Back to Misc](./README.md)</sub>
