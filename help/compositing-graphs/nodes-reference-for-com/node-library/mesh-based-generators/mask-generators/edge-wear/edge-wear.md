---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-wear.html"
breadcrumb-title: ''
description: 使用邊緣磨損節點在網格邊緣產生磨損遮罩，以創造逼真的邊緣損傷和風化效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 邊緣磨損
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---


# 邊緣磨損

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-wear.png){width="128px"}

## 邊緣磨損

**收錄於：***基於網格的生成器**/遮罩生成器*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此節點代表物件邊緣的磨損。 它有不少參數，但使用起來並不容易：我們建議你多試試看，感受一下。 節點功能相當強大，雖然無法自訂覆蓋遮罩。

## 參數

### 輸入

* **曲率**： *灰階輸入*\
  用於內部效果與遮罩的烘焙貼圖
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

### 參數

* **等級**： *0.0 - 1.0*\
  設定效果的總擴散範圍。
* **對比**&#x200B;度： *0.0 - 1.0*\
  調整結果的對比度。
* **閾值**： *0.0 - 1.0*&#x200B;類似等級，設定效果的總擴散範圍。
* **邊緣寬度**： *0.0 - 1.0*&#x200B;設定高光效果的飽滿度。 減少讓它們更稀疏。
* **無障礙**： *0.0 - 1.0*\
  這樣可以調整噪音的大小，讓聲音融合進去，打破平滑感。

## 範例圖片

![](../../../../../../assets/edge-wear-ex.gif)

</td>
</tr>
</table>
