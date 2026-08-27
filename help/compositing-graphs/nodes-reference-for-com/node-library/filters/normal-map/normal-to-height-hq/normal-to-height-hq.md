---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height-hq.html"
breadcrumb-title: ''
description: 使用「法線高度」節點將法線貼圖轉換成高品質的高度貼圖，以便擷取表面細節。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal To Height HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 標準至高度總部
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 3%

---


# 標準至高度總部

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-to-height-hq.resources/normal-to-height-hq.png){width="128px"}

<b>收錄於：</b> 法線貼圖>濾波器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一個反向轉換節點，嘗試將切線空間法線貼圖轉換回高度圖。 這是較進階的節點; [法線到高度](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height/normal-to-height.md) 的選項較少，且使用不同的計算方式。

這對於只有法線貼圖來源，但又想將它與高度貼圖結合執行操作時非常有用。 請記住，這永遠無法提供百分之百正確的結果，因為當高度轉換成一般時，資訊會因過程而遺失。 它永遠無法取代正確生成的高度圖！

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>一般格式</b> <i>DirectX、OpenGL</i> | 切換不同的法線貼圖格式（反轉綠色通道）。 |
| <b>救濟平衡</b> <i>0.0 - 1.0</i> | 低頻與高頻偏壓的混合。 |
| <b>高度強度</b> <i>0.0 - 1.0</i> | 強度或乘法器用於高度圖，運作方式有點像全域不透明度。 |
| <b>高度正規化</b> <i>錯誤/真實</i> | 它會自動縮放高度圖範圍以達到全對比度，就像 [自動調平](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md)一樣。 |
| <b>品質</b> <i>正常，高</i> | 在速度和品質之間切換。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-to-height-hq.resources/normal2height-hq-ex.png" />
        </td>
    </tr>
</table>
