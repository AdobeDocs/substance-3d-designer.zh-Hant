---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height.html"
breadcrumb-title: ''
description: 使用法線到高度節點將法線貼圖轉換成高度貼圖，以提取表面深度資訊。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal to Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 法線至高度
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 3%

---


# 法線至高度

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-to-height.resources/normal-to-height.png){width="128px"}

<b>收錄於：</b> 法線貼圖>濾波器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一個反向轉換節點，嘗試將切線空間法線貼圖轉換回高度圖。 這是稍微簡化的版本; [法線高度的總部](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height-hq/normal-to-height-hq.md) 有更多選項。

這對於只有法線貼圖來源，但又想將它與高度貼圖結合執行操作時非常有用。 請記住，這永遠無法提供百分之百正確的結果，因為當高度轉換成一般時，資訊會因過程而遺失。 如果你調整設定，這個非 HQ 版本在轉換簡單細節方面做得還不錯。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>救濟平衡</b> <i>0.0 - 1.0</i> | 調整不同頻率對最終結果的影響程度。 這很大程度上取決於輸入地圖，需要相當多的調整。 |
| <b>一般格式</b> <i>DirectX、OpenGL</i> | 切換不同的法線貼圖格式（反轉綠色通道）。 |
| <b>全域不透明度</b> <i>0.0 - 1.0</i> | 調整效應的全域不透明度。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-to-height.resources/normal2heightex.png" />
        </td>
    </tr>
</table>
