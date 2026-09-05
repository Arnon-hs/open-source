# microsoft/roosterjs

[![Stars](https://img.shields.io/github/stars/microsoft/roosterjs?style=flat-square&color=yellow)](https://github.com/microsoft/roosterjs/stargazers) [![Forks](https://img.shields.io/github/forks/microsoft/roosterjs?style=flat-square&color=blue)](https://github.com/microsoft/roosterjs/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> roosterjs is a framework-independent javascript rich text editor.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.3k |
| 🍴 **Forks** | 185 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
RoosterJS is a framework‑agnostic, TypeScript‑based rich‑text editor maintained by Microsoft. With over 1.3 k stars and recent activity (last commit 2026‑06‑26), it offers a modular API for building custom editing experiences without tying you to a specific UI framework.

**Value**  
- **Flexibility** – Because it does not depend on React, Angular, or Vue, you can embed it in virtually any web stack.  
- **Extensibility** – Its plugin architecture lets you add or replace features (e.g., custom formatting, sanitization, or clipboard handling) to match precise business rules.  
- **Microsoft backing** – The project benefits from Microsoft’s engineering standards and documentation, which can reduce the learning curve for teams already familiar with Microsoft tooling.

**Practical Adoption Path**  
1. **Initial Evaluation** – Clone the repo, run the demo, and experiment with the core editor component in a sandbox (e.g., CodeSandbox or a local Node project).  
2. **Feature Mapping** – List the required editing capabilities (tables, mentions, image upload, etc.) and verify they are either built‑in or can be added via plugins.  
3. **Integration Prototype** – Wrap the editor in a thin adapter for your chosen framework (or plain JavaScript) and connect it to your data model, ensuring proper sanitization and event handling.  
4. **Security & License Review** – Confirm the MIT license aligns with your policy and run a dependency scan (e.g., npm audit) to address any known vulnerabilities.  
5. **Testing & CI** – Add unit and integration tests for the editor’s key interactions and include it in your CI pipeline to catch regressions early.

**Production Readiness**  
The project sits at a **medium** readiness level: it is actively maintained and stable enough for prototypes or internal tools, but it lacks extensive enterprise‑grade documentation and large‑scale deployment case studies. Before using RoosterJS in a production environment, perform the following checks:  

- Verify that the maintainer community is responsive (e.g., recent pull‑request merges, issue triage).  
- Assess dependency health and lockfile integrity to avoid supply‑chain risks.  
- Conduct performance benchmarking for your expected content size and concurrency patterns.  
- Implement a fallback or migration plan in case the project’s roadmap changes.

With those safeguards in place, RoosterJS can be a solid foundation for custom rich‑text editing solutions.

### Русский

**Краткое резюме:**  
`microsoft/roosterjs` — это независимый от фреймворков JavaScript‑редактор rich‑text, написанный на TypeScript, имеющий более 1300 звёзд на GitHub и активные обновления (последний — 2026‑06‑26). Он подходит для быстрого прототипирования или внутренних приложений, где требуется встраивание настраиваемого WYSIWYG‑редактора, однако перед выводом в production рекомендуется проверить лицензирование, безопасность и наличие активных мейнтейнеров, а также провести собственную интеграционную проверку. В текущем состоянии готовность к продакшен оценивается как **средняя**: функционально пригоден, но требует дополнительного аудита и контроля зависимостей.

### 中文

**项目简介**  
RoosterJS（`microsoft/roosterjs`）是一个 **框架无关** 的 JavaScript 富文本编辑器，使用 TypeScript 编写，提供插件化的编辑功能、内容规范化和自定义渲染能力，适合在各种前端框架（React、Angular、Vue 等）或纯 JS 项目中快速集成。

**价值点**  
1. **框架独立**：不依赖特定 UI 框架，使用者可以自行决定渲染层，实现高度灵活的集成。  
2. **插件化设计**：核心编辑功能与插件分离，支持自定义键盘快捷键、粘贴过滤、内容清理、HTML 转 Markdown 等常见需求，降低二次开发成本。  
3. **微软内部成熟经验**：源自 Microsoft Office Web 组件的编辑实现，代码质量较高，社区已有 1300+ Stars，活跃度仍在维护。

**典型接入方式**  
```bash
# 通过 npm 安装
npm install roosterjs roosterjs-react   # 若使用 React，可额外装配 React 包
```

```tsx
// React 示例
import { Editor, EditorPlugin, createEditor } from 'roosterjs';
import { ToolbarPlugin } from 'roosterjs-plugin-toolbar';

function MyEditor() {
  const editorRef = useRef<Editor>(null);

  useEffect(() => {
    const editor = createEditor(editorRef.current!, {
      plugins: [new ToolbarPlugin()],
    });
    return () => editor.dispose();
  }, []);

  return <div ref={editorRef} style={{ minHeight: 200, border: '1px solid #ccc' }} />;
}
```

- **纯 JS/TS**：直接在页面中引入 `roosterjs` 包，创建 `Editor` 实例并挂载到容器元素。  
- **插件扩展**：通过 `EditorPlugin` 接口实现自定义功能（如自动保存、图片上传、内容审计），然后在 `createEditor` 时注入。  
- **样式**：编辑器本身不提供 UI 样式，需自行引入官方提供的 CSS 或自行实现工具栏、弹窗等 UI。

**生产可用性评估**  

| 维度 | 评估 | 说明 |
|------|------|------|
| **代码成熟度** | ★★★★☆ | TypeScript 编写，单元测试覆盖率尚可，最近更新于 2026‑06‑26，活跃维护。 |
| **社区与生态** | ★★★☆☆ | 1300+ Stars、185 Fork，社区讨论相对有限，插件生态主要由微软内部和少数开源贡献者提供。 |
| **集成成本** | ★★★★☆ | 只需 npm 安装，API 简洁；但缺少官方 UI，需要自行实现工具栏等，适合已有 UI 框架的项目。 |
| **安全与合规** | ★★★★☆ | MIT 许可证，代码审计相对容易；建议在引入前进行依赖漏洞扫描（`npm audit`）。 |
| **生产适配** | ★★★☆☆ | 适用于内部系统、原型或对编辑功能要求不极端的业务；在高并发、复杂文档协同（如实时协作）场景下，需要自行补充冲突解决和性能优化。 |

**结论**  
RoosterJS 具备较好的技术基底和灵活的插件体系，适合作为 **内部工具、企业后台或原型系统** 的富文本编辑器。若项目已经有成熟的 UI 框架并且对编辑功能的自定义需求较高，采用 RoosterJS 可以快速落地；在正式生产环境上线前，建议完成以下检查：

1. **安全审计**：运行 `npm audit` 并修复发现的漏洞。  
2. **性能评估**：在目标文档大小（如 10 KB–1 MB）下进行编辑、粘贴、撤销等操作的基准测试。  
3. **维护计划**：评估团队是否有能力自行维护插件和修复潜在的 bug，或是否可以依赖微软的后续更新。  

总体而言，RoosterJS 在 **原型开发和内部业务系统** 中可直接使用；在面向外部用户的大型生产环境中，需要做好额外的 UI、协同和运维支撑。

## 🧭 Practical evaluation

**Value:** microsoft/roosterjs may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1312 GitHub stars
- 185 forks
- updated 2026-06-26
- primary language: TypeScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 66/100 |
| topics | 0/100 |
| outlook | 66/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 64/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/microsoft/roosterjs) · [← Back to Misc](./README.md)</sub>
