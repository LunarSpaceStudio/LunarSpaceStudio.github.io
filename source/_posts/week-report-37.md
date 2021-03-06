---
title: 第37周难民营周报
date: 2016-09-18 22:06:34
tags:
author: 边境拾遗, 1399
---

# 边境的难民营周报

## 本周工作成果总结
本周完成了难民营资源数据的存储和分发，并进行了测试。现在玩家可以在回合中设置本回合准备分配的资源数量（不超过当前拥有的资源总量），这部分资源会被从资源储量中暂时扣除，玩家仍然可以对准备分配的资源数量进行调整，减少分配的资源会被返还到资源储量中，反之增加的则额外扣除。一旦玩家结束当前回合，准备分配的资源就会被彻底的消耗掉，同时对难民营数据造成某种影响（暂时未知）。

AVG2.0部分，完成了AVG角色制作器和AVG角色的全局保存，现在AVG角色可以在一个额外的编辑器中进行制作，包括设置角色的名字和角色的各种表情的名字和立绘贴图。角色的信息会被保存为xml文件，使用文本编辑器亦可以进行编辑。所有的角色文件都必须存储在指定的文件夹中，否则将会无法被加载。

## 挑战与困难
这个游戏并不复杂，所以单纯从游戏系统上的话没有什么困难的。比较有问题的地方在于事件，AVG和存档这些地方。存档部分我在考虑是否需要重制一个存档系统，还是重构原有的存档系统；AVG系统还在升级中，所以目前存在许多不确定性；事件的问题主要在于我并不知道这个游戏中大概会有一些什么样子的事件，需要有一两个例子来给我说明一下。另外就是游戏的规则上还存在一些不确定的地方，比如数值系统何时发生变化，如何变化等等——可以先不需要确定的数值或者计算公式，但是最好能先告诉我它们会在哪些地方受到影响。

## 下周的工作目标
1. 继续游戏系统的开发，将难民营数值系统完成。届时游戏的功能将会包括——回合开始→玩家设置本回合分配资源→结束回合→资源减少，难民营数值发生变动→新回合开始。这个工作稍微简单，并不会花费几天的时间。工作的重心可能会向AVG系统偏移。
2. AVG系统方面，首先要将AVG角色制作器和AVG剧本制作器连接起来。AVG角色制作器制作了角色之后，AVG剧本制作器要能够读取它们并设置该剧本中出现哪些角色。实验旧的AVG系统能否播放动态生成的AVGData，如果不能的话就改造让它能。如果这两个工作都完成了，就继续扩展当前的AVG动作，然后实验能否将它们转化为旧的AVGData对象并播放。

# 1399的难民营周报

## 本周工作成果总结
本周的开头两天做NGUI到UGUI的转换，然而出现了小小的问题，导致AVG接收不到点击事件，而且找不到原因，于是暂时搁置下来；不过这几天的转换工作让我对界面系统了解更深了

## 下周的工作目标
理清UI交互逻辑，开始着手构建UI的基本框架，做出开始页面UI