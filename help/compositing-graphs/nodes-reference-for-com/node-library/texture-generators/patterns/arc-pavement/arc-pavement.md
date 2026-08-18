---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/arc-pavement.html"
breadcrumb-title: ''
description: 使用 Arc Pavement 節點生成弧形路面圖案，以創造彎曲的道路與路徑貼圖。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Arc Pavement
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 弧形鋪面
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# 弧形鋪面

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/arcpavement-ex.png)

## 弧形鋪面

**收錄於：***貼圖產生器**/圖案*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

產生巴黎弧形路面圖案。 這種效果無法用標準 [的圖塊產生器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)或 [圖塊取樣](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)器達成，因此有這個專用節點。

## 參數

* **比例**： *1 - 8*&#x200B;全域縮放/平鋪組合。
* **圖案數量**： *1 -* 32\
  每個篇章中會用到多少磚塊。
* **隨機模式數量**： *0.0 - 1.0*\
  每個弧線中磚塊數量隨機。 還有一個額外效果，就是讓磚塊有不同的比例。
* **圖案最低數量**： *1 - 10*\
  控制隨機劇情時的最小磚塊數量。
* **弧數**： *0 - 20*\
  設定垂直堆疊的弧線數量。 改變磚牆高度。
* **圖案**： *輸入影像、方形、圓盤、拋物面、鐘形、高斯圖、荊棘、金字塔、磚塊、漸變、波浪、半鐘形、脊狀鐘形、新月形、膠囊、錐形*\
  選擇要使用的圖案形狀。
* **輸入影像過濾**： *雙線性 + 多重映射、雙線性、最近*
* **圖案比例**： *0.0 - 1.0*&#x200B;每塊地塊的組合縮放。
* **圖案寬度**： *0.0 - 1.0*\
  為每塊地磚設定寬度。
* **圖案高度**： *0.0 - 1.0*\
  為每塊地磚設定高度。
* **圖案寬度隨機**： *0.0 - 1.0*\
  隨機化地磚寬度。
* **圖案高度隨機**： *0.0 - 1.0*\
  隨機化地塊高度。
* **全域圖案寬度隨機**： *0.0 - 1.0*&#x200B;隨機化瓦片寬度，但不會造成較大的空隙。
* **圖案高度降低**： *0.0 - 1.0*&#x200B;控制每個弧線末端格子高度的壓縮。
* **顏色隨機**： *0.0 - 1.0*\
  隨機化方塊顏色。
* **非平方展開**： *假/真*\
  能以非平方比率補償擠壓與拉伸。

## 範例圖片

![](../../../../../../assets/arcpavement-ex.png)

</td>
</tr>
</table>
