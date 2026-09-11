---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/replace-color-range.html"
breadcrumb-title: ''
description: 使用「替換色彩範圍」節點，將指定範圍內的顏色替換為新顏色以進行色彩校正。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Replace Color Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 替換色彩範圍
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 5%

---


# 替換色彩範圍

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](replace-color-range.resources/replace-color-range.png){width="128px"}

<b>收錄於：</b> 篩選>調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

將來源顏色替換為目標顏色，並加入額外控制項。 例如可以用來重新著色材質 ID 貼圖的部分（烘焙）。

欲了解更進階版本，請參見 [色彩匹配。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-match/color-match.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>來源顏色</b> <i>（色彩值）</i> | 顏色要替換。 |
| <b>目標顏色</b> <i>（色彩值）</i> | 用來替代的顏色。 |
| <b>來源範圍</b> <i>0.0 - 1.0</i> | 選擇的源頭範圍或容忍度。 可以增加，使鄰近的顏色也會有色相偏移。 |
| <b>門檻</b> <i>0.0 - 1.0</i> | 衰減/對比度用於距離。 設定低以只替換源色，調高則替換與源色融合的顏色。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="replace-color-range.resources/replace-color-range-example.png" />
        </td>
    </tr>
</table>
