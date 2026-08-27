---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan.html"
breadcrumb-title: ''
description: 使用直方圖掃描節點來掃描並分析貼圖直方圖，進行色彩校正與調整。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 直方圖掃描
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 4%

---


# 直方圖掃描

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-scan.resources/histogram-scan-1.png){width="128px"}

<b>收錄於：</b> 篩選>調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這是一個非常簡單但實用的節點，提供一種直覺的方式來重新映射輸入灰階影像的對比度和亮度。 可以用來動態地「增大」或「縮減」遮罩。

[點此觀看Substance Academy關於組織圖操作的影片。](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=427s)

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>職位</b> <i>0.0 - 1.0</i> | 類似亮度控制，會移動結果的中點。 當用於漸層輸入時，這個會擴大並縮小過渡點。<br><br>重要提示：預設值為 0 表示最終結果永遠是黑色，試著從 0.5 開始試試看！ |
| <b>對比</b> <i>0.0 - 1.0</i> | 調整結果的對比度。 可以用來設定過渡的硬度。 |
| <b>倒置位置</b> <i>錯誤/真實</i> | 會顛倒最終結果。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="histogram-scan.resources/histogram-scan.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="histogram-scan.resources/histogram-scan2.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="histogram-scan.resources/histogram-scan3.gif" />
        </td>
    </tr>
</table>
