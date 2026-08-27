---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/linear-burn.html"
breadcrumb-title: ''
description: 使用線性燒錄節點，利用線性燒錄模式來混合材質，創造暗化和對比效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Linear Burn
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 線性燃燒
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 4%

---


# 線性燃燒

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](linear-burn.resources/linear-burn.png){width="128px"}

<b>收錄於：</b> 濾鏡>混合

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

進行線性燃燒混合。 數學公式為前景 + 背景 - 1。

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
