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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 1%

---


# AO 取消

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/ao-cancel.png){width="128px"}

## AO 取消

**收錄於：***材料濾鏡/掃描處理*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

這個節點會根據獨立的 AO 地圖輸入，嘗試從你的反照率（基底色）地圖中移除任何環境光影光照資訊。 它可以用來確保你的反照率資訊是正確的，且大部分沒有（強烈的）光照資訊。

這是一個很有用的節點，當你有從掃描網格烘焙的 AO 貼圖，或者甚至是從高度或法線資訊產生的 AO 貼圖時。

## 參數

* **AO 消除**： *0.0 - 1.0*&#x200B;移除光照資訊的強度。
* **AO 飽和度**： *針對移除光線區域的 0.0 - 1.0*（去）飽和補償。 這可以用來恢復較暗區域的顏色流失。

## 範例圖片

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
