---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/light.html"
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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 9%

---


# 亮

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](light.resources/light-2.png){width="128px"}

<b>收錄於：</b> 基於網格的生成器>遮罩生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

這個遮罩和其他生成器有點不同：它純粹根據世界空間法線貼圖做假光照，回傳一個黑白「光照貼圖」遮罩。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>水平角</b> <i>0.0 - 1.0</i> | 設定假燈的水平角度。 |
| <b>垂直角</b> <i>0.0 - 1.0</i> | 設定假燈的垂直角度。 |
| <b>高光光澤</b> <i>0.0 - 0.999</i> | 設定標示區域的衰減擴散。 |
| <b>精彩片段等級</b> <i>0.0 - 1.0</i> | 設定高亮區域的亮度等級。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="light.resources/light-ex.gif" />
        </td>
    </tr>
</table>
