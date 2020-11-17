---
layout: post
title: 3d科研图（四）流体
description: 详细教程，利用C4D制作两种简单流体。
date: 2019-11-28 11:36:47
tags: [Rhino,C4D]
categories: 3D Design
toc: true
---
本教程适合C4D入门新人学习，[Realflow插件下载](https://pan.baidu.com/s/13br8LwVpNR1OTCEx1YJXDw) 提取码：**kg6d**。

## Realflow碰撞生成浪花

### 前期工作
首先绘制一个容器以及一个比容器空腔稍小的填充体。
<center>![](https://s2.ax1x.com/2019/11/28/QiY0Q1.png) </center>

### 填充液体
选择`Realflow sense`，在`Emitters`中选择`Fill`，随后在`Fill-Emission-Body`中添加你要填充液体的填充物。
<center>![](https://s2.ax1x.com/2019/11/28/QiYBsx.png) </center>

### Gravity以及Collider标签
随后点击动画，发现所有的液体都离开容器了，这是因为初始液体处于真空状态，添加`Realflow-Daemons-Gravity`。
运行动画后发现液体穿过了容器，这是因为**C4D认为容器是一个没有碰撞体积的物件**。为了让计算机正确识别容器是具有碰撞体积的物件，给容器添加标签`标签-Realflow标签-Collider`，再次运行动画就发现液体正确的填满了容器。
<center>![](https://s2.ax1x.com/2019/11/28/QiYdzR.png) </center>

### Crown标签
添加Crown标签`Realflow-Daemons-Crown`。这里需要注意`Crown`标签下`Creation frame`以及`Acting time`两个选项的作用。
> * Creation frame 以及 Acting time
Creation frame：溅射效果开始帧。
Acting time：溅射效果持续时间，数值越大效果越强烈。

### 最终效果
配合上球体下落，控制好帧数模仿撞击液体产生溅射效果。
<center>![](https://s2.ax1x.com/2019/11/27/QCosXt.png) </center>

## Realflow沿着固定轨迹流动

### 前期工作
绘制一条线。

### 发射器选择
为了尽量模仿出水流效果，`Emmiters`选择`Circle`,其他发射器效果可以自行尝试。

### 固定路径
选择`Realflow-Daemons-DSpline`，将先前的曲线拽入`Spline object`中。调整发射器位置与角度，使其与第一个`Spline Control Circle`对应。这里需要注意`DSpline`标签下`Vortex strength`，`Axial strength`以及`Radial strength`三个选项的作用。

> * Vortex strength，Axial strength以及Radial strength
Vortex strength：涡流强度，液体以螺旋状态喷射，数值越大涡流越强。
Axial strength：轴向力强度，使液体沿喷射面法线喷射，越强越倾向垂直喷射。
Radial strength：最关键的选项，控制水流与路径的契合程度，数值越大水流运动轨迹越接近给定路径。

### 最终效果
配合上噪波，控制好噪波强度。
<center>![](https://s2.ax1x.com/2019/11/27/QCo6nP.png) </center>

## OC渲染液体材质注意事项
OC渲染器在渲染液体等透明材质时，会有很多噪点，这些噪点也被称为**热成像噪点**，这里给出几种消除办法。

> * 消除办法
增加Samples数值，1080p的屏幕2500为极限，继续增加看不出效果差异。
减少GI clamp，该数值可以简单理解成进光量，进光量越少画面越暗，同时热成像噪点越少。
OC camera标签下减少Hotpixel removal数值。