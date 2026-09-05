# lesspass/lesspass

[![Stars](https://img.shields.io/github/stars/lesspass/lesspass?style=flat-square&color=yellow)](https://github.com/lesspass/lesspass/stargazers) [![Forks](https://img.shields.io/github/forks/lesspass/lesspass?style=flat-square&color=blue)](https://github.com/lesspass/lesspass/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> :key: stateless open source password manager

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6k |
| 🍴 **Forks** | 356 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anonymous` `lesspass` `password` `password-manager` `passwords` `privacy` `self-hosted`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
LessPass is a stateless, open‑source password manager written in TypeScript that generates site‑specific passwords on‑the‑fly from a master secret, eliminating the need to store any credentials. With over 6 000 GitHub stars, frequent recent commits, and an active community, it offers a lightweight alternative to traditional vault‑based solutions for users who prefer deterministic password generation.

**Value**  
- **Stateless design**: No database or sync layer is required; passwords are derived each time, reducing attack surface and simplifying backup and recovery.  
- **Cross‑platform**: Available as a web app, CLI, browser extensions, and mobile builds, making it easy to integrate into existing workflows.  
- **Open‑source transparency**: The codebase is publicly auditable, fostering trust and allowing custom extensions or security hardening.

**Practical Adoption Path**  
1. **Proof‑of‑concept**: Clone the repo, run the CLI or web demo, and verify that the generated passwords match your existing policy (length, character set, etc.).  
2. **Pilot integration**: Replace a small set of low‑risk service passwords with LessPass‑derived values, documenting the master secret handling process.  
3. **Team rollout**: Publish internal documentation, add the browser extension to team machines, and optionally wrap the CLI in a CI/CD step for automated secret generation in scripts.  
4. **Full migration**: Gradually decommission stored passwords in vaults once confidence is built, leveraging the deterministic nature of LessPass for seamless regeneration.

**Production Readiness**  
- **Activity & adoption**: Recent commits (as of 2026‑05‑11), a large star count, and many forks indicate a healthy, maintained project.  
- **Ecosystem fit**: TypeScript core makes it easy to embed in modern web stacks; existing extensions cover most major browsers and mobile platforms.  
- **Risk considerations**: No immediate licensing or major security flags, but a final review of the MIT license compliance, dependency audit, and maintainer responsiveness is advisable before a large‑scale rollout.  

Overall, LessPass is production‑ready for pilots and can be scaled to enterprise use after a small, controlled proof‑of‑concept phase.

### Русский

**lesspass/lesspass** — это статeless‑менеджер паролей с открытым кодом, генерирующий уникальные пароли на основе мастер‑фразы и названия сервиса, без хранения секретов. Он легко интегрируется в существующие пайплайны: достаточно добавить небольшую библиотеку (TypeScript) в приложение или скрипт, настроить генерацию паролей и использовать их в автоматизированных процессах (CI/CD, DevOps, пользовательские утилиты). По оценке готовности проект находится на высоком уровне — активные коммиты, более 6000 звёзд, широкий набор форков и хороший экосистемный отклик, что делает его подходящим для пилотного внедрения в production после быстрой проверки README и лицензии.

### 中文

**项目简介**  
LessPass（lesspass/lesspass）是一款 stateless （无状态）且开源的密码管理器，核心实现使用 TypeScript。它通过对“站点名 + 用户名 + 主密码 + 可选参数”的组合进行可重复的哈希运算，实时生成强密码，而无需在本地或云端保存任何密码数据。

**价值**  
- **零存储风险**：所有密码均在本地即时生成，既不写入磁盘也不上传服务器，天然防止泄漏。  
- **跨平台一致性**：同一套输入在任何设备、任何浏览器或 CLI 中都会得到完全相同的密码，便于多设备协作。  
- **开源透明**：代码公开、社区活跃（6000+ Stars、350+ Fork），可自行审计或二次定制。

**典型接入方式**  
1. **浏览器插件/Web UI**：直接在浏览器中打开 LessPass 官方页面或安装其 Chrome/Firefox 扩展，填写站点信息即可生成密码。  
2. **命令行工具**：通过 `npm i -g lesspass-cli` 安装后，在 CI/CD、脚本或本地终端中使用 `lesspass generate …` 进行自动化密码生成。  
3. **API/库集成**：在自有前端或后端项目中 `npm install lesspass`，调用 `lesspass.generate(options)`，将生成逻辑嵌入内部系统（如内部 SSO、密码轮转脚本等）。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑11，项目仍在维护；Issues 与 PR 反馈速度快。  
- **社区与生态**：6000+ Stars、350+ Fork，已有多语言实现（Python、Go、Rust），说明生态成熟。  
- **安全与合规**：无后端存储，降低数据泄露风险；仍需自行审计依赖库的许可证与安全公告。  
- **建议**：先在测试环境进行一次 “生成‑校验‑回滚” 的 PoC，确认哈希参数、字符集符合公司密码策略后，再推广至生产环境。整体来看，LessPass 已具备在内部或面向用户的密码生成场景中直接投入使用的条件。

## 🧭 Practical evaluation

**Value:** lesspass/lesspass may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 6015 GitHub stars
- 356 forks
- updated 2026-05-11
- primary language: TypeScript
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 80/100 |
| topics | 88/100 |
| outlook | 77/100 |
| quality | 82/100 |
| recency | 80/100 |
| adoption | 76/100 |
| production | 72/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/lesspass/lesspass) · [← Back to Misc](./README.md)</sub>
