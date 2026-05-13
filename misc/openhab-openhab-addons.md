# openhab/openhab-addons

[![Stars](https://img.shields.io/github/stars/openhab/openhab-addons?style=flat-square&color=yellow)](https://github.com/openhab/openhab-addons/stargazers) [![Forks](https://img.shields.io/github/forks/openhab/openhab-addons?style=flat-square&color=blue)](https://github.com/openhab/openhab-addons/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Add-ons for openHAB

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2k |
| 🍴 **Forks** | 3.7k |
| 💻 **Language** | Java |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`add-ons` `java` `openhab`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **openhab/openhab-addons** repository houses a large collection of Java‑based plug‑ins that extend the openHAB home‑automation platform with support for new devices, protocols, and services. With over 2 000 stars and a healthy fork count, the project is actively maintained (last update 2026‑05‑13) and serves as a go‑to source for developers needing ready‑made bindings or a reference implementation for custom integrations.

**Value**  
- **Broad device coverage** – the add‑ons already implement dozens of popular smart‑home standards (Zigbee, MQTT, KNX, etc.), saving you from writing low‑level drivers.  
- **Reference code** – each add‑on follows openHAB’s modular architecture, providing concrete examples of how to interact with the core runtime, handle configuration, and expose channels.  
- **Community support** – the sizable star/fork base and open issue tracker mean you can often find existing discussions or patches for common problems.

**Practical Adoption Path**  
1. **Assess relevance** – Browse the repository’s `README` and the `bundles` directory to locate add‑ons that match the devices or protocols you need.  
2. **Prototype** – Pull the desired add‑on JARs into a local openHAB instance (or use the official add‑on installer) and verify that the expected Things/Channels appear.  
3. **Inspect code** – If you need custom behavior, clone the repo, study the specific binding’s source, and adapt it; the project’s Maven build makes local modifications straightforward.  
4. **Integrate** – Add the compiled JAR(s) to your production openHAB `addons` folder, update your `services` configuration, and restart the runtime.

**Production Readiness**  
- **Maturity**: Medium. The project is mature enough for prototypes and internal deployments, but the integration path isn’t explicit in the metadata, so a manual review of the binding’s documentation and code is required.  
- **Maintenance**: Active (last commit today) and backed by a large contributor community, yet you should monitor upstream updates for breaking changes, especially when upgrading openHAB core versions.  
- **Risk mitigation**: Perform a small‑scale pilot, lock dependency versions via Maven, and establish a test suite that validates the add‑on’s behavior before promoting to production.

### Русский

Openhab‑addons — это набор Java‑расширений для платформы openHAB, предоставляющий готовые драйверы и интеграции (более 2000 звёзд, 3700 форков). Его обычно подключают в прототипах или внутренних IoT‑проектах, где требуется быстро добавить поддержку новых устройств, а затем, после ручной проверки совместимости и оценки затрат на поддержку, переводят в продакшн. Готовность к production — средняя: проект активно поддерживается, но путь интеграции не очевиден из метаданных, поэтому перед внедрением требуется детальная проверка.

### 中文

**项目简介**  
openhab‑addons 是 openHAB 平台的官方插件仓库，提供数千个设备驱动、协议适配器和功能扩展（如天气、语音、数据库等），帮助用户快速将各种 IoT 设备接入 openHAB。

**价值**  
- **即插即用**：大多数常见硬件（ZigBee、Z-Wave、MQTT、Modbus 等）已有成熟的 Add‑on，省去自行实现协议的工作量。  
- **社区维护**：超过 2 000 颗星和 3 700 次 Fork，活跃的贡献者持续修复 bug、添加新设备，适合作为原型或内部项目的基础设施。  
- **统一管理**：所有插件遵循 openHAB 的模块化规范，统一通过 UI 或配置文件加载，便于后期维护和升级。

**典型接入方式**  
1. **在 openHAB UI 中安装**：打开 *Settings → Add-ons*，搜索所需插件并点击 *Install*。  
2. **通过文件方式**：将对应的 JAR 包下载到 `${OPENHAB_CONF}/addons/` 目录，重启 openHAB 即可加载。  
3. **自动化脚本**：使用 `openhab-cli` 或 REST API（`/rest/addons`）实现批量安装/更新，适合 CI/CD 或大规模部署。

**生产可用性**  
- **成熟度**：插件库已多年迭代，核心协议适配器（Z-Wave、MQTT、KNX 等）在生产环境中得到广泛验证。  
- **风险**：元数据中未提供完整的依赖图，部分插件可能需要额外的库或特定的系统配置；因此在正式上线前建议在测试环境完成一次完整的功能验证。  
- **维护成本**：定期关注仓库的 Release Notes 与安全公告，确保及时升级依赖的 Java 版本和第三方库。  

综上，openhab‑addons 适合作为原型验证或内部 IoT 平台的快速集成层，经过充分的测试与依赖审查后，也可以安全地用于生产环境。

## 🧭 Practical evaluation

**Value:** openhab/openhab-addons may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2050 GitHub stars
- 3722 forks
- updated 2026-05-13
- primary language: Java
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 89/100 |
| stars | 70/100 |
| topics | 38/100 |
| outlook | 76/100 |
| quality | 80/100 |
| recency | 100/100 |
| adoption | 76/100 |
| production | 74/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/openhab/openhab-addons) · [← Back to Misc](./README.md)</sub>
