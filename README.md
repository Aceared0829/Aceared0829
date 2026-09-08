<p align="center">
  <img src="assets/ninghong-banner.png" alt="NingHong / Gameplay, Engine, Motion" width="100%">
</p>

<p align="center">
  <strong>我是宁鸿，围绕 Unreal Engine / C++ 学习和实践。</strong><br>
  关注玩法、引擎机制、角色动画，也在探索脚本语言与开发工具。
</p>

<p align="center">
  <a href="#主要实践">主要实践</a> &nbsp; / &nbsp;
  <a href="#早期探索">早期探索</a> &nbsp; / &nbsp;
  <a href="https://github.com/Aceared0829?tab=repositories">全部仓库</a>
</p>

## 主要实践

<table>
<tr>
<td width="50%" valign="top">
  <img src="assets/status-wip.svg" alt="开发中，尚未完成" width="87" height="20">
  <h3><a href="https://github.com/Aceared0829/ZeroG">ZeroG</a></h3>
  <p><strong>UE 5.8 动作游戏原型</strong></p>
  <p>GAS 战斗、武器连招、命中检测与 Traversal。已有相关实现和部分回归测试。</p>
  <p><sub>地图、资产引用和打包流程仍待完善，尚非完整游戏。</sub></p>
  <p><a href="https://github.com/Aceared0829/ZeroG">查看源码</a> &nbsp; · &nbsp; <a href="https://github.com/Aceared0829/ZeroG/releases">可编辑资源</a></p>
</td>
<td width="50%" valign="top">
  <img src="assets/status-wip.svg" alt="开发中，尚未完成" width="87" height="20">
  <h3><a href="https://github.com/Aceared0829/UnrealEngine/tree/fix/generic-object-pool-lifecycle">UE Object Pool</a></h3>
  <p><strong>引擎层 Actor / Component 对象池</strong></p>
  <p>接入原生创建与回收流程，关注生命周期、延迟生成和回调重入。已有实现与自动化测试。</p>
  <p><sub>适用边界仍在验证，不承诺任意对象都能透明复用。</sub></p>
  <p><a href="https://github.com/Aceared0829/UnrealEngine/tree/fix/generic-object-pool-lifecycle">查看引擎分支</a></p>
</td>
</tr>
</table>

<sub>UE 源码分支需要相应的 Epic / GitHub 访问权限；这些修改不代表已被 Epic 官方合入。</sub>

## 早期探索

<table>
<tr><th align="left">项目</th><th align="left">进展与边界</th></tr>
<tr>
  <td width="30%" valign="top">
    <a href="https://github.com/Aceared0829/AIAnimationSystem"><strong>AIAnimationSystem</strong></a><br><br>
    <img src="assets/status-early.svg" alt="早期实验" width="87" height="20">
  </td>
  <td>基于 NVIDIA MotionBricks，探索 UE 动画数据与训练流程。<br><sub>已有实验性导出与训练入口，真实资产端到端流程和生成质量待验证；UE 运行时推理尚未实现。</sub></td>
</tr>
<tr>
  <td valign="top">
    <a href="https://github.com/Aceared0829/VerseAngelScript"><strong>VerseAngelScript</strong></a> / VAS<br><br>
    <img src="assets/status-early.svg" alt="非常早期" width="87" height="20">
  </td>
  <td>基于 AngelScript，探索受 Verse 启发的游戏脚本语言与工具链。<br><sub>目前主要是基础工程、构建入口和 Rider 工具；语言扩展、UE 绑定与热更新仍在规划。</sub></td>
</tr>
<tr>
  <td valign="top">
    <a href="https://github.com/Aceared0829/Hybrid-Motion-Imitation"><strong>Hybrid-Motion-Imitation</strong></a><br><br>
    <img src="assets/status-planned.svg" alt="已 Fork，尚未开始" width="89" height="20">
  </td>
  <td>为后续动作模仿学习保留的项目。<br><sub>目前仅 Fork，尚未开始个人开发或复现；已有代码与演示来自<a href="https://github.com/jiashunwang/Hybrid-Motion-Imitation">上游</a>。</sub></td>
</tr>
</table>

<details>
<summary>关于进度与来源</summary>

这些项目都处于开发、实验或规划阶段，尚非成熟产品。Fork 项目建立在各自上游基础上，上游代码、模型和演示不作为我的新增成果。最新实现、验证记录与已知限制以对应仓库 README 为准。

顶部横幅是个人主页概念插画，不是项目运行截图。

</details>

<p align="center"><sub>欢迎围绕具体实现、问题复现和设计取舍交流。</sub></p>
