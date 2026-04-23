## Table of Contents

Unity / C#

- [同人游戏《少前：攻性协议》](#同人游戏-少女前线攻性协议)
	- [载具和人形角色的混合战场](#载具和人形角色的混合战场)
    - [IK射击姿态控制](#ik射击姿态控制)
    - [手雷投掷瞄准](#手雷投掷瞄准)
    - [节点化关卡配置](#节点化关卡配置)
	- [GAS-in-Unity](#GAS-in-Unity)

Unreal / C++

- [UE-GAS练习](#UE-GAS练习)

---

（动态图加载可能需要耐心等待）

## 同人游戏-少女前线攻性协议

负责完成了游戏全部的程序框架，以及绝大多数具体程序功能。（基于Unity）

![](attachments/少前同人-预览图1.gif)

> 最新发布信息：
>
> [视频链接](https://www.bilibili.com/video/BV1ZePtzqEtF/)（我是团队成员：`时源之元`，该项目后续更新发布由`没头脑盒ZYC`进行）
>
> [下载地址 - 百度网盘](https://pan.baidu.com/s/1oYeQwKE7sQMnsGCOAKTt-A?pwd=GXXY) 提取码: GXXY

### 载具和人形角色的混合战场

载具能使用撞击破坏脆弱环境对象。

载具和人形角色有不同的活动区域，人形角色可以躲入室内，载具在追击时会尝试在最近的室外入口攻击。

合理的模型物理层级划分，人形可以从载具模型下的空间穿过，载具可正常在地面移动。

![](attachments/少前同人-预览图2.gif)

![](attachments/少前同人-预览图3.gif)

### IK射击姿态控制

高级IK绑定结构，支持左手持枪、右手持枪、双手持枪的切换，以及IK控制和动画控制的过渡

![](attachments/少前同人-预览图4-射击姿态IK.gif)

### 手雷投掷瞄准

基于物理抛物线计算弹道、碰撞点及反弹轨迹，手感对标《全境封锁》。

![](attachments/少前同人-预览图5.gif)

### 节点化关卡配置

基于Unity可视化编程制作的关卡配置节点工具，可快速搭建复杂关卡原型。支持的功能包括：角色生成、获取存活角色、按策略选择生成点、添加头顶标记（玩家引导）、添加互动点、设置AI活动限制区域（引导AI按剧本移动）等等

![](attachments/少前同人-预览图6.gif) 

![](attachments/少前同人-关卡配置节点演示概览图.png)

### GAS-in-Unity

借鉴了 Unreal Engine 的 GAS系统（Gameplay Ability System）设计思想，参考 GAS 使用文档制作而来的 Unity GAS。虽然不支持网络联机，功能上来说距离 UE GAS 有差距，不过在单机中已经能用一用了。

我在《少前：攻性协议》中制作的许多技能全都基于这套自制GAS，包括：

- 所有人形角色的投掷物技能
- 部分角色的双持攻击
- 爆头攻击恢复护盾等被动技能
- 受EMP攻击的角色硬直等强制行为
- ......

仓库链接：[GAS-in-Unity](https://github.com/eric02gamer/GameplayAbilitySystem-in-Unity)

---

## UE-GAS练习

在 UE（Unreal Engine）中使用GAS系统（Gameplay Ability System）复刻全境封锁2的芳心终结者装备组效果。充分使用到了GAS 制作RPG游戏的强大功能。

（该项目基于 UE-First Person C++模板）

![](attachments/UEGAS练习.gif)

仓库链接：[ue-gas-practice](https://github.com/eric02gamer/ue-gas-practice)

---