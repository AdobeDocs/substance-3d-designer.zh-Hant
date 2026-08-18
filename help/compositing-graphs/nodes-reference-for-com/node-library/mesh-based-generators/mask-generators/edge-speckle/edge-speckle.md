---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-speckle.html"
breadcrumb-title: ''
description: 使用邊緣斑點節點在網格邊緣產生斑點磨損模式，創造逼真的邊緣損傷效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Speckle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 邊緣斑點
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---


# 邊緣斑點

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-speckle.png){width="128px"}

## 邊緣斑點

**收錄於：***基於網格的生成器**/遮罩生成器*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此遮罩表示邊緣，並加以輕微斑點將其分割。 另見 [Edge Dirt](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md)。

## 參數

### 輸入

* **曲率**： *灰階輸入*\
  烘焙地圖用於邊緣高亮。 必備！
* **變異遮罩**： *灰階輸入*\
  可選的遮罩槽用於遮蔽節點的效果。 啟用「覆蓋變異遮罩」。
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

### 參數

* **等級**： *0.0 - 1.0*\
  設定邊緣高亮的總量。
* **對比**&#x200B;度： *0.0 - 1.0*\
  調整結果的對比度。
* **邊選擇**： *0.0 - 1.0*&#x200B;設定凸邊的影響。
* **變化**： *0.0 - 1.0*&#x200B;設定變化遮罩破壞效果的程度。
* **覆蓋變體遮罩**： *False/True*&#x200B;覆蓋的內建遮罩，並有自訂輸入槽。

## 範例圖片

![](../../../../../../assets/edge-speckle-ex.gif)

</td>
</tr>
</table>
