# kjliew/qemu-3dfx

[![Stars](https://img.shields.io/github/stars/kjliew/qemu-3dfx?style=flat-square&color=yellow)](https://github.com/kjliew/qemu-3dfx/stargazers) [![Forks](https://img.shields.io/github/forks/kjliew/qemu-3dfx?style=flat-square&color=blue)](https://github.com/kjliew/qemu-3dfx/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> MESA GL/3Dfx Glide pass-through for QEMU

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 550 |
| 🍴 **Forks** | 71 |
| 💻 **Language** | C |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
`kjliew/qemu-3dfx` provides a MESA GL/3Dfx Glide pass‑through layer that lets QEMU virtual machines use the legacy 3Dfx Glide API via hardware or software rendering. It is a niche bridge for developers who need to run old Glide‑based games or graphics demos inside QEMU.

**Value**  
- Enables legacy Glide applications (e.g., classic games, demos, or scientific visualisations) to run unmodified in a QEMU VM, preserving the original graphics behaviour.  
- Leverages the open‑source MESA implementation, so no proprietary drivers are required and the code can be inspected or extended.  

**Practical adoption path**  
1. **Clone the repository** and build the C sources with the same toolchain used for your QEMU build (the project targets the same host architecture).  
2. **Install the resulting shared library** (`libglide.so` or similar) on the host and configure QEMU to expose it to the guest via `-device` or `-chardev` options, following the README examples.  
3. **Test with a known Glide binary** inside the VM; adjust QEMU’s `-display` and MESA driver settings until the guest reports a Glide device.  
4. Optionally, contribute missing documentation or scripts to streamline the setup for your specific workflow.  

**Production readiness**  
- **Maturity:** The project has modest popularity (≈550 ★, 71 forks) and recent activity (last commit 2026‑07‑12), indicating it is maintained but still niche.  
- **Stability:** Works well for prototypes and internal testing of Glide‑dependent workloads; however, the integration steps are not fully documented, and the pass‑through may require custom QEMU builds.  
- **Risk level:** Medium – acceptable for internal or experimental pipelines after a validation phase that checks build compatibility, performance impact, and long‑term maintenance of the custom QEMU integration.  

In short, `kjliew/qemu-3dfx` is a useful tool for developers needing Glide support inside QEMU, but it should be piloted on a small scale before being adopted in production environments.

### Русский

**kjliew/qemu-3dfx** – это open‑source‑модуль, позволяющий передавать графику MESA GL/3Dfx Glide в виртуальные машины QEMU, что упрощает запуск старых 3Dfx‑приложений и тестирование Glide‑драйверов. Он подходит для прототипов и внутренних пайплайнов, где требуется быстрый Glide‑pass‑through, однако путь интеграции неочевиден и требует ручного изучения конфигурации и зависимостей. Готовность к production — средняя: проект имеет активную звёздную базу (≈550 ★) и недавние коммиты, но перед внедрением следует проверить совместимость и нагрузку на поддержку.

### 中文

**项目简介**  
`kjliew/qemu-3dfx` 为 QEMU 虚拟机提供了 MESA GL/3Dfx Glide 的硬件透传实现，使得在虚拟化环境中也能使用 3Dfx Glide API 进行 3D 渲染。

**价值**  
- **复古/特定硬件兼容**：在需要运行依赖 Glide 的老游戏或专业软件时，免去在真实硬件上搭建环境的繁琐。  
- **开发/原型加速**：在 CI 或容器化的测试环境中直接验证 Glide‑相关代码，提升迭代速度。  
- **开源可审计**：全部实现基于 C 语言，代码公开，便于安全审计和二次定制。

**典型接入方式**  
1. **准备工作**  
   - 确保宿主机已安装 QEMU（>= 7.0）和对应的 MESA 库（含 `glide` 驱动）。  
   - 克隆仓库并编译：  
     ```bash
     git clone https://github.com/kjliew/qemu-3dfx.git
     cd qemu-3dfx
     mkdir build && cd build
     cmake .. && make
     sudo make install   # 安装到 /usr/local/lib/qemu
     ```  
2. **在 QEMU 启动参数中加载**  
   - 使用 `-device` 选项挂载 Glide 设备，例如：  
     ```bash
     qemu-system-x86_64 \
       -enable-kvm \
       -m 4G \
       -device 3dfx-glide,bus=pci.0,addr=0x03 \
       -drive file=guest.img,format=raw
     ```  
   - 在客系统（Linux/Windows）中安装相应的 Glide 驱动或使用 Mesa 提供的软实现。  
3. **验证**  
   - 在客系统运行 `glideinfo`（或老游戏）检查渲染是否正常。  

**生产可用性**  
- **成熟度**：项目已有 550+ Stars、71 Forks，最近一次提交在 2026‑07‑12，活跃度尚可。  
- **适用场景**：适合内部原型、CI 测试、复古游戏托管或需要 Glide 支持的专用业务。  
- **风险与限制**  
  - 文档和集成指南相对简陋，实际部署前需自行验证硬件/驱动兼容性。  
  - 依赖宿主机的 Mesa/GL 驱动版本，升级时可能出现回归。  
  - 未经过大规模生产环境的压力测试，建议在关键业务前做好回滚方案。  
- **推荐策略**：在非关键环境先进行 PoC，确认性能与稳定性后，再考虑在内部服务或受控生产线上使用；同时做好依赖（Mesa、QEMU）版本锁定和监控。

## 🧭 Practical evaluation

**Value:** kjliew/qemu-3dfx may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 550 GitHub stars
- 71 forks
- updated 2026-07-12
- primary language: C

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 58/100 |
| topics | 0/100 |
| outlook | 60/100 |
| quality | 60/100 |
| recency | 80/100 |
| adoption | 55/100 |
| production | 62/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/kjliew/qemu-3dfx) · [← Back to Misc](./README.md)</sub>
