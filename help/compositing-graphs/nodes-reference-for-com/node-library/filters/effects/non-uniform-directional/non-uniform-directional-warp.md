---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/non-uniform-directional-warp.html"
breadcrumb-title: ''
description: 使用非均勻方向扭曲節點來套用非均勻方向扭曲，創造多樣化的失真效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Non Uniform Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 非均勻方向曲速
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---


# 非均勻方向曲速

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-directional-warp-color.png)![](../../../../../../assets/non-uniform-directional-warp-grayscale.png)

## 非制服導演。 扭曲（灰階）

**收錄於：***濾鏡/效果*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

非均勻方向扭曲是方向扭曲](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md)的進階版本[，允許透過影像輸入來驅動扭曲的強度與方向。它能提供更多控制，並能產生非常有用且有趣的影像變形，類似 [於斜坡模糊](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md)。

它與 [多向扭曲](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/multi-directional-warp/multi-directional-warp.md) 不同，因為它允許透過自訂地圖輸入控制角度，而多方向扭曲則只能透過參數控制方向。 這表示你可以創造進階的拖曳和彎曲效果，這是其他方法無法做到的。

## 參數

### 輸入

* **輸入**： *灰階輸入*\
  將套用扭曲的基礎地圖。
* **強度輸入**： *灰階輸入*\
  強制性的遮罩貼圖必須是灰階，能控制扭曲效果的強度。
* **扭曲角度輸入**： *灰階輸入*\
  強制性的遮罩貼圖必須是灰階，因為它驅動扭曲效果的角度。

### 參數

* **強度**： *0.0 - 20.0*\
  設定扭曲效果的強度，也就是像素要被推出多少。
* **曲速角**： *0.0 - 1.0*\
  設定 Warp 效果的角度或方向。
* **曲速角輸入倍數**： *0.0 - 1.0*\
  設定扭曲角度輸入貼圖的效果。 曲速角輸入映射將用於從 0 插值到該參數的值。
* **越野模式**： *最小、最大、平均*\
  設定軌跡的融合方式。
* **步道長度**： *0.0 - 1.0*\
  設定步道長度。
* **尾跡淡化**： *0.0 - 1.0*\
  設定每條痕跡應該淡出的程度
* **軌跡曲線**： *-1.0 - 1.0*&#x200B;只有在軌跡淡化 i 時才有效，而非 0。 設定漸入效應的行為方式。

## 範例圖片

</td>
</tr>
</table>
