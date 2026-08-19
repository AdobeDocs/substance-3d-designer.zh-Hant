---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-sampler.html"
breadcrumb-title: ''
description: 使用 Tile Sampler 節點從輸入貼圖中取樣並排列圖塊，在 Substance 3D Designer 中創造瓦片圖案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Sampler
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 瓷磚樣本
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 0%

---


# 瓷磚樣本

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tile-sampler.png){width="128px"}

## 磁磚取樣器（彩色）

**收錄於：***貼圖產生器**/圖案*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

Tile Sampler 是終極的圖塊圖案生成節點。 它是 Tile Generator[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) 的進化版、更複雜的版本。截至 2017 2.1 版本，Tile Sampler 與 [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) 之間的差異大幅縮小。 主要差異現在只在七個不同的地圖槽位上，可用於駕駛縮放、位置、旋轉、大小、顏色和遮罩。 它們的效果可以分開混合。

Tile Sampler 適合建立人工程序式模式，並可額外控制由外部輸入映射驅動的特定參數。

在開始使用圖塊取樣器之前，務必熟悉 [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) 。 大多數情況下，你會發現 [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) 就足夠了，不需要 Tile Sampler 那麼複雜。

## 參數

### 輸入

* **圖案輸入 1-6**： *灰階輸入 / 色彩輸入*\
  自訂圖案影像，當「圖案」參數設為「影像輸入」時使用。\
  可用輸入的數量由 **模式輸入數** 參數決定。
* **縮放地圖輸入**： *灰階輸入*&#x200B;用來驅動圖塊縮放的灰階貼圖。
* **位移貼圖輸入**： *灰階輸入*&#x200B;用灰階貼圖來驅動瓦片位移。
* **旋轉貼圖輸入**： *灰階輸入*\
  灰階地圖來驅動地磚旋轉。
* **向量地圖輸入**： *色彩輸入*\
  色彩向量映射以驅動非均勻縮放。
* **色彩映射輸入**： *灰階輸入/色彩輸入*&#x200B;映射，用於驅動每格的色調調整。
* **遮罩貼圖輸入**： *灰階輸入*\
  面具槽用來隱藏特定格子。
* **模式分布圖輸入**： *灰階輸入*\
  遮罩槽用於驅動多個自訂圖案輸入。
* **背景輸入**： *灰階輸入/彩色輸入*&#x200B;可選背景圖片。

### 參數

* **X 金額**： *0 - 64*\
  圖案的X字重複次數。
* **Y數量**： *0 - 64*\
  該模式的Y字重複次數。
* **非平方展開**： *假/真*\
  能以非平方比率補償擠壓與拉伸。
* **模式**
  * **圖案**： *圖案輸入、方形、圓盤、拋物面、鐘形、高斯分布、荊棘、金字塔、磚塊、漸變、波浪、半鐘、脊狀鐘、新月、膠囊、錐形*\
    選擇要使用的圖案形狀。
  * **圖案輸入編號**： *1 - 6*&#x200B;可隨機選擇的自訂圖案數量。
  * **模式輸入分布**： *隨機、模式編號、分布圖*&#x200B;設定如何選擇多個模式輸入。 隨機指隨機選出一個，圖案編號則是它們被放入循環序列中。 分布圖使用灰階地圖輸入來驅動擺放。
  * **模式輸入濾波（Engine > v4）：***雙線性 + Mipmap，雙線性，最近*
  * **特定**&#x200B;模式： *0.0 - 1.0*\
    讓你可以改變所選圖案的形狀。 效果取決於所選的模式。
  * **模式特定隨機**： *0.0 - 1.0*&#x200B;隨機化效應取決於所選模式。
  * **旋轉**： *0、90、180、270*&#x200B;階梯旋轉（90度）。
  * **旋轉**&#x200B;隨機： *0.0 - 1.0*&#x200B;隨機自由旋轉，按每格計算。
  * **對稱隨機**： *0.0 - 1.0*&#x200B;根據以下行為設定應隨機翻轉/鏡像的方塊數量。
  * **對稱隨機模式**： *水平 + 垂直，水平，*&#x200B;垂直 決定對稱鏡像行為。
