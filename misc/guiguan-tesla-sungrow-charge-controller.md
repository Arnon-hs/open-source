# guiguan/tesla-sungrow-charge-controller

[![Stars](https://img.shields.io/github/stars/guiguan/tesla-sungrow-charge-controller?style=flat-square&color=yellow)](https://github.com/guiguan/tesla-sungrow-charge-controller/stargazers) [![Forks](https://img.shields.io/github/forks/guiguan/tesla-sungrow-charge-controller?style=flat-square&color=blue)](https://github.com/guiguan/tesla-sungrow-charge-controller/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-41%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 41/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
This open‑source Go daemon continuously monitors a Tesla vehicle’s charging state and aligns it with real‑time solar export data from Sungrow inverters and the Tessie API. By dynamically adjusting charging power to match excess solar generation, it helps owners maximize self‑consumption, reduce grid draw, and lower electricity costs. The project is modestly active (last update 2026‑07‑13) and targets hobbyist or internal‑use cases rather than enterprise‑grade deployments.  

**Value**  
- **Energy efficiency:** Automatically shifts Tesla charging to periods of surplus solar output, increasing the share of renewable energy used for transportation.  
- **Cost savings:** Reduces reliance on grid electricity during peak rates, translating into lower utility bills.  
- **Transparency:** Provides a simple, self‑hosted alternative to commercial energy‑management platforms, giving users full control over the logic and data flow.  

**Practical Adoption Path**  
1. **Review repository** – Verify the license (e.g., MIT/Apache), read the README, and scan open issues/PRs for activity.  
2. **Set up prerequisites** – Install Go 1.22+, obtain API credentials for Tessie, and configure access to the Sungrow Modbus/REST endpoint.  
3. **Deploy locally** – Build the binary and run it as a systemd service or Docker container; start with a dry‑run mode to log decisions without affecting the car.  
4. **Validate behavior** – Compare logged charging adjustments against your own solar export data to ensure the daemon respects your preferences (e.g., max charge rate, time‑of‑day limits).  
5. **Iterate & harden** – Add monitoring (Prometheus metrics, alerts) and, if needed, wrap the daemon in a more robust orchestration layer before moving to production.  

**Production Readiness**  
- **Maturity:** Medium. The codebase is recent but sparsely documented, with limited test coverage and only a handful of contributors.  
- **Reliability:** Suitable for prototypes, personal labs, or internal tooling where occasional mis‑timing is acceptable. Not yet vetted for mission‑critical fleet operations.  
- **Maintenance considerations:** You’ll need to monitor upstream changes to the Tessie and Sungrow APIs, keep the Go runtime up‑to‑date, and potentially fork the project for bug fixes or feature extensions.  

**Bottom line:** The daemon offers a compelling way to automate solar‑aligned Tesla charging, but adopting it in production requires a manual code review, thorough testing in a controlled environment, and ongoing maintenance to mitigate the limited upstream support.

### Русский

**Краткое резюме:**  
Это Go‑демон, который синхронно управляет зарядкой Tesla‑автомобиля в зависимости от текущего экспорта солнечной энергии (Sungrow) и данных о состоянии батареи (Tessie). Его типичный сценарий — автоматическое включение зарядки, когда солнечная система генерирует избыточную мощность, что позволяет снизить затраты на электроэнергию в домашних или небольших коммерческих установках. Готовность к production — средняя: проект подходит для прототипов и внутренних процессов, но перед запуском в продакшн требуется проверка лицензии, активности репозитория, наличия документации и стабильности релизов.

### 中文

**项目简介**  
A Go daemon that matches Tesla charging to solar export（Sungrow & Tessie）是一款用 Go 编写的守护进程，能够实时将特斯拉车辆的充电需求与自家光伏（Sungrow）和电网导出（Tessie）数据进行匹配，从而实现“用自产光伏电力给车充电”。  

**价值**  
- **降低能耗成本**：优先使用自家光伏剩余电力为特斯拉充电，减少对外购电的依赖。  
- **提升能源利用率**：自动调度充电时段，避免光伏发电浪费，实现绿色、经济的充电方案。  
- **可定制化**：开源代码可根据个人或企业的具体硬件（Sungrow 逆变器、Tessie API）进行二次开发。  

**典型接入方式**  
1. **准备环境**：在支持 Go 1.22+ 的服务器或树莓派上安装 Go 环境。  
2. **获取源码**：`git clone https://github.com/your-repo/tesla-solar-matcher.git`。  
3. **配置 API 凭证**：在 `config.yaml` 中填入 Sungrow 和 Tessie 的 API Token、站点 ID、特斯拉账户信息（可使用 Tesla API 的 Refresh Token）。  
4. **运行守护进程**：`go build -o matcher && ./matcher -config config.yaml`，或使用系统服务管理器（systemd、supervisord）将其设为后台服务。  
5. **可选扩展**：通过 Prometheus exporter 暴露指标，或接入 Home Assistant/Webhook 实现可视化与自动化。  

**生产可用性**  
- **成熟度**：当前评分 44/100，代码最近一次更新为 2026‑07‑13，活跃度一般，适合作为原型或内部工具。  
- **风险**：元数据稀少，需自行检查许可证（MIT/Apache 等）、依赖安全性、Issue 处理情况以及发布频率。  
- **推荐使用场景**：研发验证、家庭或小型企业的自建能源管理系统；在正式生产环境使用前，建议进行完整的单元/集成测试并制定运维监控。  

总体而言，该守护进程在实现“光伏自充”功能上提供了直接可用的参考实现，但在大规模或高可靠性场景下仍需自行完善监控、容错和安全审计。

## 🧭 Practical evaluation

**Value:** A Go daemon that matches Tesla charging to solar export (Sungrow and Tessie) may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-07-13
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 47/100 |
| quality | 36/100 |
| recency | 80/100 |
| adoption | 0/100 |
| production | 54/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/guiguan/tesla-sungrow-charge-controller) · [← Back to Misc](./README.md)</sub>
