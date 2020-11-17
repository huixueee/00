---
layout: post
title: 科研仪器基本原理（三）SEM
description: SEM的基本原理，比NMR简单太多了。。。。。
date: 2019-09-10 20:36:47
tags: Material Science
categories: Science
toc: true
---
# SEM basics
我用一个对比来快速了解SEM。SEM主要由三部分构成：电子源(electron source),电磁透镜(electromagnetic lenses)以及探测器(electron detector)。
<center>![](https://s2.ax1x.com/2019/09/11/nwr4Ve.png) </center>

## electron source
电子枪，用于生产电子，目前最主要使用钨/六硼化镧作为发射源，通过**热发射**效应产生电子。区别于前两种发射源，目前最先进的场发射电子枪主要的发射机制不是靠加热阴极，而是在尖阴极表面增加强电场，从而降低阴极材料的表面势垒，并且可以使得表面势垒宽度变窄到纳米尺度，从而出现量子隧道效应，在常温甚至在低温下，将大量低能电子通过隧道发射到真空中。
相对于钨丝(尖端厚度10µm)，场发射使用的钨晶体(FEG)的厚度要小得多。
> * 什么是热发射？
热发射（thermionic emission）是一种通过热激发发射载流子的方式。这个现象发生的原因是，提供给载流子的热能使它们能够克服束缚势能（在金属材料中，这束缚势能也被称为功函数或逸出功）。通过热发射产生的载流子可能是电子或者离子。发射载流子之后原始区域会产生一个于被发射载流子总和大小相同、极性相反的载流子。

<center>![](https://s2.ax1x.com/2019/09/11/nwcvyq.png) </center>

## electromagnetic lenses
热发射后的射线是锥形扩散，因此需要添加**电磁透镜**(electromagnetic lens)聚焦电子束。
> * 电磁透镜一般分为两组
汇聚透镜：汇聚透镜用汇聚电子束
物镜：物镜为真空柱中最下方的一个电磁透镜，它负责将电子束的焦点汇聚到样品表面。

<center>![](https://s2.ax1x.com/2019/09/11/nwwyXF.png) </center>

## electron detector
一旦电子束与样品相互作用，就可以检测到几种不同类型的信号。最常用的信号是二次电子(secondary electrons)，背向散射电子(backscattered electrons)，X射线(X-rays)，俄歇电子(Auger electrons)和光子(photons)。
<center>![](https://s2.ax1x.com/2019/09/11/nwcjln.png) </center>

### secondary electron detector(SED)
二次电子（SE）具有低能量（~2至50eV）。它们仅从靠近样品表面的位置喷出。为了吸引（收集）这些低能电子，在探测器的前端施加小的偏压以吸引负电子朝向探测器。
<center>![](https://s2.ax1x.com/2019/09/11/nwgZOx.png) </center>

#### the generation of secondary electron
<center>![](https://s2.ax1x.com/2019/09/11/nwwg0J.gif) </center>

#### secondary electron imaging
<center>![](https://s2.ax1x.com/2019/09/13/nr1CAP.gif) </center>

### backscattered electron detector(BSD)
背散射电子探测器（BSD）安装在物镜极片下方。当入射电子束扫描样品表面时，产生背向散射电子（BSE）。产率受样品的地形，物理和化学特征控制。BSE比二次电子具有更高的能量，可以从样品表面下方提供信息。
#### backscattered electron imaging
<center>![](https://s2.ax1x.com/2019/09/13/nr1Ptf.gif) </center>

> * Compo and Topo
Compo(For Composition):Atomic number contrasting imaging. Lighter elements appear darker while heavier elements appear brighter.
Topo(For Topography):Surface topography imaging similar to Secondary Electron imaging

### X-ray detectors
当电子束与样品相互作用时，发射X射线。这些X射线的能量取决于样品中存在的元素。用于检测样品发射的X射线的最常见系统是能量色散X射线光谱法（EDX）。
> * EDX和EDS的区别
EDX:Energy dispersive x-ray spectrometry
EDS:Energy dispersive spectrometer

#### the generation of X-ray
<center>![](https://s2.ax1x.com/2019/09/11/nww279.gif) </center>

#### X-ray imaging
<center>![](https://s2.ax1x.com/2019/09/13/nr1p7t.gif) </center>

## electron-matter interactions
通过动量定理将这些信号分类。
弹性散射：试样内的电子轨迹发生变化，但其动能和速度基本保持不变。结果是产生反向散射电子（BSE）。
非弹性散射：声子激发(放热)；阴极发光(可见光荧光)；特征X射线辐射;等离子体产生(二次电子);俄歇电子(外壳电子的喷射)。
<center>![](https://s2.ax1x.com/2019/09/11/nwcxO0.gif) </center>

## final image
由于探测器是按点采集，最终图像由许多像素点拼接成。
<center>![](https://s2.ax1x.com/2019/09/11/nwrI5d.gif) </center>



