---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-sobel.html"
breadcrumb-title: ''
description: 使用 Curvature Sobel 節點來偵測曲率邊，使用索貝爾運算子來建立基於邊緣的遮罩。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 曲率索貝爾
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 4%

---


# 曲率索貝爾

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/curvature-sobel.png){width="128px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

執行簡單且嚴格的單次曲率轉換為輸入 [法線貼](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)圖。 結果的地圖凸面區域帶有白色調，凹面則以黑色調呈現。 曲率總是會產生更粗的線條和銳利的過渡。

此節點有助於快速高亮或調暗特定邊緣。 它與 [Curvature](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md) 略有不同，因為它產生的效果品質較佳，但仍帶有銳利且刺耳的感覺。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>強度</b> <i>0.0 - 1.0</i> | 效果強度會調整對比度。 |
| <b>正常型</b> <i>DirectX、OpenGL</i> |  |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/curv-sobel-ex.png" />
        </td>
    </tr>
</table>
