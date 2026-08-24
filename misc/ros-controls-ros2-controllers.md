# ros-controls/ros2_controllers

[![Stars](https://img.shields.io/github/stars/ros-controls/ros2_controllers?style=flat-square&color=yellow)](https://github.com/ros-controls/ros2_controllers/stargazers) [![Forks](https://img.shields.io/github/forks/ros-controls/ros2_controllers?style=flat-square&color=blue)](https://github.com/ros-controls/ros2_controllers/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> Generic robotic controllers to accompany ros2_control

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 752 |
| 🍴 **Forks** | 495 |
| 💻 **Language** | C++ |
| 📈 **Score** | 48/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ros` `ros2` `ros2-control` `ros2-controllers` `ros2-humble` `ros2-jazzy` `ros2-kilted` `ros2-rolling`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
ros‑controls / ros2_controllers provides a collection of generic, reusable robot controllers that plug into the ros2_control framework, eliminating the need to write low‑level control code for each new robot. With over 750 stars, frequent commits, and wide adoption in the ROS 2 ecosystem, it is a mature open‑source component ready for pilot projects.  

**Value** – By offering ready‑made joint, effort, and trajectory controllers, the package removes repetitive manual coding and testing, letting teams focus on higher‑level behavior and integration of their own tools into repeatable automation pipelines.  

**Adoption path** – Start with a small proof‑of‑concept: clone the repo, follow the README to build the example controllers, and connect them to a simulated robot (e.g., Gazebo). Validate the build and runtime dependencies, then incrementally replace custom control loops with the ros2_controllers equivalents in your own robot description.  

**Production readiness** – The project shows strong production signals: recent activity (last update 2026‑05‑12), high star/fork count, C++ implementation, and proven use in multiple ROS 2 deployments. While the integration details are not fully documented, a short pilot to confirm setup costs and compatibility will likely confirm its suitability for a full‑scale rollout.

### Русский

`ros-controls/ros2_controllers` — это набор готовых к использованию контроллеров для `ros2_control`, позволяющих автоматизировать типовые задачи управления роботами (например, позиционное, скоростное и импеданс‑контролирование) без написания собственного кода. Для внедрения обычно стартуют с небольшого proof‑of‑concept: проверяют README, подключают один‑два контроллера к существующей системе ROS 2 и интегрируют их в повторяемый пайплайн. Проект имеет высокий уровень готовности к продакшну — активная поддержка, более 750 звёзд GitHub, частые обновления и широкое принятие в экосистеме ROS 2.

### 中文

**价值**  
`ros-controls/ros2_controllers` 提供了一套通用的机器人控制器库，能够把常见的运动学、PID、轨迹跟踪等功能以插件形式直接挂载到 `ros2_control` 框架上。使用它可以：

1. **消除重复的手工实现**——无需每次都从头编写控制器，只需在配置文件中声明所需的控制器即可。  
2. **实现可复用、可组合的控制流水线**——不同控制器之间可以像 ROS 组件一样自由组合，形成标准化的控制流。  
3. **加速原型到生产的转化**——成熟的社区维护的控制器已经在多个真实项目中验证，降低了自行实现、调试和维护的成本。

**典型接入方式**  

| 步骤 | 说明 |
|------|------|
| 1️⃣ 环境准备 | 在 ROS 2 工作空间中 `vcs import` 或 `git clone` 该仓库，确保已安装 `ros2_control` 及对应的硬件接口驱动。 |
| 2️⃣ 编译 | `colcon build --packages-select ros2_controllers`，生成对应的控制器插件库。 |
| 3️⃣ 配置 | 在机器人的 `controller_manager` 参数文件（YAML）中声明所需的控制器，例如 `joint_state_broadcaster`、`joint_trajectory_controller`，并指定所使用的硬件接口（`hardware_interface`）。 |
| 4️⃣ 启动 | 使用 `ros2 launch ros2_controllers <controller_manager_launch>.py` 启动 `controller_manager`，随后通过 `ros2 control load_controller`、`ros2 control set_state` 等 CLI 或 `ros2_control` API 动态加载/切换控制器。 |
| 5️⃣ 验证 | 通过 `ros2 topic echo /joint_states`、`ros2 action list` 等工具检查控制器运行状态，必要时在 `rqt_controller_manager` 中可视化调参。 |

> **小技巧**：先在仿真（Gazebo/ignition）中跑一个最小的 `joint_state_broadcaster` 示例，确认硬件抽象层工作正常后，再逐步引入更复杂的轨迹控制器，降低首次集成的风险。

**生产可用性**  

- **活跃度**：截至 2026‑05‑12，仓库拥有 752 ⭐、495 🍴，最近一次提交在 2026‑05‑12，表明仍在积极维护。  
- **生态兼容**：已被 ROS 2 官方文档、Nav2、MoveIt2 等核心项目推荐，拥有成熟的 CI/CD 流水线和跨平台（Ubuntu、Debian、macOS）构建。  
- **成熟度**：多数常用控制器（如 `joint_state_broadcaster`、`joint_trajectory_controller`）已在工业机器人、移动平台等真实项目中部署，具备生产级可靠性。  
- **风险**：元数据中未提供“一键式”安装脚本，集成时需要自行搭建 `controller_manager` 与硬件接口的对应关系，建议先在小规模 PoC（例如仅使用仿真硬件）验证配置成本。  

**结论**：`ros-controls/ros2_controllers` 具备高生产就绪度，适合作为机器人项目的控制层基石。通过标准的 `controller_manager` 配置方式即可快速接入，后续可根据业务需求逐步扩展控制器组合，实现从原型到大规模部署的平滑迁移。

## 🧭 Practical evaluation

**Value:** ros-controls/ros2_controllers helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 752 GitHub stars
- 495 forks
- updated 2026-05-12
- primary language: C++
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 67/100 |
| stars | 61/100 |
| topics | 100/100 |
| outlook | 51/100 |
| quality | 63/100 |
| recency | 20/100 |
| adoption | 63/100 |
| production | 49/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/ros-controls/ros2_controllers) · [← Back to Misc](./README.md)</sub>
