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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 7%

---


# 隨機牌

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tile-random.resources/tile-random.png){width="128px"}

<b>收錄於：</b> 《產生器>模式》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

Tile Random 產生一種程序化的圖塊圖案，其瓦片形狀比其對應的 [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) 更混亂。 它透過隨機將某些格子分割成較小的格子來達成這個目標。 我們建議你先熟悉方塊產生器，再考慮方塊隨機，因為許多概念相似。

當目標是較舊且較不有條理的圖案時，會用 [拼塊隨機取代拼塊產生器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) 。 不過它也有限制，所以如果有其他進階需求，也可以考慮 [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) 。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>圖案輸入</b> <i>灰階輸入（彩色輸入）</i> | 自訂圖案影像，當「圖案」參數設為「影像輸入」時使用。 |
| <b>背景輸入</b> <i>灰階輸入（彩色輸入）</i> |  |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>X 金額</b> <i>1 - 64</i> | 圖案的X字重複次數。 |
| <b>Y 金額</b> <i>1 - 64</i> | 該模式的Y字重複次數。 |
| <b>非平方展開</b> <i>錯誤/真實</i> | 能以非平方比率補償擠壓與拉伸。 |
| <b>模式</b> |  |
| <b>模式</b> <i>圖案輸入、方形、圓盤、拋物面、鐘形、高斯分布、荊棘、金字塔、磚塊、漸變、波形、半鐘形、有脊形的鐘形、新月形、膠囊、錐形</i> | 選擇要使用的圖案形狀。 |
| <b>影像輸入過濾（引擎 > v4）</b> <i>雙線性 + 多元映射、雙線性、最近</i> |  |
| <b>圖案專屬</b> <i>0.0 - 1.0</i> | 讓你可以改變所選圖案的形狀。 效果取決於所選的模式。 |
| <b>模式特定隨機</b> <i>0.0 - 1.0</i> | 隨機化效應取決於所選模式。 |
| <b>旋轉</b> <i>0、90、180、270，隨機水平，隨機垂直</i> | 將旋轉設定為90度階梯，並可選擇隨機化。 |
| <b>旋轉隨機</b> <i>0.0 - 1.0</i> | 增加隨機自由旋轉。 |
| <b>對稱隨機</b> <i>0.0 - 1.0</i> | 隨機鏡像某些圖案，透過所選的對稱隨機模式。 這個數值越高，鏡像的模式就越多。 |
| <b>對稱隨機模式</b> <i>水平 + 垂直，水平，垂直</i> | 當對稱隨機值高於0時，判斷鏡像行為。 |
| <b>分割</b> |  |
| <b>模式</b> <i>無、自動、自動水平、自動垂直、隨機 H+V</i> | 它會訂定如何分割地塊的規則。 |
| <b>門檻</b> <i>0.0 - 1.0</i> | 分磚的時間限制尺寸。 |
| <b>乘數</b> <i>0 - 10</i> | 分裂倍數。 這個數值越高，分裂越多。 |
| <b>規模</b> |  |
| <b>隨機X</b> <i>0.0 - 1.0</i> | 隨機化 X 軸上的非均勻縮放。 |
| <b>隨機 Y</b> <i>0.0 - 1.0</i> | 隨機化非均勻縮放的 Y 軸。 |
| <b>間隙</b> |  |
| <b>模式</b> <i>相對於最小的磚， 相對於最大的磚</i> | 它會設定磚塊間隙的大小相對於什麼。 |
| <b>金額</b> <i>0.0 - 1.0</i> | 設定磚塊間距大小。 |
| <b>形狀</b> |  |
| <b>規模</b> <i>0.0 - 1.0</i> | 全域可放大每一格。 |
| <b>量表隨機</b> <i>0.0 - 1.0</i> | 每格隨機調整比例。 |
| <b>旋轉</b> <i>0.0 - 1.0</i> | 每塊地磚都要全域旋轉。 |
| <b>旋轉隨機</b> <i>0.0 - 1.0</i> | 會隨機每格旋轉。 |
| <b>旋轉約束</b> <i>錯誤/真實</i> | 限制比例，讓旋轉的方塊不會重疊。 |
| <b>職位</b> |  |
| <b>偏移</b> <i>0.0 - 1.0</i> | 全域移動或平移瓦片，僅在 X 軸上滑動 |
| <b>偏移隨機</b> <i>0.0 - 1.0</i> | 隨機化每個格子偏移，只在 X 軸上滑動 |
| <b>隨機</b> <i>0.0 - 1.0</i> | 隨機定位，方塊在 X 軸和 Y 軸上移動。 |
| <b>隨機約束</b> <i>錯誤/真實</i> | 限制縮放，讓瓦片接觸但不重疊。 大幅減弱隨機位置效應。 |
| <b>顏色</b> |  |
| <b>顏色</b> <i>（灰階值）/（色彩值）</i> | 所有地塊都設定為純色。 |
| <b>顏色隨機</b> <i>0.0 - 1.0</i> | 顏色會根據每格隨機化。 |
| <b>色彩參數化</b> <i>無，面積，大小 x，大小 y</i> | 這樣顏色變化就會依賴於這些設定之一。 |
| <b>色彩參數化強度</b> <i>0.0 - 1.0</i> | 上述參數化效應的乘數。 |
| <b>色彩參數化效果（僅限色彩）</b> <i>RGB+Alpha，僅RGB，僅Alpha</i> | 決定僅色彩參數化的效果。 |
| <b>背景色</b> <i>（灰階值）/（色彩值）</i> | 設定純色背景色。 |
| <b>混合模式</b> <i>加/加/加，Alpha 混合（彩色）</i> | 將圖塊混合模式設為背景。 |
| <b>面具</b> |  |
| <b>隨機</b> <i>0.0 - 1.0</i> | 隨機開始遮蔽地磚。 分值越高，消失的地塊越多。 |
| <b>倒轉</b> <i>錯誤/真實</i> | 反轉遮罩結果。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="tile-random.resources/tile-random-1.png" />
        </td>
    </tr>
</table>
