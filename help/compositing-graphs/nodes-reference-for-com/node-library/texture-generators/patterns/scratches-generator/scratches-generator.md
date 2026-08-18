---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/scratches-generator.html"
breadcrumb-title: ''
description: 使用刮痕產生器節點來製作程序性刮痕圖案，以增加材料的磨損和損壞。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Scratches Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 刮痕產生器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---


# 刮痕產生器

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/scratches-generator.png)

## 刮痕產生器（普通）

**收錄於：***貼圖產生器**/圖案*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

這會隨機產生刮痕，並提供多種自訂選項，例如設定方向、擴散和變形。

有一個特別版本的刮痕產生器，叫做刮痕產生法線，會根據刮痕的深度產生法線貼圖。 大多數選項都一樣，但有幾個額外參數明確標示為普通設定（見下文）。

## 參數

* **花鍵編號**： *1 - 512*&#x200B;需放置的刮痕（花鍵）數量。
* **每個花鍵**&#x200B;最大段數： *2 - 256*&#x200B;刮痕長度內的段數/細分數量。 這會讓曲線和變形變得更平滑。 失真值越高，效果越明顯。
* **樣條旋轉**： *0.0 - 1.0*&#x200B;所有樣條線均勻旋轉，以使其朝向特定方向。
* **樣條旋轉**&#x200B;隨機： *0.0 - 1.0*&#x200B;角度變化，隨機旋轉每個樣條。
* **樣條尺度**： *0.0 - 1.0*&#x200B;均勻縮放所有樣條尺度。
* **花鍵刻度隨機**： *0.0 - 1.0*&#x200B;隨機逐個花鍵縮放。
* **樣條失真**： *0.0 - 1.0*&#x200B;所有樣條鍵的變形水平均勻。
* **樣條變形隨機**： *0.0 - 1.0*&#x200B;個別隨機化每個樣條的變形程度。
* **樣條失真頻率**： *0.0 - 1.0*&#x200B;設定失真頻率，控制失真細節的尺度。
* **花鍵寬度**： *0.0 - 2.0*&#x200B;均勻設定所有花鍵的寬度。
* **花鍵寬度隨機**： *0.0 - 1.0*&#x200B;每個花鍵寬度逐一隨機化。
* **樣條鍵位置隨機**： *0.0 - 1.0*&#x200B;個別隨機化每個樣條的位置。 這個數值越低，越多樣條線會聚集到畫布中心。 可以用來製造刮痕斑點。
* **設定 px** 中的樣條寬度： *False/True（假/真*） 決定用於樣條寬度設定的單位。
* **亮度隨機（僅限灰階版本）：***0.0 - 1.0*&#x200B;可個別隨機化每個樣條的亮度。
* **正常強度（僅限普通版本）：***0.0 - 1.0*&#x200B;設定每個樣條曲線的正常效果強度。
* **&#x200B;正常強度隨機 &#x200B;**（僅限普通版本）**&#x200B;**： *0.0 - 1.0*將每個樣條線的正常強度逐一隨機化。
* **&#x200B;一般格式 &#x200B;**（僅限一般版本）**&#x200B;**： *DirectX、OpenGL*\
  切換不同的法線貼圖格式（反轉綠色通道）。
* **淡出模式**： *無，開始、結束、開始 + 結束*&#x200B;設定樣條是否以及以何方向淡出。
* **淡出長度**： *0.0 - 1.0*&#x200B;設定淡出效果的長度（如上述啟用）。
* **非平方展開**： *假/真*\
  能以非平方比率補償擠壓與拉伸。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/scratches-ex1.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/scratches-ex2.png" width="256px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
