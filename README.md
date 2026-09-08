# NingHong

你好，我是宁鸿，GitHub ID 是 **Aceared0829**。

主要在学习和实践 **Unreal Engine / C++**，关注 Gameplay、引擎源码、角色动画与脚本工具链。喜欢从具体功能出发，逐步理解它背后的运行机制。

这里的项目大多还在开发中：有已经落地的代码，也有尚待验证的原型和未实现的想法。下面分别记录它们的方向与当前进度。

[ZeroG](#zerog) · [UE 对象池](#unreal-engine-分支generic-object-pool) · [AIAnimationSystem](#aianimationsystem) · [VAS](#verseangelscriptvas) · [Hybrid-Motion-Imitation](#hybrid-motion-imitation)

## 项目

### [ZeroG](https://github.com/Aceared0829/ZeroG)

**动作游戏技术验证项目 · 开发中，尚未完成**

基于 UE 5.8 的 C++ 动作游戏原型，围绕 GAS 战斗、武器与连招、命中检测、角色运动和 Traversal 展开。

- 已有相关 C++ 系统与部分回归测试，用来实践 Gameplay 和角色系统开发。
- 源码已公开，可编辑场景和素材通过 [Releases](https://github.com/Aceared0829/ZeroG/releases) 提供。
- 仍有资产引用、地图和打包流程等问题待完善；不是完整游戏，也不是下载后即可游玩的成品。

### [Unreal Engine 分支：Generic Object Pool](https://github.com/Aceared0829/UnrealEngine/tree/fix/generic-object-pool-lifecycle)

**引擎源码改造 · 持续完善中**

在 Unreal Engine 源码基础上探索 Actor / Component 对象池，将复用机制接入原生创建与回收流程。

- 已有基于 `UWorldSubsystem` 的对象池实现、配置与相关自动化测试。
- 主要关注复用时的生命周期、延迟生成、回调重入和状态管理。
- 仍在完善适用边界与验证，不承诺任意对象都能透明复用，也不将其视为已完成的通用生产方案。

该分支属于受访问限制的 UE 源码仓库，访问需要相应的 Epic / GitHub 权限；修改不代表已被 Epic 官方合入。

### [AIAnimationSystem](https://github.com/Aceared0829/AIAnimationSystem)

**面向 UE 的 AI 角色动画 · 早期实验**

基于 NVIDIA GR00T-WholeBodyControl / MotionBricks，探索从 UE 动画数据到模型训练、再到角色姿态生成的流程。

- 目前已有实验性的 UE 动画导出、自定义骨架数据预处理与训练入口。
- 真实 UE 资产的端到端流程、完整训练和动作生成质量仍待验证。
- UE 运行时推理与 AnimGraph 接入尚未实现；现有上游模型和参考演示不代表已完成 UE 集成。

### [VerseAngelScript（VAS）](https://github.com/Aceared0829/VerseAngelScript)

**面向 UE 的脚本语言与工具链 · 非常早期**

基于 AngelScript，探索受 Verse 启发、面向游戏逻辑的语言能力，以及与 Unreal Engine 结合的开发体验。

- 当前工作主要是基础工程、`.vas` 构建入口和 Rider 工具支持。
- VAS 语言扩展、UE 绑定、热更新和可视化编辑仍属于后续规划。
- 编译器与运行时建立在 AngelScript 基础之上；它还不是一门已完成的 UE 脚本语言。

### [Hybrid-Motion-Imitation](https://github.com/Aceared0829/Hybrid-Motion-Imitation)

**动作模仿学习 · 已 Fork，尚未开始个人开发**

为后续学习和实验保留的项目。目前尚未开展个人实现或复现，仓库中的代码、方法与演示来自[上游项目](https://github.com/jiashunwang/Hybrid-Motion-Imitation)，不作为我的开发成果展示。

## 正在关注

- UE C++ Gameplay、GAS、角色运动与动画系统。
- 引擎对象生命周期、对象复用与测试验证。
- 游戏动画数据流程、学习式动画和脚本开发工具。

欢迎围绕具体实现、问题复现和设计取舍交流。各项目的最新进度、已知限制和上游来源以对应仓库说明为准。