* **規模**
  * **尺寸模式**： *正常、保持比例、絕對、像素*&#x200B;設定圖案大小的一般行為。\
    Normal 讓你可以定義圖案元素的大小。 它會受到 X 和 Y 的數量影響。\
    Keep Ratio 允許你設定受 X 和 Y 數量影響的大小，但兩者之間的 X 和 Y 比例保持不變。\
    絕對值讓你設定一個不會受 X 和 Y 影響的絕對大小。\
    像素可以設定絕對像素大小，不受 X 和 Y 數量影響。 改變解析度會影響元素的大小。
  * **尺寸（絕對/像素）：***0.0 - 1.0*&#x200B;改變圖塊的非均勻比例。具體行為取決於尺寸模式。
  * **隨機大小**： *0.0 - 1.0*&#x200B;隨機化每個格子的比例。
  * **縮放**： *0.0 - 10.0*&#x200B;設定全域格子縮放。
  * **比例隨機**： *0.0 - 1.0*&#x200B;每格隨機化比例
  * **比例地圖乘數**： *0.0 - 1.0*&#x200B;在比例地圖效果中融合。
  * **縮放向量貼圖倍率**： *0.0 - 1.0*&#x200B;將縮放向量貼圖的效果融合，以驅動非均勻縮放。
  * **尺度參數化影響**： *X 與 Y、X、Y*&#x200B;軸式參數化影響的集合。 可以用來讓縮放貼圖只影響元素的 X 或 Y。
* **職位**
  * **位置隨機**： *0.0 - 10.0*&#x200B;隨機化兩個軸上的方塊位置。
  * **偏移**&#x200B;量： *0.0 - 1.0*\
    根據偏移類型移動格子。
  * **偏移類型**： *水平五度、垂直五度、水平全局、垂直全局、垂直全局*。改變偏移的運作方向。
  * **全域偏移**&#x200B;量： *0.0 - 1.0*&#x200B;全域偏移X軸或Y軸所有圖塊。
  * **位移貼圖強度**： *0.0 - 1.0*&#x200B;將位移貼圖強度與偏移量融合。
  * **位移角**： *0.0 - 1.0*&#x200B;設定位移角度。
  * **向量貼圖位移**： *0.0 - 1.0*&#x200B;使用向量貼圖來驅動位移與角度。
* **旋轉**
  * **旋轉**： *0.0 - 1.0*&#x200B;全域旋轉所有格子。
  * **旋轉隨機**： *0.0 - 1.0*&#x200B;每格隨機旋轉。
  * **旋轉貼圖乘法**： *0.0 - 1.0*&#x200B;旋轉貼圖對每格旋轉的影響融合。
  * **向量地圖乘法**： *0.0 - 1.0*&#x200B;使用向量地圖來驅動每格旋轉。
* **顏色**
  * **遮罩貼圖閾值**： *0.0 - 1.0*&#x200B;遮罩貼圖何時開始隱藏圖塊的閾值。
  * **遮罩映射反轉**： *假/真*&#x200B;反轉遮罩貼圖效果。
  * **遮罩映射取樣技術**：*圖案中心，圖案邊界框（較慢）*隱藏應該由單一點決定還是由邊界框決定。 避免了零散像素造成的奇怪效果。
  * **遮罩隨機**： *0.0 - 1.0*&#x200B;隨機遮罩，與遮罩貼圖平行運作。
  * **反演遮罩**： *假/真 反*&#x200B;轉隨機遮罩。
  * **混合模式**：*加/字幕、最大（圖塊取樣器）/*&#x200B;加/加、字幕、Alpha 混合* （圖塊取樣器顏色）*混合模式，將圖塊與背景及彼此混合。
  * **顏色**：*（灰階值）/（色彩值）*實心的全域瓦片顏色。
  * **顏色/亮度隨機**： *0.0 - 1.0*&#x200B;顏色隨機化，每格。
  * **色彩參數化模式**： *色彩輸入、縮放、線索引、列索引、圖案索引（磚塊取樣器）*\
    */ *色彩映射、縮放、線索引、列索引、圖案索引、圖案中心位置、圖案中心位置（RG） B球大小（B）（圖塊取樣器顏色）**設定色彩隨機化的精確參數化方式。
  * **色彩參數化乘法**： *0.0 - 1.0*&#x200B;上述參數化效果中的混合效果。
  * **色彩參數化影響（僅限顏色）：**&#x200B;**RGB+Alpha，僅RGB，僅** Alpha 設定參數化如何影響顏色。
  * **全域不透明度（僅限灰階）：***0.0 - 1.0*&#x200B;設定全域磚塊不透明度。
  * **背景色**：*（灰階值）/（色彩值）*設定純色背景色。
  * **反向渲染順序**： *False/True*&#x200B;反向從後到前的繪製順序。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/tilesampler-ex2.png" width="256px"/></div> |
| --- |
|  |

*範例說明參數如何由輸入映射（圖案分布、比例、旋轉）驅動。*

</td>
</tr>
</table>
