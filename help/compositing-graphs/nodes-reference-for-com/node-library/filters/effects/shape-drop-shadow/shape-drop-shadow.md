---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-drop-shadow.html"
breadcrumb-title: ''
description: 使用 Shape Drop Shadow 節點為形狀添加投影效果，以創造材質的深度與立體感。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Drop Shadow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形狀滴影
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 6%

---


# 形狀滴影

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-drop-shadow.resources/shape-dropshadow-grayscale.png){width="128px"}

![](shape-drop-shadow.resources/shape-dropshadow.png){width="128px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

在輸入黑白遮罩（灰階版本）或帶透明影像（彩色版本）上，執行其他 2D 影像處理軟體中著名的「投影陰影」效果。

它與 [陰影](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shadows-filter-node/shadows-filter-node.md) 效果不同，因為它回傳的是全透明的影像，使得更完整的效果，類似於其他軟體的預期。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>角度</b> <i>0.0 - 1.0</i> | （假）光的入射角。 |
| <b>距離</b> <i>-0.5 - 0.5</i> | 陰影下降的距離會遠離形狀。 |
| <b>規模</b> <i>0.0 - 1.0</i> | 控制陰影模糊/模糊。 |
| <b>擴散</b> <i>0.0 - 1.0</i> | 用遮擋/斷裂來達到模糊效果，會讓陰影擴散得更遠。 |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 為了陰影效果而混合不透明度。 |
| <b>（影子）顏色</b> <i>（色彩值）</i> | 要在陰影上上色澤。 |
| <b>面具顏色</b> <i>（色彩值）（僅灰階版本）</i> | 純色用於透明度映射輸出。 |
| <b>輸入是預先乘法的</b> <i>錯誤/真實（僅彩色版本）</i> | 輸入是否應假設為預先乘法。 |
| <b>乘法前輸出</b> <i>錯誤/真實</i> | 輸出是否應該預先乘法。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-drop-shadow.resources/dropshadowex.png" />
        </td>
    </tr>
</table>
