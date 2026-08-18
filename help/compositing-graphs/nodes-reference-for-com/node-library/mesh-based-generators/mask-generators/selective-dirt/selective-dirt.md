---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/selective-dirt.html"
breadcrumb-title: ''
description: 使用選擇性泥土節點，根據網格幾何產生選擇性泥土累積遮罩，以實現逼真的風化效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Selective Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 選擇性泥土
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---


# 選擇性泥土

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/selective-dirt.png){width="128px"}

## 選擇性泥土

**收錄於：***基於網格的生成器**/遮罩生成器*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

這個 [Substance 3D Designer](https://www.adobe.com/tw/products/substance3d-designer.html) 遮罩代表凸邊上的簡單泥土效果。

## 參數

### 輸入

* **曲率**： *灰階輸入*\
  烘焙貼圖用於內部效果和遮罩。
* **變異遮罩**： *灰階輸入*\
  可透過參數啟用可選的變異地圖。
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

### 參數

* **等級**： *0.0 - 1.0*\
  設定效果的總強度，逐步揭露。
* **對比**&#x200B;度： *0.0 - 1.0*\
  調整結果的對比度。
* **變化**： *0.0 - 1.0*&#x200B;設定變化/垃圾搖滾的程度，以融入效果中。
* **覆蓋變異遮罩**： *假/真*&#x200B;啟用自訂輸入槽覆蓋變體。

## 範例圖片

![](../../../../../../assets/selective-dirt-ex.gif)

</td>
</tr>
</table>
