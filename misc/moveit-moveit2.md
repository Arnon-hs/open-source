# moveit/moveit2

[![Stars](https://img.shields.io/github/stars/moveit/moveit2?style=flat-square&color=yellow)](https://github.com/moveit/moveit2/stargazers) [![Forks](https://img.shields.io/github/forks/moveit/moveit2?style=flat-square&color=blue)](https://github.com/moveit/moveit2/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> :robot: MoveIt for ROS 2

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.9k |
| 🍴 **Forks** | 761 |
| 💻 **Language** | C++ |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
MoveIt 2 is an open‑source motion‑planning framework for ROS 2 that automates robot trajectory generation, collision checking, and manipulation tasks. It lets developers replace repetitive, hand‑crafted motion scripts with reusable, configurable pipelines, accelerating prototyping and internal tooling. With a strong community (≈1.9 k stars, 761 forks) and active C++ development, it is a mature yet evolving solution for robotics automation.

**Value**  
- **Productivity boost** – By handling path planning, kinematics, and execution, MoveIt 2 removes the need for engineers to write low‑level motion code for every new robot or task.  
- **Repeatable workflows** – Planners, constraints, and controllers can be scripted and version‑controlled, enabling deterministic, repeatable operations across multiple robots or simulation environments.  
- **Extensibility** – The ROS 2 ecosystem provides ready‑made interfaces to perception, control, and simulation, allowing teams to stitch together complex pipelines without reinventing the wheel.

**Practical adoption path**  
1. **Prototype** – Clone the repository, run the provided demos (e.g., `moveit2_tutorials`) on a supported robot or in simulation (Gazebo/ignition).  
2. **Integrate** – Replace existing motion‑script nodes with MoveIt 2 planning pipelines, using ROS 2 parameters and launch files to expose configuration.  
3. **Validate** – Perform manual inspection of the generated trajectories and collision checks; tune planners (OMPL, CHOMP, etc.) to meet accuracy and speed requirements.  
4. **Automate** – Wrap the MoveIt 2 nodes in higher‑level orchestration tools (e.g., ROS 2 Lifecycle, ros2_control) and connect them to CI pipelines for regression testing.

**Production readiness**  
MoveIt 2 sits at a **medium** readiness level: it is stable enough for internal tools and prototypes, but production deployments should include:  
- **Dependency audit** – Verify compatible ROS 2 distribution (e.g., Humble/Humble) and third‑party libraries.  
- **Maintenance plan** – Track upstream releases and security patches; consider pinning versions.  
- **Integration testing** – Because metadata on integration signals is sparse, build end‑to‑end tests to confirm that MoveIt 2 interacts correctly with your robot drivers, perception stacks, and scheduling systems.  

With these checks in place, MoveIt 2 can be safely promoted from prototype to a reliable component of a production robotics workflow.

### Русский

MoveIt 2 ( moveit/moveit2 ) — open‑source библиотека для ROS 2, автоматизирующая повторяющиеся ручные операции в робототехнических приложениях: она позволяет связать инструменты в воспроизводимые потоки и планировать задачи управления движением. Типичный сценарий внедрения — замена ручного программирования траекторий на готовый набор планировщиков и контроллеров, что ускоряет прототипирование и упрощает внутренние рабочие процессы. Готовность к production — средняя: проект стабилен и активно поддерживается (1865 звёзд, 761 форк, обновления в 2026 г.), но интеграция требует предварительной проверки и настройки, так как метаданные интеграционных точек ограничены.

### 中文

**项目简介**  
MoveIt 2（moveit/moveit2）是面向 ROS 2 的机器人运动规划框架，提供碰撞检测、逆向运动学、路径规划等核心能力，帮助开发者把繁琐的手工操作转化为可重复的自动化工作流。  

**价值**  
- **提升效率**：通过统一的规划接口，消除手工调参和脚本编写的重复劳动。  
- **易于组合**：可与感知、控制、仿真等 ROS 2 生态组件无缝拼接，构建端到端的自动化任务流。  
- **加速原型**：丰富的算法实现和示例让研发团队快速验证新方案，缩短产品迭代周期。  

**典型接入方式**  
1. **依赖声明**：在 ROS 2 工作空间的 `package.xml`/`CMakeLists.txt` 中加入 `moveit_ros_planning`、`moveit_ros_move_group` 等组件。  
2. **配置文件**：使用 MoveIt Setup Assistant 生成 `.srdf`、`.yaml` 等配置文件，描述机器人模型、规划组和约束。  
3. **启动节点**：通过 `ros2 launch moveit2 move_group.launch.py` 启动规划服务；随后在自定义节点中调用 `move_group` 接口或 Action Server 实现路径规划、执行等功能。  
4. **集成测试**：在仿真（Gazebo、Ignition）或真实机器人上运行示例场景，验证运动学、碰撞模型和实时性能。  

**生产可用性**  
- **成熟度**：GitHub ★1865，Fork 761，活跃维护（最近更新 2026‑06‑24），代码主要为 C++，社区文档和示例较为完整。  
- **适用场景**：适合内部原型、实验平台或对运动规划要求不极端的生产线；在正式上线前需进行依赖审查、性能基准和安全评估。  
- **风险**：元数据中集成信号稀疏，实际部署时可能需要手动排查兼容性问题（如 ROS 2 发行版、第三方驱动、实时调度等）。建议在预研阶段完成一次完整的端到端验证，再决定是否投入生产环境。

## 🧭 Practical evaluation

**Value:** moveit/moveit2 helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1865 GitHub stars
- 761 forks
- updated 2026-06-24
- primary language: C++

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 70/100 |
| topics | 0/100 |
| outlook | 64/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 70/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/moveit/moveit2) · [← Back to Misc](./README.md)</sub>
