---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/dissolve.html"
breadcrumb-title: ''
description: 使用 Dissolve 節點用 Dissolve 模式混合材質，來創造材質間的過渡與淡出效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Dissolve
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 溶解
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 4%

---


# 溶解

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dissolve.resources/dissolve-2.png){width="128px"}

<b>收錄於：</b> 濾鏡>混合

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

將兩個輸入混合在一起，並以白噪音作為過渡的遮罩。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>前景</b> <i>色彩輸入</i> |  |
| <b>背景</b> <i>色彩輸入</i> |  |
| <b>面具</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>不透明度</b> <i>0.0 - 1.0</i> | 融合前景與背景的不透明度。 |
| <b>Alpha 混合</b> <i>錯誤/真實</i> | 切換前景與背景 alpha 通道的混合。 若設為 False，則忽略前景的 alpha 通道。 |
