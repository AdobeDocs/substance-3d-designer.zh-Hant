---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/difference.html"
breadcrumb-title: ''
description: 使用差異混合節點，利用差分模式來混合材質，以創造反轉和對比效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Difference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 差異
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---


# 差異

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](difference.resources/difference.png){width="128px"}

<b>收錄於：</b> 濾鏡>混合

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

在前置與背景輸入之間呈現差異混合模式。 從前景減去背景，回傳絕對結果（絕不為負值）。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>背景</b> <i>色彩輸入</i> |  |
| <b>前景</b> <i>色彩輸入</i> |  |
| <b>面具</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>不透明度</b> <i>0.0 - 1.0</i> | 融合前景與背景的不透明度。 |
| <b>Alpha 混合</b> <i>錯誤/真實</i> | 切換前景與背景 alpha 通道的混合。 若設為 False，則忽略前景的 alpha 通道。 |
