---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/ao-cancellation.html"
breadcrumb-title: ''
description: 使用 AO 消除節點移除掃描材質的環境遮蔽，讓貼圖處理乾淨。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > AO Cancellation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: AO 取消
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 4%

---


# AO 取消

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/ao-cancel.png){width="128px"}

<b>收錄於：</b> 《材料濾>掃描處理》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這個節點會根據獨立的 AO 地圖輸入，嘗試從你的反照率（基底色）地圖中移除任何環境光影光照資訊。 它可以用來確保你的反照率資訊是正確的，且大部分沒有（強烈的）光照資訊。

這是一個很有用的節點，當你有從掃描網格烘焙的 AO 貼圖，或者甚至是從高度或法線資訊產生的 AO 貼圖時。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>AO 取消</b> <i>0.0 - 1.0</i> | 移除光照資訊的強度。 |
| <b>AO 飽和度</b> <i>0.0 - 1.0</i> | （De）光線被移除區域的飽和補償。 這可以用來恢復較暗區域的顏色流失。 |
