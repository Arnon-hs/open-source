# nix-community/nix-ld

[![Stars](https://img.shields.io/github/stars/nix-community/nix-ld?style=flat-square&color=yellow)](https://github.com/nix-community/nix-ld/stargazers) [![Forks](https://img.shields.io/github/forks/nix-community/nix-ld?style=flat-square&color=blue)](https://github.com/nix-community/nix-ld/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-43%2F100-brightgreen?style=flat-square)](#)

> Run unpatched dynamic binaries on NixOS [maintainer=@Mic92]

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.6k |
| 🍴 **Forks** | 25 |
| 💻 **Language** | Rust |
| 📈 **Score** | 43/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`build-with-buildbot` `managed-by-renovate`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*nix-community/nix‑ld* is a Rust‑based utility that enables you to run unpatched dynamic binaries on NixOS without manually tweaking the system’s linker or library paths. By automating the otherwise repetitive steps required to make foreign binaries work in the Nix ecosystem, it turns a one‑off debugging chore into a repeatable part of your workflow.  

**Value**  
The tool eliminates the tedious, error‑prone manual configuration that developers normally perform when trying to execute pre‑compiled binaries on NixOS. This saves time, reduces friction when integrating third‑party tools, and makes it easier to build reproducible pipelines that involve legacy or closed‑source executables.  

**Practical Adoption Path**  

| Step | Action |
|------|--------|
| 1️⃣  | Clone the repository and run the provided examples on a test NixOS machine to verify that the binary you need can be launched with `nix-ld`. |
| 2️⃣  | Integrate the `nix-ld` wrapper into your build scripts or CI pipelines (e.g., `nix run github:nix-community/nix-ld -- <binary>`). |
| 3️⃣  | Add a small validation stage that checks the expected libraries are found; this catches edge cases early. |
| 4️⃣  | Document the wrapper usage in your project’s README and ship the binary as part of a reproducible Nix flake. |
| 5️⃣  | Once the workflow is stable, promote the flake to your internal or production Nix channel. |

Because the project’s metadata provides few integration hints, the manual “smoke‑test” in step 1 is essential to confirm that the specific binaries you rely on are supported.  

**Production Readiness**  
The project scores a medium readiness level: it has strong community interest (≈ 1.6 k stars, 25 forks) and is actively maintained (last update 2026‑05‑11). It is suitable for prototypes, internal tooling, or any environment where you can afford a short validation phase. Before moving to production, perform a dependency audit (ensure the required glibc/libstdc++ versions are available) and set up monitoring for any future changes in the upstream `nix-ld` repository that could affect your workflow. Once those checks are in place, the utility can be considered reliable for regular use.

### Русский

**nix-ld** — это open‑source утилита (Rust) для запуска непатченных динамических бинарников в NixOS, позволяющая автоматизировать рутинные шаги, связанные с подготовкой окружения и подключением зависимостей. Типичный сценарий — интеграция в CI/CD или внутренний пайплайн, где требуется быстро и надёжно запускать сторонние бинарники без ручного вмешательства, а затем связывать их с другими инструментами в повторяемый workflow. Проект находится на среднем уровне готовности к production: подходит для прототипов и внутренних сервисов, но перед масштабным внедрением стоит проверить путь интеграции и оценить затраты на настройку.

### 中文

**项目简介**  
`nix-community/nix-ld` 是一个用于在 NixOS 上运行未打补丁的动态链接二进制文件的工具，由 @Mic92 维护。它通过在 Nix 环境中自动提供缺失的共享库，使得原本只能在传统 Linux 发行版上运行的二进制程序能够直接在 NixOS 上启动。

**价值**  
- **消除手动补丁**：无需手动下载、编译或拷贝共享库，极大降低了运维人员的重复劳动。  
- **提升可重复性**：所有依赖都由 Nix 包管理器声明并固定，保证在不同机器、不同时间得到完全相同的运行环境。  
- **加速原型与内部工具开发**：开发者可以快速在 NixOS 上验证第三方闭源工具或脚本，而不必为兼容性问题费时调试。

**典型接入方式**  
1. **在项目的 `shell.nix` 或 `default.nix` 中引入**  
   ```nix
   { pkgs ? import <nixpkgs> {} }:

   pkgs.mkShell {
     nativeBuildInputs = [ pkgs.nix-ld ];
     # 需要运行的二进制文件路径
     LD_LIBRARY_PATH = pkgs.nix-ld.run { program = ./my-binary; };
   }
   ```
2. **在 CI/CD 流水线中使用**：在 GitHub Actions、GitLab CI 等环境的步骤里先 `nix-shell -p nix-ld --run "nix-ld ./binary"`，即可确保每次构建都使用相同的库集合。  
3. **作为系统服务**：在 NixOS 配置 (`configuration.nix`) 中加入 `services.nix-ld.enable = true;`，让所有用户的动态链接请求自动走 `nix-ld`。

**生产可用性**  
- **成熟度**：GitHub ★1618，近期（2026‑05‑11）仍在活跃维护，主要实现语言为 Rust，社区活跃度较高。  
- **适用场景**：适合原型、内部工具或需要快速迁移闭源二进制到 NixOS 的场景。  
- **风险与注意事项**：元数据中对外部依赖的描述较少，首次接入前需要手动验证所需的共享库是否完整；在大规模生产环境使用前建议做好依赖审计和回滚方案。  
- **总体评估**：**中等**（Medium）——在经过依赖检查和维护成本评估后，可用于生产环境，尤其是对可重复性要求高且对手动补丁成本敏感的团队。

## 🧭 Practical evaluation

**Value:** nix-community/nix-ld helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1618 GitHub stars
- 25 forks
- updated 2026-05-11
- primary language: Rust
- 2 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 68/100 |
| topics | 25/100 |
| outlook | 43/100 |
| quality | 50/100 |
| recency | 20/100 |
| adoption | 59/100 |
| production | 44/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/nix-community/nix-ld) · [← Back to Misc](./README.md)</sub>
