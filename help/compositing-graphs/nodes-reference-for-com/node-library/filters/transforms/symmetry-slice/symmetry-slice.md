---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry-slice.html"
breadcrumb-title: ''
description: 使用 Symmetry Slice 節點沿著對稱軸切片貼圖，創造鏡像圖案和效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry Slice
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 對稱切片
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 6%

---


# 對稱切片

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](symmetry-slice.resources/mirror-2.png){width="128px"}

<b>收錄於：</b> 《濾波器>轉換》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

複雜對稱/鏡像操作節點。 允許進行多種幾何運算並完全控制，但需要一些實驗。

與 [鏡像](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md) 與 [對稱](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/symmetry/symmetry.md)相比，這個節點有更多選擇。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>對稱模式</b> <i>0 - 6</i> | 選擇對稱幾何/鏡像線。 選項有水平、垂直、對角左右、對角左右、垂直倒轉、角落和斜角。 |
| <b>傳輸模式</b> <i>0 - 6</i> | 混合模式。 選項包括： |
| <b>混合</b> <i>0.0 - 1.0</i> | 將原始影像混合回結果中。 |
| <b>反面</b> <i>錯誤/真實</i> | 翻轉原點，意即操作的原點方向反轉。 例如，從左到右的對稱會變成從右到左。 |
| <b>反面2</b> <i>錯誤/真實</i> | 僅在對稱模式為5或6時使用。 翻轉角落的起點。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="symmetry-slice.resources/symslice.png" />
        </td>
    </tr>
</table>
