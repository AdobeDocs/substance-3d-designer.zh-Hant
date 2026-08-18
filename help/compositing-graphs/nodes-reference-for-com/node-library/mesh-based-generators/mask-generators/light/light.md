---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/light.html"
breadcrumb-title: ''
description: 利用 Light 節點根據網格光照條件產生遮罩，創造逼真的材質變化。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 亮
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 3%

---


# 亮

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/light-2.png){width="128px"}

## 亮

**收錄於：***基於網格的生成器**/遮罩生成器*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

這個遮罩和其他生成器有點不同：它純粹根據世界空間法線貼圖做假光照，回傳一個黑白「光照貼圖」遮罩。

## 參數

* **水平角度**： *0.0 - 1.0*&#x200B;設定假燈的水平角度。
* **垂直角度**： *0.0 - 1.0*&#x200B;設定假燈的垂直角度。
* **高亮光澤度**： *0.0 - 0.999*&#x200B;設定高亮區域的衰減擴散。
* **高亮等級**： *0.0 - 1.0*&#x200B;設定高亮區域的亮度等級。

## 範例圖片

![](../../../../../../assets/light-ex.gif)

</td>
</tr>
</table>
