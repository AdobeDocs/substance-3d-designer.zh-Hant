---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-range.html"
breadcrumb-title: ''
description: 使用直方圖範圍節點，根據直方圖範圍重新映射材質值，進行色彩校正與調整。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 直方圖範圍
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 5%

---


# 直方圖範圍

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-range.resources/histogram-range-1.png){width="128px"}

<b>收錄於：</b> 篩選>調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

減少和/或移動灰階輸入的範圍。 可以用來重新映射過渡，類似 [對比亮度](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/contrast-luminosity/contrast-luminosity.md)，但控制方式不同，某些情況下可能更合理。\
另請參見 [直方圖掃描](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) ，這是另一種更實用的範圍重映射方法。

[點此觀看Substance Academy關於直方圖範圍的影片。](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=517s)

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>分布範圍</b> <i>0.0 - 1.0</i> | 應該從多少程度降低距離。 這類似於將 Levels 最小和最大滑桿都往內移動。 |
| <b>職位</b> <i>0.0 - 1.0</i> | 偏移以減少射程，設定不同的中點以減少射程。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="histogram-range.resources/histogram-range.gif" />
        </td>
    </tr>
</table>
