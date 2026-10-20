<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/header-dark.svg">
    <img src="assets/header-light.svg" alt="NingHong — Unreal Engine / C++ · Harness" width="640">
  </picture>
</p>

<p align="center">
  我是宁鸿（Zining Zhao）。<br>
  主线是 Unreal Engine / C++；近来也把 DeepSeek Harness 收成可以装到别的机器上的插件。<br>
  <sub>把功能做出来，也把它背后的运行机制弄明白。</sub>
</p>

<p align="center">
  <a href="https://github.com/Aceared0829?tab=repositories">全部仓库</a>
  &nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="#engineering-notes">实现与验证</a>
  &nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="#关注与交流">关注与交流</a>
</p>

## 关于我

主要和 Unreal Engine / C++ 打交道，做的是玩法、引擎生命周期与角色动画之间需要互相咬合的那一层：GAS 的战斗结构、Actor / Component 的生成与回收、动画数据的导出与推理接入，以及为这些流程配的编辑器工具。

- **方向** — Gameplay、Engine、Animation、Tools & Language 四条互相咬合。
- **在做** — Unreal 侧的 ZeroG、UnrealAgent 与 AIAnimationSystem；以及把这台机器上的 Harness 用法收成别人也能装的插件套件。
- **原则** — 功能做出来之后继续追它为什么能跑；实现与验证分开写，上游来源与自己的增量分开写。
- **交流** — [在本仓库提 Issue](https://github.com/Aceared0829/Aceared0829/issues)，或到各项目仓库的 Discussion 里说。

## Selected work

点项目名进入仓库。长说明在下方，默认收起。

| 方向 | 项目 | 一句话 |
|---|---|---|
| 工具 | [**dsh-kit**](https://github.com/Aceared0829/dsh-kit) | 插件源码、版本清单和一键安装。不含账号和本机路径。 |
| 工具 | [**deepseek-harness**](https://github.com/Aceared0829/deepseek-harness) | 官方 Harness 的个人 fork。引擎在这里，插件不在这里。 |
| 论文 | [**Zing-0.5**](https://arxiv.org/abs/2609.17909) | 署名作者；个人部分是游戏数据采集工程。[仓库](https://github.com/seedleap/zing-world-model) |
| 编辑器 | [**UnrealAgent**](https://github.com/Aceared0829/UnrealAgent) | 把智能体工作流带进 Unreal Editor。Beta · MIT |
| 原型 | [**ZeroG**](https://github.com/Aceared0829/ZeroG) | 战斗、角色运动与动画协作的 C++ 原型。开发中 |
| 引擎 | [**UE Object Pool**](https://github.com/Aceared0829/UnrealEngine/tree/fix/generic-object-pool-lifecycle) | Actor / Component 生命周期与对象复用。访问需授权 |
| 动画 | [**AIAnimationSystem**](https://github.com/Aceared0829/AIAnimationSystem) | MotionBricks 之上的 UE 动画数据、训练与 GPU 推理。实验阶段 |
| 语言 | [**VerseAngelScript**](https://github.com/Aceared0829/VerseAngelScript) | 从脚本约定到 Rider 开发体验。早期探索 |

阅读储备：[Hybrid-Motion-Imitation](https://github.com/Aceared0829/Hybrid-Motion-Imitation) 目前仅 Fork，尚无个人实现或复现成果。

## Engineering notes

展示具体做了什么，也记录尚未完成的部分。以下保留项目细节、上游来源与验证范围。默认收起。

<details>
<summary><strong>deepseek-harness</strong> — 个人 fork，引擎</summary>

官方仓库的 fork，用来跑我自己构建的 Windows Desktop。不装官方安装包：两边 appId 相同，装官方会覆盖自建包。

插件和本机设置不在这个 fork 里。可以分给别人的部分在 dsh-kit。

[我的 fork](https://github.com/Aceared0829/deepseek-harness) · [上游](https://github.com/deepseek-ai/deepseek-harness)

</details>

<details>
<summary><strong>dsh-kit</strong> — 插件套件与一键安装</summary>

把这台机器上的插件用法整理成别人也能装的库。对方需要已经有 DeepSeek Harness；安装器不负责重做桌面端。

- 自己写的插件放源码：Grok 连接、desktop-extras、桌宠桥接与生命周期。
- 别人发布的插件只记包名和版本，安装时从 npm 装。
- 空的设置层才会写入模板。已有设置不会被覆盖。
- 账号、令牌、本机路径不入库。Grok 要自己登录。桌宠本体在另一个仓库，没填目录不会自启。

[dsh-kit](https://github.com/Aceared0829/dsh-kit)

[![](https://img.shields.io/badge/powered_by-dsh-4D6BFE?style=flat-square&logo=deepseek&logoColor=white)](https://github.com/deepseek-ai/deepseek-harness)

</details>

<details>
<summary><strong>Zing-0.5</strong> — 论文署名与个人工程贡献</summary>

**Zing-0.5 是 Seedleap 团队的世界模型项目。** Zining Zhao 列于论文作者名单；我在职期间参与的是数据采集工程，未参与论文撰写。

- **UE 数据采集中台**：参与开发 Unreal Engine 数据采集中台，经历从 0.1 到 1.0 阶段的建设。
- **第三方游戏采集管线**：开发通过内存注入采集第三方游戏数据的管线。
- **数据贡献**：为项目提供一批采集数据；不公开未披露的数据规模或数据内容。

项目模型、训练方法和论文写作属于团队工作；上述条目仅说明我的个人贡献。

[论文与作者名单](https://arxiv.org/abs/2609.17909) · [项目仓库](https://github.com/seedleap/zing-world-model)

</details>

<details>
<summary><strong>UnrealAgent</strong> — 实现、状态与验证边界</summary>

**将 Codex / Cursor 智能体工作流接入 Unreal Editor 的开源 C++ 插件。** 从采集项目中独立拆出，采用 MIT 许可证，目前为 Beta。

- **编辑器工作流**：Slate 会话面板、ACP 适配、流式反馈，以及通过本机 MCP 调用结构化编辑器工具。
- **工具执行与扩展**：参数校验、风险审批、协作式取消、事务与审计；通过 Provider SDK 注册外部工具。
- **来源与边界**：Agent 推理由外部 Codex / Cursor 完成；Action 契约保留 ue-mcp 的上游兼容基线，不将目录数量等同于全部原创或全场景验证。
- **当前阶段**：Windows / UE 5.8 开发基线；Codex ACP 已更新至 1.11.0，其他系统、引擎版本及完整场景覆盖仍需验证。

[源码与安装说明](https://github.com/Aceared0829/UnrealAgent) · [验证边界](https://github.com/Aceared0829/UnrealAgent/blob/main/Docs/FinalAcceptance.md)

</details>

<details>
<summary><strong>ZeroG</strong> — 实现、状态与验证边界</summary>

<sub>开发中 · GAMEPLAY / GAS / TRAVERSAL</sub>

**基于 UE 5.8 的 C++ 动作游戏技术验证项目。** 围绕战斗、武器、连招和角色运动，实践游戏逻辑、动画与引擎机制之间的协作。

**已有实践**

- **GAS 战斗结构**：由 PlayerState 持有 ASC 与属性集，结合 GameplayAbility、GameplayEffect 和 Gameplay Tags 组织技能与角色状态。
- **武器与连招**：通过组件和动作数据管理武器切换、连招与 Montage；处理武器攻击贡献的重复更新和 Avatar 交接清理。
- **命中检测**：采样当前骨骼姿态的世界空间插槽，结合帧间运动路径补偿，提供 Line、Box、Sphere、Capsule 等检测方式。
- **角色运动与 Traversal**：在 MotionMatchingInCpp 插件中组织运动状态、障碍与边缘检测、Chooser 动作选择、Motion Warping 和 Montage 播放辅助。

**当前阶段**：源码和可编辑工程资源已经公开，但它仍是原型。地图、资产引用、动画表现、多人玩法和完整 Cook / 游戏包启动仍需继续完善或验证。

<details>
<summary><strong>模块关系、回归验证与后续工作</strong></summary>

#### 模块与数据

- ZeroG 游戏模块负责玩家、Boss、GAS 战斗、武器、连招和命中处理。
- MotionMatchingInCpp 插件提供通用角色运动与 Traversal 能力，通过接口与游戏侧协作，不反向依赖 ZeroG 模块。
- 动画蓝图、PoseSearch 数据库、Chooser 表、Montage 与关卡配置仍由工程资源承载；插件名称不代表整个动画图已经由 C++ 实现。

#### 已记录的验证

2026-09-07 / 08 的公开预览版本记录了 UE 5.8.2 下的 Editor / Game 编译，以及四项 UE 回归：

- 命中检测的世界空间采样与帧间路径。
- 武器攻击贡献的幂等更新及清理。
- 武学状态重置的有效与无效 Avatar 路径。
- Chooser 选定动作之后的 Traversal 禁用标签检查。

四项回归均通过，其中两项带警告；资源恢复脚本也有独立的完整性与冲突保护测试。这些是指定版本的验证记录，不等于完整地图、联网或游戏打包已经通过。

#### 后续重点

修正残留资产与默认地图引用，梳理 Blueprint / C++ Traversal 调用路径，补充真实场景、动画效果、多人 PIE 与 Cook 验证。Release 提供可编辑资源，不是玩家双击运行的安装包。

</details>

[源码](https://github.com/Aceared0829/ZeroG) · [架构说明](https://github.com/Aceared0829/ZeroG/blob/codex/open-source/Docs/ARCHITECTURE.md) · [验证记录](https://github.com/Aceared0829/ZeroG/blob/codex/open-source/Docs/VALIDATION.md) · [可编辑工程资源](https://github.com/Aceared0829/ZeroG/releases)

</details>

<details>
<summary><strong>UE Object Pool</strong> — 实现、状态与验证边界</summary>

<sub>开发中 · ENGINE / LIFECYCLE / REUSE</sub>

**Unreal Engine 源码分支中的 GenericObjectPool。** 探索按类型配置、显式启用的 Actor / Component 复用机制，将对象池接入引擎原生创建与回收流程。

**已有实践**

- **按 World 管理**：基于 `UObjectPoolSubsystem` 组织对象池，维护活动实例、休眠实例、容量与配置状态。
- **原生流程接入**：围绕 Actor 生成与销毁、Component 添加与销毁处理池化路径，而不仅是在业务代码外包一层数组缓存。
- **生成与唤醒时序**：处理延迟生成、生成中的容量占位，以及对象完成初始化前不应被重新回收的问题。
- **生命周期与回归**：围绕唤醒 / 休眠、回调重入、配置刷新和池收缩补充处理与测试，关注回调中销毁对象或修改池状态的边界。

**当前阶段**：已有实现和自动化测试，仍在完善适用范围与验证。已提交 [Epic PR #15156](https://github.com/EpicGames/UnrealEngine/pull/15156)，截至本页整理时尚未合入。

<details>
<summary><strong>设计关注点、测试范围与限制</strong></summary>

#### 不只是“把对象藏起来”

Actor / Component 复用需要协调注册状态、所有权、激活状态、生成上下文和回调顺序。延迟生成尚未完成的实例仍属于在途对象，不能直接作为容量回收策略的候选。

配置刷新、唤醒 / 休眠与销毁回调都可能重入对象池；实现需要重新检查对象和池状态，不能假定回调前取得的引用仍然有效。

#### 已有测试关注

预分配的休眠状态、容量与溢出策略、生成上下文、延迟生成占位、回收及获取时的回调安全、配置刷新与池收缩。测试源码是具体行为的入口，不代表已经覆盖任意业务对象或所有网络场景。

#### 仍需谨慎的边界

- 复用保留 UObject 身份，不等于重新构造对象，也不会自动清空任意业务状态。
- 外部引用、委托、资源所有权与对象专有数据，仍需要明确的复用契约。
- 不承诺所有对象都能透明池化，也没有在此宣称未经测量的通用性能提升。

</details>

[引擎分支](https://github.com/Aceared0829/UnrealEngine/tree/fix/generic-object-pool-lifecycle) · [PR 与讨论](https://github.com/EpicGames/UnrealEngine/pull/15156) · [回归测试源码](https://github.com/Aceared0829/UnrealEngine/tree/fix/generic-object-pool-lifecycle/Engine/Source/Runtime/Engine/Private/Tests/GenericObjectPool)

<sub>上述引擎源码与 PR 需要相应的 Epic / GitHub 访问权限；贡献提交不代表官方采纳或背书。</sub>

</details>

<details>
<summary><strong>AIAnimationSystem</strong> — 实现、状态与验证边界</summary>

<sub>实验阶段 · ANIMATION / DATA / TRAINING</sub>

**面向 Unreal Engine 的 AI 角色动画实验。** 基于 NVIDIA GR00T-WholeBodyControl / MotionBricks，探索从游戏动画数据到模型训练，再到角色姿态生成的流程。

**已有实践**

- **UE 动画导出**：实验性 Editor 插件从 AnimSequence 采样并导出骨架、参考姿态和动作数据。
- **数据约束与预处理**：保留原生帧率和逐帧时间，处理坐标、骨架与语义映射；增加名称规则标签、家族划分和仅训练帧统计量。
- **训练工具入口**：增加自定义 UE 骨架的 VQ-VAE、Pose、Root 训练入口，以及检查点保存、续训和指标记录。
- **质量评估与推理导出**：加入真实帧掩码、几何监督和短姿态采样，提供原生时间 HTML 对照、量化旁路诊断及完整/仅解码 FP32 推理包。
- **参考演示适配**：对上游工程做游戏动画方向的裁剪，补充中文交互界面和 Windows 参考演示启动器。

- **GASP 推理实验台**：新增 ONNX 导出、模型契约校验和 AnimGraph 节点，在动画工作线程执行 DirectML GPU 推理；通过固定采样、重叠窗口融合、延迟插值与静止保护改善重建连续性。

**当前阶段**：已完成真实 UE 资产导出、GPU 训练、留出集骨架重建评估，以及 GASP 独立对照场景中的 GPU 推理与 AnimGraph 姿态输出验证。当前模型重建已知源动画；文字生成、玩家意图驱动与正式游戏运行时接入仍待开发和验证。

<details>
<summary><strong>验证基础、运行时设想与上游边界</strong></summary>

#### 已有验证基础

UE 5.8.2 插件实际导出 1,728 段 UEFN Mannequin 动画，保留原生 30/60 FPS。30 FPS 数据划分为 1,355 段训练、189 段验证、178 段测试；两轮 VQ-VAE 均在 RTX 4070 Laptop GPU 上训练 20,000 步，完整网络保持约 2,540 万参数。

同一测试集的平均姿态误差从 7.63 降到 7.37 cm，6 段极短姿态从 17.78 降到 10.87 cm；但 121/178 段误差上升，走跑蹲类有所退步，所以保留上一轮为通用基线。本结果是已知动作的 VQ 编码重建，不是文字生成效果；名称家族划分也不等同于录制级独立测试。

上述离线完整 FP32 推理包约 102 MB，仅解码包约 54 MB。后者需要兼容 token，不能单独生成动画。新的 UE 实验台使用自定义 UE 骨架的 Schema v2 VQ-VAE 导出模型；数据、权重和具体测量边界见项目实验记录。

#### GASP 动画线程推理验证 / 2026-09-22

UE Editor 构建和三项动画自动化测试通过；RTX 4070 Laptop GPU、60 FPS 上限下，三种播放模式均完成 Walk、Run、Crouch、Jump、Traversal、Idle 六类动作测试，推理失败、回退与游戏线程跳过均为零。

默认采用 30 Hz 输入、每 4 帧推理一次和 8 帧延迟融合，播放延迟约 267 ms；同步推理均值 2.055 ms、P95 2.755 ms，包含传输与等待。同源时间区间的主要运动二阶差分降低约 49%–65%，但 Idle 位置误差及 Traversal 旋转误差仍有局限。此结果用于评估重建连续性与推理开销，尚未覆盖完整玩法、打包、多角色并发或长时运行。

[![GASP Walk：延迟对齐的源动画与 GPU 重建对照](https://raw.githubusercontent.com/Aceared0829/AIAnimationSystem/6a2dba3416172526eada3b1240559c04739d0995/unreal-script/AIAnimation/docs/images/walk_comparison.png)](https://github.com/Aceared0829/AIAnimationSystem/blob/main/unreal-script/AIAnimation/README.md)

<sub>实际实验截图；左右角色按同一源时间对齐。点击查看推理链路、连续性图表、性能报告和复现步骤。</sub>

#### 跑酷参考姿态与硬约束实验（2026-09-23）

新增本地 HTML 参考姿态实验室：手动选帧，比较基线、软条件重建和融合后的平滑硬约束，并审计关键帧位置、局部旋转及邻域连续性。阶段候选、短姿态和已知代理前瞻保留为独立消融记录。

在一条低障碍动画、用户选择的六个参考帧上，软→硬平均关节误差为 **11.322→6.903 cm**；六个参考帧通过等式约束精确到位。加速度误差 **4.008→4.186 cm/帧²**，因此不能宣称消除抽搐。零关键帧误差是后处理约束的结果，不是模型预测精度。当前仍读取完整已知动画窗口，代理模式含已知未来；没有完成稀疏参考生成未知过渡或 UE 跑酷代理执行。

[手选实验室与软/硬对照](https://github.com/Aceared0829/AIAnimationSystem/blob/main/inference/profiling/pose-reference-lab.md) · [审查修复与验证范围](https://github.com/Aceared0829/AIAnimationSystem/blob/main/inference/profiling/pose-reference-review.md)

#### 后续运行时方向

计划由 CMC / Mover 负责移动模拟，动画模型依据实际运动状态与轨迹条件生成姿态。现有推理插件用于实验和性能验证；生产运行时接口、条件生成、目标骨架适配、重定向、接触修正和多人联机仍需逐项实现与验证。

#### 上游与个人增量

模型架构、动作表示、原训练 / 推理代码、G1 权重与参考演示来自 NVIDIA / MotionBricks。这里的新增工作主要是游戏动画工程适配、UE 导出、自定义骨架训练工具、动画线程推理实验台与连续性评估，不将上游模型或演示作为个人自研成果。

现有 G1 权重与参考骨架绑定；自定义 UE 训练入口不支持直接加载 G1 权重微调，也不能把 G1 参考演示当作 UE 实时运行效果。

</details>

[项目仓库](https://github.com/Aceared0829/AIAnimationSystem) · [UE 导出与训练](https://github.com/Aceared0829/AIAnimationSystem/blob/main/unreal-script/AILocomotionSystem/README.md) · [训练结果与限制](https://github.com/Aceared0829/AIAnimationSystem/blob/main/unreal-script/AILocomotionSystem/TrainingResults.md) · [GASP 推理实验与效果](https://github.com/Aceared0829/AIAnimationSystem/blob/main/unreal-script/AIAnimation/README.md)

</details>

<details>
<summary><strong>VerseAngelScript / VAS</strong> — 实现、状态与验证边界</summary>

<sub>早期探索 · LANGUAGE / TOOLCHAIN / RIDER</sub>

**基于 AngelScript 的游戏脚本语言与工具链探索。** 希望在 C++ 风格的类型与对象模型基础上，逐步探索受 Verse 启发的语言能力及 Unreal Engine 开发体验。

**已有实践**

- **脚本与构建约定**：建立 `.vas` 文件约定，统一入口脚本与递归 include 的后缀检查，整理构建器、运行器与测试入口。
- **工程化入口**：整理 CMake / MSVC C++23 开发预设及解决方案，便于构建和运行基础脚本工程。
- **Rider 工具支持**：文件识别、语法高亮、符号索引、补全、跨文件导航、查找用法、重命名及调用关系入口。
- **诊断与集成测试**：接入真实编译器诊断、当前脚本构建 / 运行操作与起步模板，为 include 和声明导航补充 Rider Solution Host 测试。

**当前阶段**：语言本体仍然非常初步，现阶段工作主要集中在基础工程与工具支持。VAS 自有语言扩展、UE 绑定、热更新和可视化编辑尚未实现。

<details>
<summary><strong>语言愿景、工具链与尚未实现的部分</strong></summary>

#### 基础来自哪里

当前编译器、字节码、执行上下文、暂停 / 恢复、GC 与原生 API 绑定建立在 AngelScript 基础之上，不是从零实现的脚本虚拟机。Rider 工具已经开展，不意味着 VAS 语言与 UE 集成已经完成。

#### 计划探索的能力

- 更简洁的语法糖，以及受 Verse 启发的异步、可暂停执行和任务组合语义；不承诺与 Epic Verse 完全兼容。
- UObject / UFunction 反射绑定、对象生命周期与 UE 模块管理。
- 有明确替换边界、状态管理和回滚机制的运行时热更新。
- 以 VAS 源码为逻辑依据的可视化编辑，以及文本 / 图双向同步和语义差异、合并能力。

以上属于规划与后续开发内容。目前更适合把它看作一个语言和开发工具实验，而非可直接投入游戏生产的成熟脚本方案。

</details>

[项目愿景与状态](https://github.com/Aceared0829/VerseAngelScript) · [Rider 插件说明](https://github.com/Aceared0829/VerseAngelScript/blob/master/plugins/rider/README.md) · [工具源码与测试入口](https://github.com/Aceared0829/VerseAngelScript/blob/master/tools/rider-plugin/README.md)

</details>

<details>
<summary><strong>Hybrid-Motion-Imitation</strong> — 实现、状态与验证边界</summary>

<sub>仅 Fork，尚未开始 · MOTION IMITATION</sub>

**为后续动作模仿学习保留的项目。** 目前只是 Fork，还没有开始个人开发或复现。

- **当前已有**：保留上游代码与资料入口，便于后续阅读和实验。
- **尚未开展**：个人实现、训练复现、效果评测或 UE 集成。
- **成果归属**：仓库中已有的方法、代码与演示来自上游，不作为我的开发成果展示。

[我的 Fork](https://github.com/Aceared0829/Hybrid-Motion-Imitation) · [上游项目](https://github.com/jiashunwang/Hybrid-Motion-Imitation)

</details>

## 关注与交流

目前的兴趣集中在四个相互关联的方向：

- **Gameplay**：GAS、角色战斗、动作数据，以及玩法与动画的协作。
- **Engine**：对象生命周期、引擎原生调用路径、对象复用和行为验证。
- **Animation**：角色运动、动画数据处理，以及学习式动画的游戏工程接入。
- **Tools & Language**：脚本构建、IDE 支持、诊断反馈与 UE 编辑器工作流。
- **Agent tooling**：把自己的 Harness 配置收成可安装的插件，而不是只留在本机。

这些是正在实践和学习的方向，不是已经完成的能力清单。欢迎围绕具体实现、问题复现、设计取舍和改进建议交流。

<details>
<summary>关于进度与来源</summary>

项目状态最初整理于 **2026-09-08**；AIAnimationSystem 进展同步于 **2026-09-23**。公开说明对应各项注明日期的仓库与文档，后续进度、实现和验证以各项目的最新记录为准。

编译成功、自动化测试通过、真实场景运行与完整交付是不同层次的验证；页面中引用的验证记录只适用于各自注明的版本与范围。

Fork 项目保留上游来源与适用许可。自有增量、引擎代码、第三方模型和资源不能混为一份个人成果或统一授权的素材库。

页面于 **2026-10-19** 换成随深浅主题切换的字标和项目目录，长说明默认收起；**2026-10-20** 在导航与项目目录之间补了「关于我」。旧的全宽封面还在 `assets/`，不再显示。说明里保留的 GASP 对照图是实验截图，不是装饰。

</details>

<p align="center"><sub>NingHong / Aceared0829 &nbsp; · &nbsp; <a href="https://github.com/Aceared0829?tab=repositories">探索全部仓库</a></sub></p>
