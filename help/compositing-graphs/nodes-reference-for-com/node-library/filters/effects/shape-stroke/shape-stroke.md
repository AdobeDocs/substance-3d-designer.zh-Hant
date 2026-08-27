---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-stroke.html"
breadcrumb-title: ''
description: 使用 Shape Stroke 節點為形狀添加筆劃輪廓，以建立邊框和邊緣效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Stroke
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形狀泳法
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 4%

---


# 形狀泳法

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-stroke.resources/shape-stroke.png){width="128px"}

![](shape-stroke.resources/shape-stroke-grayscale.png){width="128px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

在黑白遮罩（灰階版本）或帶有 alpha 通道的形狀（彩色版本）周圍加上筆劃或輪廓，這點你可能在其他 2D 影像編輯軟體中很熟悉。 可以視為Edge Detect](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md)的更完整版本[。

非常適合各種影像編輯效果。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>寬度</b> <i>-1.0 - 1.0</i> | 筆劃的寬度效應。 |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 效應的全域不透明度。 |
| <b>（大綱）色彩</b> <i>（色彩值）</i> | 輪廓效果所用的顏色。 |
| <b>面具顏色</b> <i>（色彩值）（僅灰階版本）</i> | 純色用於透明度映射輸出。 |
| <b>輸入是預先乘法的</b> <i>錯誤/真實（僅彩色版本）</i> | 輸入是否應假設為預先乘法。 |
| <b>乘法前輸出</b> <i>錯誤/真實</i> | 輸出是否應該預先乘法。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-stroke.resources/shapestroke-ex.png" />
        </td>
    </tr>
</table>
