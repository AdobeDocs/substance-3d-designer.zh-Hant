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
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 1%

---


# 洪水填埋至索引

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-index.png){width="200px"}

## 洪水填埋至索引

**收錄於：***濾鏡/效果*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

洪水填充到索引會將每個洪水填充儲存格依其索引號轉換成值，索引號從左上角的 0 開始。 它可以用來回傳灰階色調，呈現正規化形式（0.0到1.0，除以洪泛填充所找到的格數），或作為HDR未固定值（0到n，n為格數）。

此外，Flood Fill to Index 會利用 [值](../../../../../values-compositing-graphs/values-in-substance-compositing-graphs.md)，回傳發現的形狀數量及可選的內部資料表。

### 輸入

* **洪水填充 Bbox**： *顏色輸入標準*&#x200B;洪水填充輸入映射。 必要資訊。
* **特殊形狀資訊**： *顏色輸入*&#x200B;額外洪水填充地圖，必須在之前的洪水填充節點上明確啟用，且必須連接！

### 參數

* **輸出**： *正規化，整數*&#x200B;判斷輸出是在 LDR 0-1 範圍還是 HDR 0-n 範圍內。
* **忽略形狀 小於**： *0.0 - 1.0*&#x200B;忽略小形狀的容忍值。
* **顯示洪水填充資料表**： *錯誤/真*&#x200B;返回額外（除錯）資料，供進階使用。

## 範例

![](../../../../../../assets/flood-fill-ex02.jpg)

</td>
</tr>
</table>
