---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/ground-dirt.html"
breadcrumb-title: ''
description: 使用 Ground Dirt 節點根據網格位置和相對於地面的方向產生泥土累積遮罩。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Ground Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 地面泥土
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# 地面泥土

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/ground-dirt.png){width="128px"}

## 地面泥土

**收錄於：***基於網格的生成器**/遮罩生成器*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

這個面具代表從地面往上累積的泥土，與 [「從下到上](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/bottom-to-top/bottom-to-top.md) 」或 [「塵埃](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/dust/dust.md)」相反。 它沒有自訂地圖覆蓋功能。

## 輸入

* **位置**： *灰階輸入*\
  將烘焙位置圖貼入基底效果。 必備！
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

## 參數

* **等級**： *0.0 - 1.0*\
  設定土壤的整體外觀高度。
* **對比**&#x200B;度： *0.0 - 1.0*\
  調整結果的對比度。
* **泥土高度**： *0.0 - 1.0*&#x200B;設定土土應該出現的高度（比例）。

## 範例圖片

![](../../../../../../assets/ground-dirt-ex.gif)

</td>
</tr>
</table>
