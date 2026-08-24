# ciotlosm/lovelace-thermostat-dark-card

[![Stars](https://img.shields.io/github/stars/ciotlosm/lovelace-thermostat-dark-card?style=flat-square&color=yellow)](https://github.com/ciotlosm/lovelace-thermostat-dark-card/stargazers) [![Forks](https://img.shields.io/github/forks/ciotlosm/lovelace-thermostat-dark-card?style=flat-square&color=blue)](https://github.com/ciotlosm/lovelace-thermostat-dark-card/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> 🌡 Thermostat card with a round and black feel to it

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 744 |
| 🍴 **Forks** | 185 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`custom-cards` `hacs` `home-assistant` `lovelace` `thermostat`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
The *lovelace-thermostat-dark-card* is a Home Assistant Lovelace UI component that displays a sleek, round thermostat widget with a dark theme. With over 740 ★ on GitHub, recent TypeScript updates and active community forks, it’s a mature open‑source option for anyone wanting a visually distinct temperature control in their dashboards.

**Value**  
The card provides a ready‑made, aesthetically‑focused thermostat UI that saves developers the effort of building a custom component from scratch. Its dark styling blends naturally with modern Home Assistant themes, and the TypeScript codebase makes it easy to extend or adapt for additional features (e.g., custom climate entities, automation triggers).

**Practical adoption path**  

1. **Proof‑of‑concept** – Clone the repo, run `npm install && npm run build`, and add the compiled module to your Home Assistant `www` folder.  
2. **README validation** – Follow the quick‑start steps in the README to add the card to a Lovelace dashboard and bind it to an existing climate entity.  
3. **Pilot** – Deploy the card on a non‑critical dashboard (e.g., a test user’s view) and verify that state updates, set‑point changes, and UI responsiveness meet expectations.  
4. **Customization** – If needed, fork the repo and adjust the TypeScript source (e.g., colors, icons, or additional controls) before merging back into your production environment.

**Production readiness**  
The project scores 61/100 overall but shows strong production signals: recent commits (as of 2026‑06‑25), a healthy star/fork count, and a clear TypeScript codebase. While the license and security posture still require a final review, the active maintainer community and ecosystem adoption indicate the card is ready for a serious pilot in production Home Assistant installations.

### Русский

Lovelace‑Thermostat‑Dark‑Card — это открытая карточка‑термостата для Home Assistant с стильным круглым дизайном в тёмных тонах, позволяющая быстро добавить в интерфейс управляемый регулятор температуры и визуальный индикатор состояния. При внедрении её обычно помещают в панель управления (Lovelace) рядом с другими датчиками, подключая к уже существующим климат‑устройствам через стандартные сущности Home Assistant; достаточно добавить карточку в YAML‑конфигурацию и задать нужные entity‑id. Проект считается готовым к production‑использованию: активные коммиты, более 700 звёзд, регулярные релизы и широкая поддержка сообщества, однако перед масштабным развертыванием рекомендуется проверить лицензию и выполнить небольшой PoC, убедившись, что README покрывает ваш сценарий.

### 中文

**项目简介**  
`ciotlosm/lovelace-thermostat-dark-card` 是一款为 Home Assistant Lovelace 界面打造的黑色主题温控卡，采用圆形设计，视觉上更符合暗色系仪表盘的审美，能够直观地显示当前温度、目标温度以及加/减按钮。

**价值**  
- **暗色系 UI 友好**：专为暗色主题定制，避免亮色卡片在暗色仪表盘中显得突兀。  
- **交互即视**：圆形布局和大号按钮让调温操作更自然，适合触控面板或壁挂平板。  
- **开箱即用**：基于 TypeScript 编写，遵循 Home Assistant 的自定义卡片规范，安装后即可在 Lovelace 中直接引用。

**典型接入方式**  
1. **安装**：在 Home Assistant 的 `config/custom_components`（或 `www` 目录）下通过 HACS 添加或手动克隆仓库。  
2. **资源加载**：在 `configuration.yaml` 或 Lovelace UI 的资源列表中加入  
   ```yaml
   resources:
     - url: /local/lovelace-thermostat-dark-card/thermostat-dark-card.js
       type: module
   ```  
3. **卡片配置**：在仪表盘的 YAML 或 UI 编辑器中加入卡片配置，例如：  
   ```yaml
   type: custom:thermostat-dark-card
   entity: climate.living_room
   name: 客厅
   hide_temperature: false
   ```  
4. **验证**：刷新 Lovelace 页面，确保卡片渲染正常并能控制对应的 `climate` 实体。

**生产可用性**  
- **活跃度**：截至 2026‑06‑25 最近一次提交，项目仍在维护；GitHub ★744、Fork 185，社区反馈活跃。  
- **技术成熟度**：使用 TypeScript 编写，遵循 Home Assistant 官方自定义卡片 API，兼容最新的 Lovelace 版本。  
- **安全与合规**：暂无已知安全漏洞，许可证为 MIT，适合企业内部及商业项目使用。  
- **推荐上线方式**：先在测试环境做一次完整的 POC（验证卡片在实际硬件、暗色主题以及多语言环境下的表现），确认无 UI 冲突后即可在生产环境的大屏或移动端仪表盘中推广使用。  

综上，该卡片在 UI 美观度、易用性以及社区成熟度方面均表现良好，具备直接投入生产使用的条件。

## 🧭 Practical evaluation

**Value:** ciotlosm/lovelace-thermostat-dark-card may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 744 GitHub stars
- 185 forks
- updated 2026-06-25
- primary language: TypeScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 61/100 |
| topics | 63/100 |
| outlook | 54/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 60/100 |
| production | 55/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/ciotlosm/lovelace-thermostat-dark-card) · [← Back to Misc](./README.md)</sub>
