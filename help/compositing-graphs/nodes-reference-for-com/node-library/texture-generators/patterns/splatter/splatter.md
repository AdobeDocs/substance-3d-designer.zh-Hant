---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter.html"
breadcrumb-title: ''
description: 使用濺射節點將形狀散布到貼圖中，創造隨機圖案和有機貼圖細節。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 濺射
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---


# 濺射

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/splatter.png)

![](../../../../../../assets/splatter-color.png)

## 濺射（彩色）

**收錄於：***貼圖產生器**/圖案*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

Splatter 是一種設計用於隨機放置地圖輸入的圖案產生器。 它有許多幾何圖案放置的控制，使用比圖塊產生器[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)更簡單。後者也能達到類似的效果，但複雜得多。

Splatter 很適合快速壓印某些形狀，不需要太多調整。

請記住，預設的 Splatter 參數看起來一點也不隨機：你需要調整其中幾個參數才能達到隨機化（主要是 Disorder 參數）。 另外要記得，Splatter 需要地圖輸入才能運作。

## 參數

* **圖樣尺寸寬度**： *0.0 - 1000.0* X 軸上可使用的圖樣數量。
* **圖案尺寸高度**： *0.0 - 1000.0* Y軸可使用圖案數量。
* **旋轉**： *-360.0 - 360.0*&#x200B;旋轉每個圖案固定數量。
* **旋轉變化**： *0.0 - 360.0*&#x200B;引入對每個獨立形狀的隨機旋轉。
* **縮放**： *100.0 - 10000.0*&#x200B;放大最終結果。 請記得這會破壞磁磚！
* **增益**： *0.0 - 10.0*&#x200B;調整每個圖案的混合增益。 這樣會讓他們更突出。
* **Pan X**： *-100.0 - 100.0* Pan 整個 X 軸結果。
* **Y全景**： *-100.0 - 100.0*&#x200B;全景在Y軸上。
* **無障礙**： *0.0 - 100.0*\
  會隨機變換形狀。
* **網格編號**： *0 - 8*&#x200B;跳過不同格子大小以調整結果比例。 能維持磁磚。
* **無序角**： *0.0 - 360.0*&#x200B;控制無序移動角度。
* **無序隨機**： *假/真*&#x200B;隨機化無序角度，增加了更多混亂。
* **圖案尺寸**： *5 - 12*
* **尺寸變化**： *0.0 - 100.0*&#x200B;為每個形狀引入隨機縮放。
* **影像輸入過濾（僅引擎 > v4）**： *雙線性 + 多重映射、雙線性、最近*&#x200B;哪個濾波套用到輸入影像。
* **輸出電平最小**&#x200B;值： *0.0 - 1.0*&#x200B;出最低電平調整。
* **輸出電平最大**&#x200B;值： *0.0 - 1.0*&#x200B;輸出最大電平調整。
* **背景色**：*（灰階值）*設定為純色背景色。
* **亮度變化**：*0.0 - 1.0（僅限灰階版本）*引入亮度變化。
* **色彩變化**：*0.0 - 1.0（僅限彩色版本）*引入色彩變化。

## 範例圖片

![](../../../../../../assets/splatter-ex.gif)

</td>
</tr>
</table>
