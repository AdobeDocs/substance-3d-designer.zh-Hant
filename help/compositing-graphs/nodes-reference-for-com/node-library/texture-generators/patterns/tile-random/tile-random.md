---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random.html"
breadcrumb-title: ''
description: 使用圖塊隨機節點來建立帶有程序變化的隨機圖塊圖案，以產生有機的貼圖效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 隨機牌
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---


# 隨機牌

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tile-random.png){width="128px"}

## 方塊隨機（彩色）

**收錄於：***生成器/模式*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

Tile Random 產生一種程序化的圖塊圖案，其瓦片形狀比其對應的 [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) 更混亂。 它透過隨機將某些格子分割成較小的格子來達成這個目標。 我們建議你先熟悉方塊產生器，再考慮方塊隨機，因為許多概念相似。

當目標是較舊且較不有條理的圖案時，會用 [拼塊隨機取代拼塊產生器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) 。 不過它也有限制，所以如果有其他進階需求，也可以考慮 [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) 。

## 參數

### 輸入

* **圖案輸入**： *灰階輸入（彩色輸入）*\
  自訂圖案影像，當「圖案」參數設為「影像輸入」時使用。
* **背景輸入**： *灰階輸入（彩色輸入）*

### 參數

* **X 金額**： *1 - 64*\
  圖案的X字重複次數。
* **Y金額**： *1 - 64*\
  該模式的Y字重複次數。
* **非平方展開**： *假/真*\
  能以非平方比率補償擠壓與拉伸。
* **模式**
  * **圖案**： *圖案輸入、方形、圓盤、拋物面、鐘形、高斯分布、荊棘、金字塔、磚塊、漸變、波浪、半鐘形、脊狀鐘、新月形、膠囊、錐形*\
    選擇要使用的圖案形狀。
  * **影像輸入過濾（引擎 > v4）：***雙線性 + 多元映射，雙線性，最近*
  * **特定**&#x200B;模式： *0.0 - 1.0*\
    讓你可以改變所選圖案的形狀。 效果取決於所選的模式。
  * **模式特定隨機**： *0.0 - 1.0*&#x200B;隨機化效果取決於所選模式。
  * **旋轉**： *0、90、180、270，隨機水平、隨機垂直*，旋轉以90度步進，並可選擇隨機化。
  * **旋轉隨機**： *0.0 - 1.0*&#x200B;增加隨機自由旋轉。
  * **對稱隨機**：  **0.0 - 1.0** 透過所選對稱隨機模式隨機鏡像特定圖案。 這個數值越高，鏡像的模式就越多。
  * **對稱隨機模式**： *水平 + 垂直，水平，垂直*&#x200B;當對稱隨機高於0時，決定鏡像行為。
* **分割**
  * **模式**： *無、自動、自動水平、自動垂直、隨機 h+v*&#x200B;設定分割方塊的規則。
  * **閾值**： *0.0 - 1.0*&#x200B;分割格塊的限制大小。
  * **倍數**： *0 - 10*&#x200B;分割倍數。 這個數值越高，分裂越多。
* **規模**
  * **隨機 X**： *0.0 - 1.0*&#x200B;隨機化 X 軸上的非均勻縮放。
  * **隨機 Y**： *0.0 - 1.0*&#x200B;隨機化 Y 軸上的非均勻縮放。
* **間隙**
  * **模式**： *相對於最小的磚塊，相對於最大磚*，設定磚塊的尺寸相對於的間隙。
  * **金額**： *0.0 - 1.0*&#x200B;設定磚塊間的間隙大小。
* **形狀**
  * **縮放**： *0.0 - 1.0*&#x200B;全域調整每一格。
  * **隨機比例**： *0.0 - 1.0*&#x200B;每格隨機調整。
  * **旋轉**： *0.0 - 1.0*&#x200B;對每個格子進行全域旋轉。
  * **旋轉隨機**： *0.0 - 1.0*&#x200B;隨機旋轉，每格隨機旋轉。
  * **旋轉限制**： *False/True*&#x200B;限制了縮放，使旋轉的瓦片不會重疊。
* **職位**
  * **偏移**&#x200B;量： *0.0 - 1.0*\
    全域移動或平移瓦片，僅在 X 軸上滑動
  * **偏移隨機**： *0.0 - 1.0*&#x200B;隨機偏移每個格塊，僅在 X 軸滑動
  * **隨機**： *0.0 - 1.0*&#x200B;隨機位置，方塊在X軸和Y軸上移動。
  * **隨機限制**： *假/真*&#x200B;限制會縮放，讓瓦片接觸但不會重疊。 大幅減弱隨機位置效應。
* **顏色**
  * **顏色**：*（灰階值）/（色彩值）*為所有磚塊設定純色。
  * **顏色隨機**： *0.0 - 1.0*&#x200B;依每格隨機分配顏色。
  * **色彩參數化**： *無，面積、大小 x、大小 y*&#x200B;使顏色變化依賴於上述設定之一。
  * **色彩參數化強度**： *上述參數化效果的乘數倍數為0.0 - 1.0*。
  * **色彩參數化效果（僅限色彩）：**   **RGB+Alpha，僅RGB，僅** Alpha。決定僅色彩參數化效果。
  * **背景色**：*（灰階值）/（色彩值）*設定純色背景色。
  * **混合模式**： *新增/訂閱、最大值 /*&#x200B;新增/訂閱、Alpha 混合（色彩）**設定將圖塊混合到背景的模式。
* **面具**
  * **隨機**： *0.0 - 1.0*&#x200B;隨機開始遮蔽方塊。 分值越高，消失的地塊越多。
  * **反轉**： *錯誤/真實*\
    反轉遮罩結果。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/tile-random-1.png" width="256px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
