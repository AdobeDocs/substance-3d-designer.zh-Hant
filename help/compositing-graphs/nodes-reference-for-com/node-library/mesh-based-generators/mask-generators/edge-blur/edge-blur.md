---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-blur.html"
breadcrumb-title: ''
description: 使用邊緣模糊節點來模糊邊緣遮罩，創造柔和過渡和基於邊緣的平滑風化效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 邊緣模糊
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# 邊緣模糊

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-blur.png){width="128px"}

## 邊緣模糊

**收錄於：***基於網格的生成器**/遮罩生成器*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此遮罩會根據烘焙的曲率貼圖高亮邊緣。 它是較簡單的遮罩產生器之一。

## 參數

### 輸入

* **曲率**： *灰階輸入*\
  用來設計效果的烘焙地圖。
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

### 參數

* **等級**： *0.0 - 1.0*\
  設定邊緣高光的程度。
* **對比**&#x200B;度： *0.0 - 1.0*\
  調整結果的對比度。
* **模糊半徑**： *0.0 - 8.0*&#x200B;設定高亮邊緣的模糊程度。

## 範例圖片

![](../../../../../../assets/edge-blur-ex.gif)

</td>
</tr>
</table>
