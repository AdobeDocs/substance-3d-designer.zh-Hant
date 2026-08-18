---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-notch.html"
breadcrumb-title: ''
description: 使用邊緣缺口節點在網格邊緣上產生缺口圖案，創造逼真的邊緣損傷和縮排效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Notch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 邊緣缺口
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 1%

---


# 邊緣缺口

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-notch.png){width="128px"}

## 邊緣缺口

**收錄於：***基於網格的生成器**/遮罩生成器*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此遮罩代表凸起邊緣的簡單遮罩，中間有高頻雜訊。 更多選項請參考 [邊緣泥土](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md) 或 [邊緣損傷](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-damages/edge-damages.md) 。

## 輸入

* **曲率**： *灰階輸入*\
  烘焙地圖用於高亮邊緣。 必備！
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

## 參數

* **等級**： *0.0 - 1.0*\
  設定邊緣缺口效應的音量。
* **對比**&#x200B;度： *0.0 - 1.0*\
  調整結果的對比度。

## 範例圖片

![](../../../../../../assets/edge-notch-ex.gif)

</td>
</tr>
</table>
