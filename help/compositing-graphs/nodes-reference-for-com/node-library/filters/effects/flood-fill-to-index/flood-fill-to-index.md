---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-index.html"
breadcrumb-title: ''
description: 使用 Flood Fill to Index 節點，將區域填充索引值，以建立編號和標籤圖案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Index
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 洪水填埋至索引
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 2%

---


# 洪水填埋至索引

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-index.resources/flood-fill-to-index-01.png){width="200px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

洪水填充到索引會將每個洪水填充儲存格依其索引號轉換成值，索引號從左上角的 0 開始。 它可以用來回傳灰階色調，呈現正規化形式（0.0到1.0，除以洪泛填充所找到的格數），或作為HDR未固定值（0到n，n為格數）。

此外，Flood Fill to Index 會利用 [值](../../../../../values-compositing-graphs/values-in-substance-compositing-graphs.md)，回傳發現的形狀數量及可選的內部資料表。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>洪水填充 Bbox</b> <i>色彩輸入</i> | 標準洪水填入地圖。 必要資訊。 |
| <b>特殊形狀資訊</b> <i>色彩輸入</i> | 額外的洪水填滿地圖，必須在之前的淹水填滿節點明確啟用，且必須連接！ |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>產出</b> <i>正規化，整數</i> | 判斷輸出是 LDR 0-1 範圍還是 HDR 0-n 範圍。 |
| <b>忽略小於</b> <i>0.0 - 1.0</i> | 忽略小形狀的容忍值。 |
| <b>顯示洪水填補資料表</b> <i>錯誤/真實</i> | 回傳額外的（除錯）資料以供進階使用。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-index.resources/flood-fill-to-index-02.jpg" />
        </td>
    </tr>
</table>
