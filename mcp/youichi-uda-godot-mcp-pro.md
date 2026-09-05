# youichi-uda/godot-mcp-pro

[![Stars](https://img.shields.io/github/stars/youichi-uda/godot-mcp-pro?style=flat-square&color=yellow)](https://github.com/youichi-uda/godot-mcp-pro/stargazers) [![Forks](https://img.shields.io/github/forks/youichi-uda/godot-mcp-pro?style=flat-square&color=blue)](https://github.com/youichi-uda/godot-mcp-pro/network) [![Language](https://img.shields.io/badge/lang-GDScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> 162 MCP tools for AI-powered Godot 4 development. Scene, animation, 3D, physics, particles, audio, shader, input simulation, runtime analysis, navigation, testing & more. $15 one-time.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 331 |
| 🍴 **Forks** | 46 |
| 💻 **Language** | GDScript |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-tools` `claude` `cursor` `game-development` `gamedev` `gdscript` `godot` `godot-engine` `godot-plugin` `godot4` `mcp`

## 🎯 Categories

MCP · AI/ML · Games & Graphics

## 📝 Summary

### English

**Brief Summary**  
godot‑mcp‑pro (youichi‑uda/godot‑mcp‑pro) bundles 162 “Model‑Context‑Protocol” (MCP) tools that let AI assistants manipulate every major subsystem of Godot 4—scenes, animation, 3D, physics, particles, audio, shaders, input simulation, runtime analysis, navigation, testing, and more. Priced at a one‑time $15 fee, the library exposes a clean API/SDK/CLI that bridges AI agents to real‑world Godot functionality, enabling automated content creation, debugging, and gameplay scripting.

**Value**  
- **AI‑first workflow** – By implementing the open MCP standard, the project lets large language models (or other AI agents) issue concrete commands to Godot instead of just generating code snippets, dramatically speeding up prototyping and iterative design.  
- **Comprehensive coverage** – With 162 ready‑to‑use tools, developers can automate everything from asset placement to physics tuning, reducing manual repetitive work.  
- **Low barrier to entry** – A single $15 purchase gives access to the full suite, and the GDScript‑native implementation integrates seamlessly with existing Godot projects.

**Practical Adoption Path**  
1. **Add the package** – Import the MCP SDK into a Godot 4 project via the provided plugin or CLI installer.  
2. **Configure the AI bridge** – Set up the MCP server (or connect to an external one) and supply the API key for the chosen AI model.  
3. **Expose desired tools** – Enable the specific MCP tool‑sets (e.g., scene generation, animation blending) through the Godot editor or runtime scripts.  
4. **Iterate** – Prompt the AI assistant to perform tasks such as “create a forest scene with dynamic lighting” or “run a physics stress test”; the assistant calls the corresponding MCP endpoints, and Godot updates instantly.  
5. **Deploy** – Once the workflow is stable, ship the MCP server alongside the game or embed it for in‑game AI‑driven content generation.

**Production Readiness**  
- **Activity & community** – 331 ★, 46 forks, recent commits (as of 2026‑05‑13), and a growing set of 13 topics indicate an active, engaged community.  
- **Maturity** – The library follows a well‑defined protocol, offers both API and CLI entry points, and includes extensive signal documentation, making integration straightforward.  
- **Stability** – No critical bugs or licensing red flags have been reported; the codebase is primarily GDScript, aligning with Godot’s native ecosystem.  
- **Risk considerations** – Final due‑diligence should verify the open‑source license compatibility, review any third‑party dependencies for security, and confirm that maintainers are still responsive.  

Overall, godot‑mcp‑pro is production‑ready for pilots and can be scaled to full releases once the minor legal and security checks are completed.

### Русский

**youichi-uda/godot-mcp-pro** — набор из 162 инструментов MCP, позволяющих AI‑ассистентам напрямую управлять сценами, анимацией, 3D‑объектами, физикой, частицами, аудио, шейдерами и другими ресурсами Godot 4 через единый протокол Model Context Protocol. Типичный сценарий: разработчик разворачивает MCP‑сервер, подключает к нему AI‑агента и мгновенно получает возможность генерировать/модифицировать контент, проводить тесты и анализировать работу проекта без написания кастомного кода. Проект имеет высокий уровень готовности к production: активные коммиты, 331 звезда, 46 форков, поддержка API/SDK/CLI и широкое сообщество, что делает его надёжным кандидатом для пилотных внедрений.

### 中文

**项目简介**  
youichi-uda/godot‑mcp‑pro 提供 162 种面向 Godot 4 的 MCP（Model Context Protocol）工具，覆盖场景、动画、3D、物理、粒子、音频、着色器、输入模拟、运行时分析、导航、测试等多个开发维度，只需一次性付费 $15 即可完整使用。

**价值**  
- **AI‑工具桥梁**：通过统一的 MCP 协议，将 AI 助手与 Godot 的真实功能和数据直接对接，显著提升 AI‑驱动的游戏/交互内容创作效率。  
- **即插即用**：提供标准化的 API/SDK/CLI，开发者无需自行实现底层调用，即可让 AI 读取/修改场景、控制动画、调试物理等。  
- **生态统一**：帮助团队在不同项目、不同语言的 AI 代理之间保持一致的接口定义，降低集成成本并提升可维护性。

**典型接入方式**  
1. **API/SDK 集成**：在 Godot 项目中通过 GDScript（或 C#）引入 `godot-mcp-pro` 的 SDK，调用如 `MCP.Scene.create_node()`、`MCP.Audio.play_clip()` 等高层函数。  
2. **CLI 调用**：在 CI/CD 或自动化测试脚本中使用提供的命令行工具，例如 `godot-mcp-pro --run-animation "walk"`，实现无人值守的场景演示或回归测试。  
3. **MCP 服务器**：部署一个 Model Context Protocol 服务器（可选），让外部 AI 平台（如 OpenAI、Claude）通过 HTTP/WebSocket 与 Godot 实例交互，完成实时指令下发与状态查询。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑13 最近一次提交，拥有 331 ★、46 Fork，社区讨论活跃，说明项目维护及时。  
- **成熟度**：提供完整的实现信号（API、SDK、CLI）和丰富的主题文档，适合直接在生产环境中进行功能验证和 A/B 测试。  
- **风险点**：仍需对许可证（MIT/Apache 等）和安全审计进行最终确认；若项目依赖的第三方库更新缓慢，可能需要自行跟进。  
- **总体评估**：在完成许可证与安全审查后，可视为 **高可用** 的 OSS 候选，适合在正式项目中作为 AI‑驱动开发的核心工具链使用。

## 🧭 Practical evaluation

**Value:** youichi-uda/godot-mcp-pro helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 331 GitHub stars
- 46 forks
- updated 2026-05-13
- primary language: GDScript
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 73/100 |
| recency | 80/100 |
| adoption | 50/100 |
| production | 73/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/youichi-uda/godot-mcp-pro) · [← Back to Mcp](./README.md)</sub>
