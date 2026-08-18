---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/multi-directional-warp.html"
breadcrumb-title: ''
description: 使用多方向扭曲節點，在多個方向上套用扭曲效果，創造複雜的失真圖案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Multi Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多向曲速
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# 多向曲速

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-directional-warp-color.png)![](../../../../../../assets/multi-directional-warp-grayscalepng.png)

## 多向曲速（灰階）

**收錄於：***濾鏡/效果*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

多向扭曲會多次以相反方向套用[](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md)方向扭曲，而移位的材質保持原位。它與標準的方向曲速不同之處在於，它能向多個方向推進，而原子版本只能推動一個方向。 這樣一來，它解決了經典的問題：方向扭曲總是會把影像推得太遠，而是沿著多個方向或軸線運作，而不是單一方向。

它與 [非均勻方向曲速](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/non-uniform-directional/non-uniform-directional-warp.md) 的主要不同在於其稍微受限：曲速的方向僅透過參數控制，無法透過輸入映射設定。 優點是它稍微容易使用，且根據你的使用情境可以更精準。

## 參數

### 輸入

* **輸入**： *灰階/彩色輸入*\
  將套用扭曲的基礎地圖。 可以是彩色或灰階。
* **強度輸入**： *灰階輸入*\
  強制性的遮罩貼圖必須是灰階，能控制扭曲效果的強度。

### 參數

* **強度**： *0.0 - 20.0*\
  設定扭曲效果的強度，也就是像素要被推出多少。
* **曲速角**： *0.0 - 1.0*\
  設定 Warp 效果的角度或方向。
* **模式**： *平均、最大、最小、連鎖*\
  設定連續通過的混合模式。 只有當指令數達到2或4時才有效！
* **說明**： *1、2、4*&#x200B;扭曲能用多少軸數設定。 1 表示它沿角度方向移動，且方向相反;2 表示角度軸加上垂直軸;4 表示前軸，加上 45 度的陡坡。

## 範例圖片

</td>
</tr>
</table>
