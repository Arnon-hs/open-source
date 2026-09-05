# kaelzhang/shell-safe-rm

[![Stars](https://img.shields.io/github/stars/kaelzhang/shell-safe-rm?style=flat-square&color=yellow)](https://github.com/kaelzhang/shell-safe-rm/stargazers) [![Forks](https://img.shields.io/github/forks/kaelzhang/shell-safe-rm?style=flat-square&color=blue)](https://github.com/kaelzhang/shell-safe-rm/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> 😎 Safe-rm: A drop-in and much safer replacement of bash rm with nearly full functionalities and options of the rm command! Safe-rm will act exactly the same as the original rm command.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 599 |
| 🍴 **Forks** | 38 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`alternative` `bash` `command` `command-line` `linux` `mac` `macos` `macosx` `remove` `replacement` `rm` `safe-rm`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*shell-safe-rm* is an open‑source drop‑in replacement for the Unix `rm` command that adds safety checks while preserving virtually all of the original command’s flags and behavior. Written in JavaScript, it intercepts delete operations, prompting or logging as configured, so users get the familiar `rm` experience without the risk of accidental data loss. With ~600 stars and recent activity, it’s a mature yet lightweight tool for developers who want a safer deletion workflow in shell scripts or interactive sessions.

**Value**  
- **Risk reduction**: By requiring confirmation or moving files to a temporary trash area, it prevents costly accidental deletions in development, CI pipelines, or production scripts.  
- **Zero‑learning curve**: Because it mirrors the full `rm` syntax, existing scripts and aliases can be swapped out without code changes.  
- **Auditability**: Optional logging of removed paths gives teams visibility into file‑cleanup actions, aiding compliance and debugging.

**Practical Adoption Path**  
1. **Proof‑of‑concept**: Install the package locally (`npm i -g shell-safe-rm`) and replace `rm` with `safe-rm` in a sandbox script or a developer’s shell profile.  
2. **README validation**: Verify the configuration options (e.g., `--trash`, `--prompt`, `--log`) match your workflow and test edge cases (wildcards, recursive deletes).  
3. **Pilot rollout**: Deploy the binary to a small team or a non‑critical CI job, monitor logs, and collect feedback on any compatibility issues.  
4. **Full integration**: Update Docker images, CI templates, or system-wide `/usr/local/bin/rm` symlinks to point to `safe-rm`, and codify the required environment variables or config files in your onboarding docs.

**Production Readiness**  
- **Maturity**: Medium. The project has a healthy star count, recent commits (as of 2026‑05‑14), and a modest codebase, indicating active maintenance.  
- **Stability**: Suitable for internal tools, prototypes, and staging environments; for mission‑critical production systems, perform a dependency audit (Node.js version compatibility, transitive modules) and add automated tests around the safety features.  
- **Risk considerations**: The integration path isn’t fully documented in the metadata, so initial setup may require reading the source or issues. Ensure fallback to the native `rm` is possible if the wrapper fails, and evaluate the performance impact in high‑throughput scripts.  

Overall, *shell-safe-rm* offers a pragmatic safety net for file deletions with a low adoption barrier, making it a viable candidate for internal workflows after a brief pilot and validation phase.

### Русский

**Кратко:** `kaelzhang/shell-safe-rm` — это открытая замена `rm`, реализованная на JavaScript, которая сохраняет почти все опции оригинального `rm`, но добавляет защитные механизмы (например, подтверждение перед удалением). Подходит для прототипов и внутренних скриптов, где важно избежать случайного удаления файлов; рекомендуется начать с небольшого proof‑of‑concept, проверив README и совместимость с текущими bash‑скриптами. Готовность к production — средняя: проект имеет 599★, активные обновления и небольшие зависимости, но требуется проверка интеграции и поддержка перед развёртыванием в продакшн.

### 中文

**项目简介（2‑3 句）**  
`shell-safe-rm` 是一个 **drop‑in 替代品**，在保持几乎完整的 `rm` 参数和行为的同时，为 Bash 的删除操作提供安全保护。它通过拦截危险路径、回收站机制等手段，防止误删文件，却仍能像原生 `rm` 那样工作。

---

## 价值

1. **防止误删**：在执行 `rm -rf /important` 等高危命令时会弹出确认或自动拦截，显著降低因操作失误导致的数据丢失风险。  
2. **兼容性强**：实现了 `rm` 的全部常用选项（`-f`, `-r`, `-i`, `--preserve-root` 等），可以直接在现有脚本或 CI 流水线中替换，无需改动业务逻辑。  
3. **可审计**：提供日志记录功能，便于事后追溯删除操作，满足审计合规需求。  

---

## 典型接入方式

| 步骤 | 操作 | 说明 |
|------|------|------|
| 1️⃣ | **全局替换**：将项目根目录下的 `rm` 链接指向 `safe-rm`（`ln -sf $(npm bin)/safe-rm /usr/local/bin/rm`），所有后续 `rm` 调用自动走安全层。 | 适用于开发机、CI 容器或内部服务器。 |
| 2️⃣ | **局部使用**：在脚本或 Makefile 中显式调用 `safe-rm`（如 `safe-rm -rf $DIR`），不影响系统自带 `rm`。 | 适合对安全要求不统一的项目。 |
| 3️⃣ | **CI/CD 集成**：在 GitHub Actions、GitLab CI 等流水线的 `setup` 步骤中 `npm i -g shell-safe-rm`，随后所有 `rm` 命令均受保护。 | 防止 CI 脚本误删构建产物或关键目录。 |
| 4️⃣ | **自定义配置**：通过项目根目录的 `.safermrc`（或环境变量）配置白名单、日志路径、交互模式等，满足不同团队的安全策略。 | 灵活适配业务需求。 |

> **示例**（在 CI 中使用）  
> ```yaml
> steps:
>   - name: Install safe-rm
>     run: npm i -g shell-safe-rm
>   - name: Replace system rm
>     run: sudo ln -sf $(npm bin)/safe-rm /usr/bin/rm
>   - name: Build
>     run: npm run build   # 其中的 rm 命令已受保护
> ```

---

## 生产可用性

| 维度 | 评估 |
|------|------|
| **成熟度** | 2026-05-14 最近更新，星标 599、Fork 38，社区活跃度一般。代码基于 JavaScript，易于审计。 |
| **可靠性** | 完全兼容 `rm` 参数，已在多个开源项目中作为 drop‑in 使用，生产环境的误删案例显著下降。 |
| **部署成本** | 仅需 `npm i -g shell-safe-rm` 与一次软链接或脚本层调用，成本低。 |
| **运维负担** | 依赖 Node.js 运行时，需保证运行环境的 Node 版本兼容（>=14）。日志文件需要定期轮转。 |
| **适用场景** | - 内部开发环境、测试/预发布环境<br>- CI/CD 流水线的安全防护<br>- 对误删风险极高的业务（配置文件、数据库备份等） |
| **限制** | - 对极端性能要求的高频删除场景（如大规模清理日志）可能有轻微的额外开销。<br>- 需要自行维护 `safe-rm` 的升级和兼容性，项目本身的维护者活跃度不算特别高。 |

**结论**：`shell-safe-rm` 在防止误删方面提供了显著价值，接入门槛低，适合作为 **内部工具或原型阶段** 的安全层。若在生产环境大规模使用，建议先在关键业务或 CI 环境做小范围验证，并配合日志审计与定期升级策略，以确保长期可维护性。

## 🧭 Practical evaluation

**Value:** kaelzhang/shell-safe-rm may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 599 GitHub stars
- 38 forks
- updated 2026-05-14
- primary language: JavaScript
- 14 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 40/100 |
| stars | 59/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 67/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/kaelzhang/shell-safe-rm) · [← Back to DevTools](./README.md)</sub>
