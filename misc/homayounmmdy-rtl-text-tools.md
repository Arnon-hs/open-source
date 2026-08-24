# homayounmmdy/rtl-text-tools

[![Stars](https://img.shields.io/github/stars/homayounmmdy/rtl-text-tools?style=flat-square&color=yellow)](https://github.com/homayounmmdy/rtl-text-tools/stargazers) [![Forks](https://img.shields.io/github/forks/homayounmmdy/rtl-text-tools?style=flat-square&color=blue)](https://github.com/homayounmmdy/rtl-text-tools/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-36%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3 |
| 🍴 **Forks** | 0 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 45/100 |
| 🗓️ **Last push** | 2026-07-02 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Text Processing / Utilities / Localization

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
RTL Text Tools is a zero-dependency TypeScript/JavaScript toolkit for processing right-to-left (RTL) scripts like Arabic, Hebrew, and Persian. It provides utilities for fixing ellipses, converting digits and punctuation, normalizing bidirectional text, and managing DOM/CSS attributes, all compiled to ES5 for maximum legacy browser compatibility (down to IE11). The project is fully tested and MIT-licensed, though its public ecosystem signals remain modest.

**Value**
- **Zero-dependency footprint** keeps bundle size minimal and eliminates transitive-dependency security concerns.
- **Comprehensive RTL fixes** handle nuanced typography issues (brackets, ellipses, bidi markers, locale-specific digits) often missing in general-purpose libraries.
- **Maximum legacy compatibility** (ES5 output, no modern JS features) guarantees it works seamlessly in older environments like IE11.

**Practical Adoption Path**
1. **Install via NPM** – Add the package to your project using `npm install rtl-text-tools`.
2. **Quick Processing** – Use the primary `fixRTL(text, options)` function to automatically normalize mixed strings in your UI or data pipelines.
3. **Component Integration** – Utilize helper functions like `getRTLStyles()` for React inline styles or `setDirAttribute()` for raw DOM manipulation.
4. **Granular Control** – Import individual functions like `moveEllipsis` or `toPersianDigits` if you only need specific transformations.

**Production Readiness**
- **Readiness level:** *Medium* – the project is fully tested, strictly typed, and MIT-licensed, but limited metadata and modest issue activity mean you should perform a short due-diligence cycle.
- **What to verify before production:** Ensure the specific RTL languages you are targeting behave as expected with the default options. Once verified, the toolkit can be safely promoted to internal services or customer-facing web applications.

### Русский

**Краткое описание (2-3 предложения)**
RTL Text Tools — это независимый набор инструментов на TypeScript/JavaScript для обработки текста на языках с письмом справа налево (арабский, иврит, персидский и др.). Он предоставляет функции для исправления многоточий, конвертации цифр и пунктуации, нормализации смешанного текста и работы с DOM/CSS, сохраняя при этом совместимость вплоть до IE11 (компиляция в ES5). Проект полностью покрыт тестами и распространяется под лицензией MIT.

**Ценность**
- **Нулевые зависимости** во время выполнения гарантирует минимальный размер бандла и отсутствие рисков безопасности.
- **Глубокая поддержка RTL** решает специфические типографские проблемы, такие как позиционирование многоточий, исправление скобок и локализация знаков препинания.
- **Совместимость со старыми браузерами** (компиляция в ES5) позволяет использовать библиотеку даже в IE11 без полифилов.

**Путь внедрения**
1. **Установка** – Добавьте пакет через `npm install rtl-text-tools`.
2. **Базовая обработка** – Используйте функцию `fixRTL()` для автоматического форматирования строк в ваших React-компонентах или бэкенд-процессах.
3. **Интеграция** – Применяйте хелперы `getRTLStyles()` или `setDirAttribute()` для корректного отображения интерфейса.
4. **Точечное использование** – Импортируйте отдельные функции (например, `toPersianDigits`), если вам не нужен полный цикл обработки.

**Готовность к продакшену**
- **Уровень готовности:** *Средний* — наличие полных тестов и лицензии MIT делает библиотеку надежной, но ограниченная публичная активность требует краткой проверки.
- **Что проверить:** Убедитесь, что параметры по умолчанию (например, персидские или арабские цифры) соответствуют требованиям вашего проекта. После проверки библиотека отлично подходит для клиентских веб-приложений.

### 中文

**项目简介**  
RTL Text Tools 是一个零运行时依赖的 TypeScript/JavaScript 文本处理工具集，专为从右到左（RTL）语言（如阿拉伯语、希伯来语、波斯语等）设计。它提供了一套全面的 API，用于修复省略号、转换数字和标点符号、规范化双向文本以及处理 DOM/CSS 属性，同时向下兼容至 IE11（编译目标为 ES5）。

**价值**
- **零运行时依赖**：极小的打包体积，无供应链安全风险。
- **深度的 RTL 支持**：不仅限于方向检测，还能处理括号修复、省略号位置调整和特定语言的标点转换等复杂排版问题。
- **极致的旧版兼容性**：编译目标为 ES5，不使用现代 API，确保在 IE11 等老旧浏览器中完美运行。

**典型接入方式**
1. **NPM 安装**：通过 `npm install rtl-text-tools` 引入项目。
2. **核心处理**：在数据流或 UI 渲染前，调用 `fixRTL()` 函数一键修复文本的排版和标点问题。
3. **框架集成**：使用 `getRTLStyles()` 生成 React 行内样式，或使用 `setDirAttribute()` 直接操作 DOM 节点的 `dir` 属性。
4. **按需引入**：若仅需单一功能（如仅转换波斯数字），可直接导入 `toPersianDigits` 等独立函数以减小体积。

**生产可用性**
- **成熟度**：**中等**。项目包含完整的测试覆盖率并采用 MIT 开源协议，但公开的生态信号较少，建议在正式集成前进行快速审查。
- **风险与检查点**：代码已针对浏览器兼容性进行极致优化。在正式上线前，只需根据目标受众确认 `lang` 选项（`'arabic'` 或 `'persian'`）是否符合业务需求即可。

## 🧭 Practical evaluation

**Value:** RTL Text Tools – A zero-dependency TypeScript/JavaScript text processing toolkit for RTL languages with legacy browser support (IE11+).

**Best use cases**

- Frontend web applications requiring RTL text normalization.
- Legacy system modernization where IE11 support is still required.
- React/Vanilla JS components needing dynamic RTL styling and DOM attribute management.

**Integration notes:** Easy to install via npm. Offers both a main `fixRTL` function for quick processing and granular utilities for specific tasks.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-07-02
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 36/100 |
| quality | 26/100 |
| recency | 40/100 |
| adoption | 0/100 |
| production | 38/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/homayounmmdy/rtl-text-tools) · [← Back to Misc](./README.md)</sub>
