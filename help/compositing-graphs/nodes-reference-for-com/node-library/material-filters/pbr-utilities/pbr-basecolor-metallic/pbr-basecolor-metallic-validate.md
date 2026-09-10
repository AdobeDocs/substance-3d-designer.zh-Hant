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
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---


# PBR 基色 / 金屬驗證

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-basecolor-metallic-validate.resources/pbr-basecolor-metallic-validate.png){width="128px"}

<b>收錄於：</b> PBR工具>材料過濾器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一個公用節點，產生一個從好到壞的「熱圖」，根據 PBR 標準，該熱圖上的數值正確或錯誤。

它作為 PBR 的學習工具非常有用，因為它能清楚呈現錯誤所在及其出現位置的視覺回饋。

不要把它當作萬能工具，但同時務必清楚知道為什麼你會違反這些工具可能標示的規則。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>驗證模式</b> <i>反照率、金屬、合體</i> | 可以設定只勾選 Albedo、Metal 或兩者合併作為總覽模式。 |
| <b>反照率暗域閾值</b> <i>50 sRGB，30 sRGB</i> | 將較低的反照率限制設為 50 或 30 sRGB。 可以減少或增加對紅色區域的耐受性。 |
| <b>金屬反射範圍</b> <i>70-100%反射，60-100% 反射</i> | 更改金屬範圍以判定為正確。 可以減少或增加對紅色區域的耐受性。 |
| <b>覆蓋地圖</b> <i>錯誤/真實</i> | 快速除錯模式可疊加輸入映射，能更快追蹤問題區域。 |
