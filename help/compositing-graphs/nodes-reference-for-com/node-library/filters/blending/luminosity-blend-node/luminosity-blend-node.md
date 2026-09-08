---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/luminosity-blend-node.html"
breadcrumb-title: ''
description: 使用亮度混合節點根據亮度值混合材質，創造基於亮度的複合效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Luminosity (Blend Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 亮度（混合節點）
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 3%

---


# 亮度（混合節點）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<b>收錄於：</b> 濾鏡>混合

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

執行亮度混合模式，保留背景的色調與色度，同時採用前景的亮度。

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
