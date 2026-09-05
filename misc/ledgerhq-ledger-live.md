# LedgerHQ/ledger-live

[![Stars](https://img.shields.io/github/stars/LedgerHQ/ledger-live?style=flat-square&color=yellow)](https://github.com/LedgerHQ/ledger-live/stargazers) [![Forks](https://img.shields.io/github/forks/LedgerHQ/ledger-live?style=flat-square&color=blue)](https://github.com/LedgerHQ/ledger-live/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Mono-repository for packages related to Ledger Live and its JavaScript ecosystem.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 587 |
| 🍴 **Forks** | 466 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ledger-live`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
LedgerHQ/ledger‑live is the mono‑repo that houses all JavaScript packages powering Ledger Live, the desktop and mobile wallet for Ledger hardware devices. With 587 ⭐ and 466 🍴, it offers a TypeScript‑first SDK for interacting with Ledger devices, managing accounts, and handling transactions across multiple blockchains.

**Value**  
The project gives developers a single source of truth for Ledger‑specific APIs, UI components, and utilities, enabling rapid prototyping of hardware‑wallet‑enabled applications without building low‑level communication layers from scratch. Its TypeScript typings and well‑documented README make integration straightforward for teams already using JavaScript/Node.js.

**Practical adoption path**  

1. **Explore the README & examples** – clone the repo, run the `examples` folder, and verify that the device‑communication flow matches your use case (e.g., signing Ethereum or Bitcoin transactions).  
2. **Select needed packages** – the mono‑repo is split into publishable packages (e.g., `@ledgerhq/hw-transport-node-hid`, `@ledgerhq/live-common`). Add them via `npm install` or `yarn add`.  
3. **Run the test suite** – execute `yarn test` to confirm that your environment (OS, Node version, HID libraries) works with the latest code.  
4. **Create a thin wrapper** – encapsulate the Ledger calls in your service layer, handling device detection, user prompts, and error mapping.  
5. **Security review** – audit the transport layer and any third‑party dependencies, then lock versions with a lockfile or a package manager like `pnpm` to prevent accidental upgrades.

**Production readiness**  
The repository is actively maintained (last commit 2026‑05‑13) and written in TypeScript, which aids reliability. Its medium readiness rating means it is suitable for internal tools, prototypes, or customer‑facing features after a brief due‑diligence step: verify the license (Apache‑2.0), run a security scan (e.g., Snyk), and confirm that the core maintainers are responsive. With those checks in place, Ledger Live’s JavaScript ecosystem can be safely promoted to production environments.

### Русский

LedgerLive — это монорепозиторий от LedgerHQ, содержащий набор TypeScript‑пакетов для экосистемы Ledger Live (интеграция с аппаратными кошельками, UI‑компоненты, API‑обёртки). Он подходит для быстрого прототипирования или внутренних сервисов, где требуется взаимодействие с Ledger‑устройствами, однако перед выводом в продакшн рекомендуется проверить актуальность зависимостей, лицензионные условия и безопасность кода. Текущий уровень готовности — средний: проект активно поддерживается (587 ★, 466 forks, обновления 2026‑05‑13), но интеграционные сигналы ограничены, поэтому требуется ручная оценка перед масштабным внедрением.

### 中文

**项目简介**  
LedgerHQ/ledger-live 是一个 mono‑repository，聚合了 Ledger Live 桌面/移动客户端以及其整个 JavaScript 生态（包括 SDK、UI 组件、后台服务等）的所有源码和工具。项目采用 TypeScript 编写，活跃度高（截至 2026‑05‑13 最近一次提交），在 GitHub 上拥有 587 ★、466 Fork。

**价值**  
- **统一代码库**：所有与 Ledger 设备交互的前端、后端以及工具链都在同一个仓库中，便于统一管理、版本同步和跨包协作。  
- **完整生态**：提供了 Ledger Live UI、钱包管理、加密签名、硬件通信等完整功能，开发者可以直接复用或定制，而无需从零实现硬件交互层。  
- **社区与维护**：拥有较大的社区关注度和活跃的贡献者，适合作为内部原型或产品原始代码的参考。

**典型接入方式**  
1. **直接引用子包**：在项目的 `package.json` 中通过 npm/yarn 安装 `@ledgerhq/live-common`、`@ledgerhq/hw-transport-node-hid` 等子包，按需引入对应的 API。  
   ```bash
   yarn add @ledgerhq/live-common @ledgerhq/hw-transport-node-hid
   ```
2. **使用 SDK 示例**：仓库提供了完整的示例代码（`apps/ledger-live-desktop`、`apps/ledger-live-mobile`），可以克隆后直接运行或改写为自己的业务流程。  
3. **自定义插件**：如果需要在现有 Ledger Live 基础上扩展功能（如新增币种、定制 UI），可以在 `packages/` 目录下创建新包，复用内部的工具函数和 UI 组件。

**生产可用性**  
- **成熟度**：项目已在 Ledger 官方产品中长期使用，代码质量和安全审计相对成熟。  
- **适用场景**：适合内部工具、原型验证以及面向企业客户的硬件钱包集成；在对安全合规要求极高的对外产品中使用前，需要完成以下检查：  
  1. **许可证审查**：确认 MIT/Apache 等开源许可证符合公司政策。  
  2. **安全审计**：审查 `@ledgerhq/hw-transport-*` 系列的依赖是否存在已知 CVE。  
  3. **依赖管理**：锁定依赖版本，定期跟进上游更新，避免因破坏性改动导致业务中断。  
- **总体评估**：在完成上述检查后，可视为 **中等成熟度**（Medium）并投入生产使用；若对可靠性有极致要求，建议在内部环境中进行完整的集成测试后再上线。

## 🧭 Practical evaluation

**Value:** LedgerHQ/ledger-live may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 587 GitHub stars
- 466 forks
- updated 2026-05-13
- primary language: TypeScript
- 1 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 67/100 |
| stars | 59/100 |
| topics | 13/100 |
| outlook | 63/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 61/100 |
| production | 66/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/LedgerHQ/ledger-live) · [← Back to Misc](./README.md)</sub>
