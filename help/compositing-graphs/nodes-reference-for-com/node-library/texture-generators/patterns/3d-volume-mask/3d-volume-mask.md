---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-volume-mask.html"
breadcrumb-title: ''
description: 使用 3D 體積遮罩節點，根據 3D 位置建立體積遮罩，以達到進階材質效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Volume Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 體積遮罩
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---


# 3D 體積遮罩

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask.png){width="256px"}

**收錄於：** 生成器*/模式*

**很簡單**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 說明

**3D Volume Mask** 節點會根據 Position **輸入貼圖產生一個基本形狀&#x200B;***的表示*。

</td>
</tr>
</table>

## 參數

### 輸入

* **位置***顏色*\
  描述該原件所表示的三維空間座標&#x200B;*的映射*。\
  **X/Y/Z** 座標分別映射到 **R/G/B** 通道。

### 參數

* **整數形狀** **\
  應表示的基本形狀：
  * *立方*&#x200B;體- *圓柱*&#x200B;體- *球體*
* **比例***浮球*\
  定義&#x200B;*了原件的全域*&#x200B;尺度，並均勻地應用&#x200B;**&#x200B;於所有軸上。
* **尺寸** *Float3*\
  定義形狀在每個軸上的大小。
* **位置輸入***整數*\
  透過 **Position** 輸入表示空間&#x200B;*的方法*：
  * *UV 位置*：使用 *UV 貼圖*。 X/Y（U/V）座標分別映射到R/G通道。 Z軸假設為 *正交的正交向量* 。
  * *世界空間位置：使用**位置圖*&#x200B;將原始物件映射到三維空間中。X/Y/Z 座標分別映射到 R/G/B 通道。
* **位置 UV** *Float2*\
  原始元素在紫外線空間中的位置。\
  *注意*：此參數僅在 Position Input **參數設為 *UV Position* 時可用**。
* **位置** *Float3*\
  原始元素在世界空間中的位置。\
  *注意*：此參數僅在位置輸入&#x200B;**參數設為&#x200B;*世界空間位置*時可用**。
* **旋轉** *Float3*\
  定義了圖形在世界空間中的旋轉。
* **羽寬***浮球*\
  調整從基元表面向內漸變的漸變&#x200B;*寬*&#x200B;度。

## 範例圖片

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant4.jpg){width="256px"}

</td>
</tr>
</table>
