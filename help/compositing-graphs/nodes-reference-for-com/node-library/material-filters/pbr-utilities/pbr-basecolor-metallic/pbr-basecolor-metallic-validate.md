---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic-validate.html"
breadcrumb-title: ''
description: 使用 PBR BaseColor Metallic Validate 節點來驗證並校正 PBR 材料的基色與金屬值。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR BaseColor  Metallic Validate
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR BaseColor 金屬驗證
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# PBR 基色 / 金屬驗證

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-basecolor-metallic-validate.png){width="128px"}

## PBR 基色 / 金屬驗證

**收錄於：***材料過濾器/PBR工具*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

一個公用節點，產生一個從好到壞的「熱圖」，根據 PBR 標準，該熱圖上的數值正確或錯誤。

它作為 PBR 的學習工具非常有用，因為它能清楚呈現錯誤所在及其出現位置的視覺回饋。

不要把它當作萬能工具，但同時務必清楚知道為什麼你會違反這些工具可能標示的規則。

## 參數

* **驗證模式**： *反照率、金屬組、合併*&#x200B;組，無論只勾選反照率、金屬組，或兩者合併作為總覽模式。
* **反照率暗範圍閾值**： *50 sRGB，30 sRGB*&#x200B;將較低的反照率限制設為 50 或 30 sRGB。 可以減少或增加對紅色區域的耐受性。
* **金屬反射範圍**： *70-100%反射率，60-100%反射*&#x200B;變化，金屬範圍視為正確。 可以減少或增加對紅色區域的耐受性。
* **疊加映射**： *False/True*&#x200B;快速除錯模式，疊加輸入映射，能更快追蹤問題區域。

## 範例圖片

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
