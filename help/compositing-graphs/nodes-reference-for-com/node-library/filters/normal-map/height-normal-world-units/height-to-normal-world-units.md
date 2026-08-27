---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-to-normal-world-units.html"
breadcrumb-title: ''
description: 使用「高度轉法線世界單位」節點，將高度圖轉換為法線圖，並使用世界單位縮放技術，以達到更精確的細節。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height to Normal World Units
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 高度與正常世界單位
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---


# 高度與正常世界單位

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-to-normal-world-units.resources/normal-hq.png){width="128px"}

<b>收錄於：</b> 法線貼圖>濾波器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一個進階的身高轉普通轉換節點，在轉換過程中會使用真實世界的單位。

當你知道來源高度圖的尺寸，並希望進行最精確的轉換時，例如處理掃描資料時，這很有用。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>表面積（公分）</b> <i>0.0 - 1000.0</i> | 輸入高度圖的尺寸。 |
| <b>高度深度（公分）</b> <i>0.0 - 100.0</i> | 高度圖細節的最大深度。 |
| <b>一般格式</b> <i>OpenGL、DirectX</i> | 切換不同的法線貼圖格式（反轉綠色通道）。 |
| <b>抽樣</b> <i>標準，索貝爾</i> | 在兩種取樣模式間切換以判斷準確度。 |
