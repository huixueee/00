---
layout: post
title: 科研仪器基本原理（二）NMR
description: NMR的基本原理
date: 2019-09-09 20:36:47
tags: Material Science
categories: Science
toc: true
---
# NMR basics

## Spin
在量子力学中，**自旋**（Spin）是粒子所具有的内禀性质，其运算规则类似于经典力学的角动量，并因此产生一个磁场。NMR所检测的原子核中含有质子、中子这样亚原子粒子，他们的自旋通常指的总角动量，即亚原子粒子的自旋角动量和轨道角动量的总和。
> *中子作为电中性粒子为什么可以自旋也能产生磁场？
中子作为亚原子粒子，本质由三种夸克这种基本粒子组成，三种夸克的净电荷为零使得中子呈电中性，然而三种夸克自旋的总角动量不为零，因而具有微小但非零的磁矩。
### Pauli exclusion principle
质子与中子作为自旋为1/2的粒子，遵循费米-狄拉克统计，因而他们是**费米子**（fermion）中的成员。所有费米子都服从**泡利不相容原理**（Pauli exclusion principle），泡利原理表明，两个全同的费米子不能处于相同的量子态。换句话说处于同一原子轨域的两个同种费米子必定拥有相反的自旋方向。
### Nuclear spin
质子与中子共同构成了原子核，整个原子核的自旋看上去很“**复杂**”。然而根据泡利原理，我们可以很容易的得到原子核的自旋。这里我们引入一个新的定义：**净自旋**（Net Spin），当同一能级存在两个质子时，由于泡利原理的限制，其中一个质子自旋为1/2，那么另一个质子的自旋为-1/2。二者自旋角动量相互抵消，此时的净自旋为0.
只有净自旋不为0的原子核才能够产生磁矩被NMR检测。显然并不是所有元素都能被NMR所识别。
<center>![](https://s2.ax1x.com/2019/09/10/nakxWF.png) </center>

## Nucleus in magnetic field
我们将原子核类比为一个小磁铁，在正常状态下，原子核做无规运动，此时的磁矩方向也是随机分布。我们在Z轴上给予一个恒定磁场B0，原子核在磁场的作用下其磁矩与磁场方向平行，而这时原子核在磁场中存在两种分布，一种磁矩方向与磁场方向相同（**α-spin**），而另外一种与磁场方向相反（**β-spin**）。

<center>![](https://s2.ax1x.com/2019/09/10/naApQJ.png) </center>
<center>![](https://s2.ax1x.com/2019/09/10/naACLR.png) </center>
<center>![](https://s2.ax1x.com/2019/09/10/naA9y9.png) </center>

> * 为什么存在β-spin？
实际上原子核的自旋并不是与磁场方向垂直，而是有一定角度(如图)，这种自转轴绕着另一轴旋转的现象也叫**进动**(Precession)，这样在施加磁场后，最终的自旋角动量便拥有两种自旋方向。其中β-spin的原子核具有更高的能量，且能量大小与施加的场强B0成正比。
><center>![](https://s2.ax1x.com/2019/09/10/nakLd0.png) </center>

## RF radiation
由于原子核存在α-spin与β-spin，这两者的能量差称之为ΔE，当施加一定大小的射频辐射时(RF radiation),根据光子能量公式，只有一定频率的能量才能被吸收。这时在Frequency中便可以检测到特定频率被吸收，这便是NMR的基本原理。
<center>![](https://s2.ax1x.com/2019/09/10/nakzz4.png) </center>
<center>![](https://s2.ax1x.com/2019/09/10/nakOoV.png) </center>
<center>![](https://s2.ax1x.com/2019/09/10/nakvJU.png) </center>
我们通过一组动态图更直观的观察原子核在磁场下的运动模式。

首先空间无序分布的所有原子拥有竖直与水平两种方向的分量，由于**玻尔兹曼分布**使得竖直方向矢量向上。
> *什么是玻尔兹曼分布？
简单理解，通常情况下，在正温度范围内，处于低能级的原子数量要大于处于高能级的原子数量，这种分布模式在物理中被称为“玻尔兹曼分布”（Boltzmann distribution）。
<center>![](https://s2.ax1x.com/2019/09/18/nHjDDH.gif) </center>
接着在磁场作用下，所有原子从低能级跃迁到高能级(竖直方向矢量向下移动)，水平方向上原本处于不同相位的原子向相同方向进动。最终所有原子在水平方向上拥有了相同的角动量。
<center>![](https://s2.ax1x.com/2019/10/25/KwrYZV.gif) </center>
<center>![](https://s2.ax1x.com/2019/09/18/nHjwvD.gif) </center>
<center>![](https://s2.ax1x.com/2019/09/18/nHjUC6.gif) </center>
接着撤除磁场，经过一段时间后原子重新回到初始状态。而仪器则记录原子从被约束到恢复自由这个过程。
<center>![](https://s2.ax1x.com/2019/09/18/nHjdgO.gif) </center>
<center>![](https://s2.ax1x.com/2019/09/18/nHjBKe.gif) </center>

## Compound in magnetic field
然而NMR检测的化合物，每一个原子核都不会完美的在磁场中呈现出α-spin。原子核会受到周围电子的影响而形成**电磁屏蔽**效应。这时我们再施加RF，其中受到电磁屏蔽的原子核旋转到β-spin时的能量(**E2**)会小于理想状态下由α-spin转动至β-spin时所需的能量(**E1**)。这时能观察到不同程度shield的原子核在坐标系上的分布。
<center>![](https://s2.ax1x.com/2019/09/11/ndKX59.png) </center>
<center>![](https://s2.ax1x.com/2019/09/11/ndKOUJ.png) </center>
<center>![](https://s2.ax1x.com/2019/09/11/ndKvCR.png) </center>

## Upfield and downfield
这里我们接着引入一个新的定义:**有效磁场**(B-effective),他的大小等于施加磁场大小(B-applied)减去电磁屏蔽所产生的磁场(B-local)，屏蔽效应越大，磁场效应越小，导致共振频率降低，我们一般称此现象的原子核位于**高场区**(Upfield)。反之屏蔽效应越小，磁场效应越大，共振频率变大，此原子核位于**低场区**(Downfield)。
<center>![](https://s2.ax1x.com/2019/09/11/ndNf1g.png) </center>

## spin–spin coupling(splitting)

