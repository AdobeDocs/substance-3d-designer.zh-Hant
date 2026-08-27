---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-selector.html"
breadcrumb-title: ''
description: 使用材質選擇節點，根據網格資料選擇材質，以建立多材質材質效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Selector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材質選擇器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 5%

---


# 材質選擇器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-selector.resources/material-selector.png){width="128px"}

<b>收錄於：</b> 基於網狀的發電機>公用事業

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

將全彩 ID 映射轉換為二進位黑白遮罩。 允許將不同顏色混合並組合成一個遮罩。

如果你不想用 [多材質混合](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md) ，偏好手動使用遮罩，或者想在其他地方手動使用相同的遮罩，這很方便。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>材料</b> <i>1 - 16</i> | 集合可啟用的材料數量。 |
| <b>啟用資料 #1-16</b> <i>錯誤/真實</i> | 切換顏色混合與組合到最終輸出遮罩中。 你可以啟用任意多種顏色組合。 |
| <b>資料 #1-16</b> <i>（色彩值）</i> | 用來選色材料的顏色，這些材質會轉成黑白。 |
| <b>色彩選擇器的參數</b> | 修改色彩的混合與黑白轉換。 |
| <b>模糊感</b> <i>0.01 - 1.0</i> | 要與鄰近的顏色融合多少。 |
| <b>填充物</b> <i>0.0 - 1.0</i> | 過渡的銳利度，就像對比。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="material-selector.resources/matselector-ex.png" />
        </td>
    </tr>
</table>
