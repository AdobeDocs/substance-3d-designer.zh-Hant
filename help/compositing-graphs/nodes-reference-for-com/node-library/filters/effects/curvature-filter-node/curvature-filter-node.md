---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-filter-node.html"
breadcrumb-title: ''
description: 使用曲率濾波器節點，從高度圖產生曲率圖，以偵測凸面與凹面。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 曲率（濾波節點）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 07f136ebd89fbe737b6c042f1275bd348b2be514
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# 曲率（濾波節點）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](curvature-filter-node.resources/curvature-1.png){width="128px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

執行簡單且嚴格的單次曲率轉換為輸入 [法線貼](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)圖。 結果的地圖凸面區域帶有白色調，凹面則以黑色調呈現。 曲率總是會產生像素級的細線和銳利的過渡。

這個節點對於快速高亮或調暗某些邊緣很有用。 與 Curvature Smooth[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md)（品質較高）和 [Curvature Sobel](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md)（選項較多）相比，它有限制。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>強度</b> <i>0.0 - 10.0</i> | 效果的強度。 這樣可以增加結果的對比度。 |
| <b>一般格式</b> <i>DirectX、OpenGL</i> | 切換不同的法線貼圖格式（反轉綠色通道）。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="curvature-filter-node.resources/curvature-ex.png" />
        </td>
    </tr>
</table>
