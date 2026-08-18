---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-mapper.html"
breadcrumb-title: ''
description: 使用 Flood Fill Mapper 節點，利用泛洪填充演算法來映射相連區域的值，進行貼圖處理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 洪水填埋地圖儀
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 0%

---


# 洪水填埋地圖儀

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-mapper-gray.png)![](../../../../../../assets/floodfill-mapper-color.png)

## 洪水填埋映射器（灰階）

**收錄於：***濾鏡/效果*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

洪水填充映射器允許將現有的圖案或紋理重新映射到洪水填充](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)的[每個單元上。它和其他洪水填充轉換軟體不同，比如 [隨機灰階](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md) 或 [漸層](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md) ，因為它不會產生純色或數值，而是允許你使用自己的輸入貼圖。 它可以被視為洪水填充](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)與[圖塊取樣器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)或[形狀映射器的](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-mapper/shape-mapper.md)結合[，因為它提供了相當多相似的控制與介面。

彩色版本有額外控制項可搭配法線貼圖 [，能補償切線空間 Normap 的旋轉](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-vector-rotation/normal-vector-rotation.md)。

## 參數

### 輸入

* **洪水填充 Bbox**： *顏色輸入標準*&#x200B;洪水填充輸入，必須。
* **圖案輸入 1-8**： *灰階/彩色輸入*\
  自訂圖案影像輸入。
* **圖案分布圖**： *灰階輸入* ID 圖，用以判斷哪個圖案會對應哪個儲存格。 也可以來自其他洪水填水地圖，例如洪水填水到索引。
* **縮放圖**： *用灰階輸入*&#x200B;圖來決定每個格子的縮放。
* **旋轉映射**： *用灰階輸入*&#x200B;映射來決定每個格子的旋轉。
* **亮度偏移映射**： *用灰階輸入*&#x200B;映射設定每個格子的亮度

### 參數

* **平鋪模式**： *無平鋪，H+V*&#x200B;設定是否使用平鋪。 只有當 Size 或 Scale AR 設定低於 1 時才會顯示。
* **模式**
  * **圖案輸入編號**： *1 - 8*&#x200B;設定可使用的自訂圖案輸入數量。
  * **圖案分布模式**： *隨機、形狀大小、分布圖輸入*&#x200B;設定方法以判斷格子中顯示的圖案。
  * **圖案分布抖動**： *0.0 - 1.0*&#x200B;允許圖案分布出現輕微變化或偏移，且不會透過隨機種子改變所有內容。
* **規模**
  * **尺寸模式**： *相對於紋理、相對於形狀 BSphere、相對於最大形狀、相對於最小形狀、擬合形狀 BBox*&#x200B;設定每個格子中圖案大小的決定方式。
  * **尺寸**： *0.0 - 1.0*&#x200B;允許非均勻縮放圖樣。
  * **等級**： *0.0 - 1.0*\
    設定效果的全域（均勻）比例。
  * **比例尺地圖 多重調整**&#x200B;器： *0.0 - 1.0*&#x200B;設定可選比例尺地圖的影響。
  * **隨機**&#x200B;比例： *-1.0 - 1.0*&#x200B;設定圖案尺度內的隨機變化量。
* **旋轉**
  * **旋轉**： *0.0 - 1.0*&#x200B;為每個格子設定全域且均勻的旋轉。
  * **旋轉地圖 多重器**： *0.0 - 1.0*&#x200B;設定可選旋轉地圖的影響。
  * **旋轉隨機**： *0.0 - 1.0*&#x200B;設定每個格子的隨機旋轉量。
  * **旋轉自動縮放**： *假/真*&#x200B;設定，若圖案在旋轉時應該調整縮放以符合格子。
* **職位**
  * **位置偏移**： *0.0 - 1.0*&#x200B;為每個格子設定全域位置偏移。
  * **位置偏移對齊**： *貼圖，模式*&#x200B;設定，將偏移0點對齊到圖案單元或貼圖。
  * **位置偏移**&#x200B;隨機： *0.0 - 1.0*&#x200B;設定每個格子的位置偏移隨機化數量。
* **彩色** （僅限灰階版本）
  * **亮度範圍**： *0.0 - 1.0*&#x200B;設定貼圖的全局對比度，0 變為中間灰色。
  * **亮度範圍隨機**： *0.0 - 1.0*&#x200B;設定亮度範圍的隨機化程度。
  * **亮度偏移**： *-1.0 - 1.0*&#x200B;設定亮度偏移，作為亮度控制。
  * **亮度偏移隨機**： *0.0 - 1.0*&#x200B;設定亮度偏移的隨機化程度。
  * **亮度偏移貼圖 多重映射**： *0.0 - 1.0*&#x200B;設定可選明度偏移貼圖的影響。
  * **背景色**：*（灰階值）*設定背景色到被混合的材質上。
* **彩色** （僅限彩色版本）
  * **法線映射**： *false/true*&#x200B;是將圖案輸入解讀為法線貼圖嗎？ 將補償並修正法線切線空間旋轉。
  * **一般格式**： *DirectX、OpenGL*\
    切換不同的法線貼圖格式（反轉綠色通道）。 只有當 的法線貼圖為真時才會啟動。
  * **HSL 調整**： *-1.0 - 1.0*&#x200B;全球調整 HSL。
  * **HSL 隨機**： *-1.0 - 1.0*&#x200B;設定每個細胞的 HSL 隨機化。
  * **Alpha 調整**： *-1.0 - 1.0*&#x200B;設定全域 Alpha 調整，降低 Alpha 對比度。
  * **Alpha 隨機**： *-1.0 - 1.0*&#x200B;設定每個細胞的 Alpha 調整隨機化。
  * **背景色**：*（色彩值）*設定背景色到紋理被混合的材質上。

.

## 範例圖片

![](../../../../../../assets/floodfill-mapper-ex01.png)

![](../../../../../../assets/floodfill-mapper-ex02.jpg)

</td>
</tr>
</table>
