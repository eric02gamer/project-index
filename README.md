## Table of Contents

Unity / C#

- [同人TPS游戏《少前：攻性协议》](#同人游戏-少女前线攻性协议)
- [GAS-in-Unity](#GAS-in-Unity)
- [动作游戏战斗原型](#动作游戏战斗原型)

Unreal Engine

- [UE-GAS练习](#UE-GAS练习)
- [UE-多人游戏练习](#UE-多人游戏练习)
- [UE-TeamCity-持续部署](#UE-TeamCity-持续部署)

（动态图加载可能需要耐心等待）

---

## 同人游戏-少女前线攻性协议

负责完成了TPS同人游戏全部的程序框架，以及绝大多数具体程序功能。（基于Unity）。

> 点击链接查看详细亮点功能动图展示
> 
> [少前-攻性协议](sub-pages/少前-攻性协议.md)
> 
> （该项目为非商业化的少女前线同人游戏项目，下载游玩完全免费，无需捐赠等门槛，我是团队成员：`时源之元`，该项目后续更新发布交由`没头脑盒ZYC`进行）
> 
> 近期发布信息：
> - [视频链接](https://www.bilibili.com/video/BV1ZePtzqEtF/)
> - [下载地址 - 百度网盘](https://pan.baidu.com/s/1oYeQwKE7sQMnsGCOAKTt-A?pwd=GXXY) 提取码: GXXY

![](attachments/少前同人-预览图1.gif)

---

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

## 动作游戏战斗原型

独立完成的动作游戏战斗原型，包含动作游戏常用技术点，例如：输入缓冲，技能编辑器，连招，受击反馈，RootMotion等。

> 点击下面链接查看详细亮点功能动图展示。
> 
> [动作游戏战斗原型](sub-pages/动作游戏战斗原型.md)
> 
> Demo下载地址：前往本仓库Releases页面下载 `act-demo.7z` ，解压即可体验。

![](attachments/Act-普攻连击.gif)

---

## UE-GAS练习

在 UE（Unreal Engine）中使用GAS系统（Gameplay Ability System）复刻全境封锁2的芳心终结者装备组效果。充分使用到了 GAS 制作涉及复杂数值计算 RPG 游戏的强大功能。

（该项目基于 UE-First Person C++模板）

![](attachments/UEGAS练习.gif)

仓库链接：[ue-gas-practice](https://github.com/eric02gamer/ue-gas-practice)

---

## UE-多人游戏练习

可本地运行的多人射击游戏Demo，核心网络同步模块，重点解决“网络延迟导致攻击判定不准”这一核心体验问题，并提供了可交互的对比验证工具。

- 基于延迟补偿实现高精度射线命中判定，回溯到玩家开火瞬间的世界快照。
- 服务器持续记录并更新玩家世界快照，关键射线判定逻辑由服务器执行；
- 基于 NTP 思想的网络时间同步，多次采样取均值减弱网络波动影响（更严峻情况可能得考虑卡尔曼滤波等算法）
- 可打包专有服务器（Dedicated Server）并使用作弊码启用调试功能，验证补偿效果带来的实际体验提升

> 该部分预览图较大，请点击查看
> - [关闭服务器延时补偿](attachments/UE网络练习-关闭服务器延时补偿.gif)
> - [启用服务器延时补偿](attachments/UE网络练习-启用服务器延时补偿.gif)

---

## UE-TeamCity-持续部署

基于 TeamCity 的 UE 持续部署，使用 VCS Trigger，轮询检查 Github 仓库的变更，并自动在发生变更时触发UAT编译并打包游戏到指定目录。用于自动化测试和保障游戏质量。使用 PostgreSQL 管理打包记录。

![自动调用打包](attachments/UE-CD-调用打包.png)

![打包记录和追溯](attachments/UE-CD-打包记录和追溯.png)

---
