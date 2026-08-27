---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-filter-node.html"
breadcrumb-title: ''
description: 利用 Bevel 濾鏡節點在形狀和圖案上製作斜邊，增加深度與立體感。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 斜角（濾波節點）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 4%

---


# 斜角（濾波節點）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](bevel-filter-node.resources/bevel.png){width="128px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

在輸入的灰階高度圖上呈現邊緣斜面效果。 會回傳斜角高度圖和基於該高度圖的法線貼圖。

這是一個有用的節點，用於在理想情況下的二元值（高縮約黑白）基本高度圖上套用精確曲線剖面。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入</b> <i>灰階輸入</i> | 高度圖需要轉換。 |
| <b>自訂曲線</b> <i>灰階輸入</i> | 決定精確曲線/坡度的梯度。 理想狀況是有個漸層線性節點，可以做任何調整，比如 [等級](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) 或 [曲線](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)。 只有當「使用自訂曲線」為真時才會啟動。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>距離</b> <i>-1.0 - 1.0</i> | 斜角效應應該延伸到多遠。 |
| <b>角型</b> <i>圓形、棱角分明</i> | 斜面輪廓應該是圓潤還是直線。 |
| <b>平滑化</b> <i>0.0 - 5.0</i> | 斜角後還要做多少額外的平滑（模糊）處理。 |
| <b>使用非均勻模糊</b> <i>錯誤/真實</i> | 平滑是否應該非均勻進行。 |
| <b>使用自訂曲線</b> <i>錯誤/真實</i> | 切換使用你自訂的高度曲線。 更多資訊請參考上文。 |
| <b>正常強度</b> <i>0.0 - 50.0</i> | 產生的法線貼圖強度。 |
| <b>一般格式</b> <i>DirectX、OpenGL</i> | 切換不同的法線貼圖格式（將綠色通道反轉）。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="bevel-filter-node.resources/bevel-example.png" />
        </td>
    </tr>
</table>
