---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/paint-wear.html"
breadcrumb-title: ''
description: 使用 Paint Wear 節點根據網格幾何生成油漆磨損遮罩，創造逼真的油漆剝落效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Paint Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 油漆磨損
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 1%

---


# 油漆磨損

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/paint-wear.png){width="128px"}

## 油漆磨損

**收錄於：***基於網格的生成器**/遮罩生成器*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

這個面具象徵油漆剝落與邊緣磨損。

## 參數

### 輸入

* **環境遮蔽**： *灰階輸入*\
  烘焙貼圖用於內部效果和遮罩。
* **曲率**： *灰階輸入*\
  烘焙貼圖用於內部效果和遮罩。
* **變異遮罩**： *灰階輸入*\
  遮罩槽用於遮蔽節點的效果。
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

### 參數

* **等級**： *0.0 - 1.0*\
  設定總油漆磨損量，逐漸顯現。
* **對比**&#x200B;度： *0.0 - 1.0*\
  調整結果的對比度。
* **遮蔽度**： *0.0 - 1.0*&#x200B;設定烘焙 AO 在較暗區域防止磨損的效果。
* **半徑**： *0.0 - 2.0*&#x200B;設定剝削效應從凸邊擴散的範圍。
* **變化**： *0.0 - 1.0*&#x200B;設定變化量（垃圾搖滾）以融入效果中。
* **覆蓋變體遮罩**： *False/True*&#x200B;啟用自訂變體（grunge）地圖輸入槽。

## 範例圖片

![](../../../../../../assets/paint-wear-ex.gif)

</td>
</tr>
</table>
