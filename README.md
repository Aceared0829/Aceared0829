<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/header-dark.svg">
    <img src="assets/header-light.svg" alt="Zining Zhao — Unreal Engine / C++" width="640">
  </picture>
</p>

<p align="center">
  我是 Zining Zhao（宁鸿），GitHub 上是 <a href="https://github.com/Aceared0829">@Aceared0829</a>。<br>
  Unreal Engine / C++ · Gameplay · Engine · Animation · Tools<br>
  <sub>把功能做出来，也把它背后的运行机制弄明白。</sub>
</p>

<p align="center">
  <a href="#项目">项目</a>
  &nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="#上游贡献">上游贡献</a>
  &nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="#联系">联系</a>
</p>

## 关于我

主要和 Unreal Engine / C++ 打交道，做玩法、引擎生命周期与角色动画之间需要互相咬合的那一层；也把训练出来的模型接进编辑器与运行时。

- **方向** — Gameplay、Engine、Animation、AI、Tools & Language 五条互相咬合。
- **在做** — MotionWeaver、ZeroG、UnrealAgent，以及自己每天在用的 dsh-kit 和 pkg-installer。
- **AI** — 动画模型进运行时（MotionWeaver）、游戏数据采集（Zing-0.5）、智能体进编辑器（UnrealAgent）。
- **原则** — 实现与验证分开写，上游来源与个人增量分开写；AI 辅助完成的部分如实标注。
- **交流** — [在本仓库提 Issue](https://github.com/Aceared0829/Aceared0829/issues)，或到各项目仓库的 Discussion。

验证记录按版本写明范围：编译通过、自动化测试、真实场景运行和完整交付分开记；页面与仓库里的数字只对应注明的数据集、硬件和提交。

## 项目

实现细节、验证范围与已知限制都在各仓库的 README / `docs/` 里，这里只保留索引。

| 项目 | 做什么 | 状态 |
|---|---|---|
| [**MotionWeaver**](https://github.com/Aceared0829/MotionWeaver) | UE 动画数据、离散姿态训练，以及动画线程上的 GPU 推理 | 实验阶段 |
| [**ZeroG**](https://github.com/Aceared0829/ZeroG) | UE 5.8 C++ 动作原型：GAS 战斗、武器连招、命中检测、Traversal | 原型 |
| [**UnrealAgent**](https://github.com/Aceared0829/UnrealAgent) | 把 Codex / Cursor 的工作流接进 Unreal Editor：Slate、ACP、本机 MCP | Beta · MIT |
| [**pkg-installer**](https://github.com/Aceared0829/pkg-installer) | Arch 上双击安装 .deb / .rpm / .AppImage / .flatpak，免 root，不污染 pacman | v2.2.0 |
| [**dsh-kit**](https://github.com/Aceared0829/dsh-kit) | DeepSeek Harness 插件套件、版本清单与一键安装 | 维护中 |
| [**VerseAngelScript**](https://github.com/Aceared0829/VerseAngelScript) | AngelScript 之上的 UE 脚本语言与 Rider 工具链 | 早期探索 |
| [**Zing-0.5**](https://arxiv.org/abs/2609.17909) | 世界模型论文署名作者；个人贡献是 UE 数据采集中台与采集管线 | 团队项目 |

`deepseek-harness` 是官方仓库的个人 fork，用来跑自建的 Windows 桌面端，插件部分在 dsh-kit。`Hybrid-Motion-Imitation` 目前仅 Fork，尚无个人实现。

## 上游贡献

- **[CachyOS/packageinstaller #85](https://github.com/CachyOS/packageinstaller/pull/85)** — 简体 / 繁体中文界面与语言设置（open）
- **[omdsh-dev/dsh-genui #375](https://github.com/omdsh-dev/dsh-genui/pull/375)** — 修复围栏解析中的单元素数组成员键（merged）
- **[EpicGames/UnrealEngine #15156](https://github.com/EpicGames/UnrealEngine/pull/15156)** — Actor / Component 生命周期与对象复用（open，需访问权限）

## 联系

- **Issue / Discussion** — 具体实现、问题复现、设计取舍都欢迎在这些地方聊。
- **合作** — 目前主要做 UE 的玩法、动画与工具链，也接 Linux 侧的小工具。

<p align="center"><sub>最后更新 2026-11-18 &nbsp;·&nbsp; <a href="https://github.com/Aceared0829?tab=repositories">探索全部仓库</a></sub></p>
