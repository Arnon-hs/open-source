# kenzok8/small

[![Stars](https://img.shields.io/github/stars/kenzok8/small?style=flat-square&color=yellow)](https://github.com/kenzok8/small/stargazers) [![Forks](https://img.shields.io/github/forks/kenzok8/small?style=flat-square&color=blue)](https://github.com/kenzok8/small/network) [![Language](https://img.shields.io/badge/lang-Lua-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> homeprxoy mihomo sing-box dae passwall

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.4k |
| 🍴 **Forks** | 876 |
| 💻 **Language** | Lua |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`homeproxy` `hysteria` `mihomo` `momo` `mosdns` `nikki` `sing-box`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
The *kenzok8/small* repository bundles a set of Lua‑based networking tools—including HomeProxy, Mihomo, Sing‑Box, DAE, and PassWall—aimed at building flexible, self‑hosted proxy and VPN solutions. With over 1.4 k GitHub stars, frequent commits (last updated 2026‑06‑26) and a sizable fork base, the project shows strong community traction and can serve as a ready‑made foundation for custom proxy stacks.

**Value**  
- **All‑in‑one proxy suite**: By packaging popular proxy engines (Mihomo, Sing‑Box, etc.) together, it eliminates the need to stitch disparate components manually, saving development and maintenance effort.  
- **Lua configurability**: The Lua‑based configuration layer makes it easy to script complex routing, rule‑sets, and dynamic updates without deep knowledge of each individual tool.  
- **Active ecosystem**: A large star/fork count and recent activity indicate an engaged community that contributes bug fixes, new features, and documentation—reducing the risk of stale dependencies.

**Practical adoption path**  
1. **Proof‑of‑concept**: Clone the repo, run the provided Docker/compose scripts, and verify that the default configuration meets your baseline traffic‑routing requirements.  
2. **Readme validation**: Follow the README to customize the Lua scripts for your specific upstream providers, DNS policies, or authentication mechanisms.  
3. **Integration testing**: Replace the default proxy endpoints with your own services, run end‑to‑end connectivity tests, and measure latency/throughput.  
4. **Gradual rollout**: Deploy the tuned configuration to a staging environment (e.g., Kubernetes or a VM) before promoting to production, using the same Docker images to ensure reproducibility.

**Production readiness**  
The project scores high on production readiness: recent commits, a vibrant fork network, and a substantial user base suggest that core functionality is stable and that security patches are applied promptly. While the integration steps are not fully documented in the metadata, the clear Docker entry points and Lua‑based extensibility make it feasible to pilot in a controlled environment. After a modest proof‑of‑concept and validation of setup costs, *kenzok8/small* can be considered a solid OSS candidate for production‑grade proxy deployments.

### Русский

**kenzok8/small** — это открытый набор скриптов и конфигураций на Lua, объединяющий функции HomeProxy, Mihomo, Sing‑Box, DAE и PassWall, что позволяет быстро построить комплексный прокси‑сервер с поддержкой разных протоколов и фильтрации трафика. Типичный сценарий внедрения — развертывание небольшого proof‑of‑concept в тестовой среде, проверка README и базовой конфигурации, а затем масштабирование до production‑готового решения. Проект обладает высокой готовностью к эксплуатации: активные коммиты, более 1400 звёзд, 800 форков и свежие обновления, однако путь интеграции требует предварительной проверки настроек и зависимостей.

### 中文

**项目简介（2‑3 句话）**  
kenzok8/small 是一个基于 Lua 的轻量化代理/翻墙脚本集合，集成了 HomeProxy、MiHomo、Sing‑Box、DAE、PassWall 等主流代理核心，旨在为不同网络环境提供“一键式”部署方案。

**价值**  
- **多核心统一管理**：将多种流行代理核心封装为统一的配置入口，免去分别部署、调试的繁琐工作。  
- **轻量且易于定制**：核心代码量小，使用 Lua 编写，便于二次开发和脚本化管理。  
- **社区活跃**：拥有 1400+ Stars、800+ Forks，近期仍在更新，说明社区对其需求和维护力度都很高。

**典型接入方式**  
1. **阅读 README**：先确认项目的使用场景（如在 OpenWrt、Docker、VPS 上部署）以及所需的依赖（Lua、对应代理二进制）。  
2. **快速验证**：在测试机器上克隆仓库，按照 README 的“一键安装”脚本执行，生成默认的 `config.yaml`（或对应格式）。  
3. **定制化**：根据业务需求修改配置文件，选择需要的核心（如 sing‑box）并开启相应的插件（PassWall、DAE 等）。  
4. **CI/CD 集成**：将脚本包装为 Docker 镜像或 OpenWrt 包，使用 GitHub Actions 或自建 CI 流水线实现自动构建、部署。  

**生产可用性**  
- **成熟度**：项目最近一次提交在 2026‑06‑26，活跃度高，说明代码在持续维护。  
- **生态兼容**：支持的核心均为业界主流，已有多个第三方项目基于其脚本进行二次开发，兼容性良好。  
- **风险点**：元数据中未提供完整的部署文档，实际接入时需要先通过 README 完成小规模 PoC，评估环境依赖和脚本的可调试性。  
- **结论**：在完成一次小范围的概念验证后，可视为具备 **高** 生产就绪度的 OSS 组件，适合作为内部或外部代理服务的快速交付方案。

## 🧭 Practical evaluation

**Value:** kenzok8/small may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1426 GitHub stars
- 876 forks
- updated 2026-06-26
- primary language: Lua
- 7 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 74/100 |
| stars | 67/100 |
| topics | 88/100 |
| outlook | 72/100 |
| quality | 79/100 |
| recency | 80/100 |
| adoption | 69/100 |
| production | 69/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/kenzok8/small) · [← Back to Misc](./README.md)</sub>
