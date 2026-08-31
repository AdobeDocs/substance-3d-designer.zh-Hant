---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-generator.html"
breadcrumb-title: ''
description: 使用圖塊產生器節點來創建具有可自訂尺寸、偏移和變化控制的程序化圖塊圖案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 圖塊產生器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 5%

---


# 圖塊產生器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tile-generator.resources/tile-generator-01.png){width="128px"}

<b>收錄於：</b> 紋理產生器>圖案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

瓦片產生器是函式庫中最先進的節點之一。 如果你學會精通，就能創造任何模式（當然有一定限制）。 從 2017 版本 2.1 開始，有一些重大更新，讓這個節點更符合 [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) 的功能。

這個節點在各種情境下都非常有用，但要注意，單純讀取參數並不能完全教你如何使用它們。 我們建議你也多做實驗！

在99%的情況下，彩色版本根本不需要！

一些一般使用建議：

* 你可以先從基本形狀開始，但如果你有自訂輸入（將 **圖案類型** 設定為 *影像輸入*），請先建立它！ 它決定了整體的外觀。
* 首先要正確設定你的X和Y數量。
* 找到合適的 **尺寸** 模式：相對模式如 **間隙** 模式的行為與 **絕對** 模式有很大不同。
* 接著調整全域 **縮放** 和非均勻 **大小** 。
* 最後，調整任何 **「變化」** 參數直到符合你的需求。 變化的關鍵在於細膩！

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>模式輸入 1-6</b> <i>灰階輸入</i> | 自訂圖案影像，當「圖案」參數設為「影像輸入」時使用。 |
| <b>背景</b> <i>灰階輸入</i> | 用背景代替純色。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>X 金額</b> <i>1 - 64</i> | 圖案的X字重複次數。 |
| <b>Y 金額</b> <i>1 - 64</i> | 該模式的Y字重複次數。 |
| <b>非平方展開</b> <i>錯誤/真實</i> | 能以非平方比率補償擠壓與拉伸。 |
| <b>模式</b> |  |
| <b>模式</b> <i>影像輸入、方形、圓盤、拋物面、鐘形、高斯分布、荊棘、金字塔、磚塊、漸變、波浪、半鐘形、脊狀鐘、新月形、膠囊、錐形</i> | 選擇要使用的圖案形狀。 |
| <b>模式輸入編號</b> <i>1 - 6</i> | 可以使用的多種不同影像輸入。 僅在上方選擇影像輸入</i>時<i>才可用。 |
| <b>模式輸入分布</b> <i>隨機，按模式編號</i> | 如果選取了多個影像輸入，該如何在不同的影像輸入中選擇。 |
| <b>圖案專屬</b> <i>0.0 - 1.0</i> | 讓你可以改變所選圖案的形狀。 效果取決於所選的圖案。 |
| <b>影像輸入過濾（僅限引擎>v4）</b> <i>雙線性 + 多元映射、雙線性、最近</i> |  |
| <b>旋轉</b> <i>0, 90, 180, 270</i> | 以 90 度步進，全域旋轉所有磁磚，並以固定角度旋轉。 |
| <b>旋轉隨機</b> <i>0.0 - 1.0</i> | 隨機旋轉一格，旋轉四個90度步梯中的一個。 |
| <b>五分翻轉</b> <i>錯誤/真實</i> | 每隔一格旋轉90度。 |
| <b>對稱隨機</b> <i>0.0 - 1.0</i> | 隨機鏡像某些圖案，透過所選的對稱隨機模式。 這個數值越高，鏡像的模式就越多。 |
| <b>對稱隨機模式</b> <i>水平 + 垂直，水平，垂直</i> | 當對稱隨機值高於0時，判斷鏡像行為。 |
| <b>規模</b> |  |
| <b>尺寸模式</b> <i>Normal - 間隙，Normal - 大小、保持比率、絕對值、像素</i> | 設定圖案大小的一般行為。<br><br>正常 - 間隙（Interstice）讓你定義圖案元素之間的間隙。 它會受到 X 和 Y 的數量影響。<br><br>Normal - Size 讓你可以定義圖案元素的大小，不論縫隙大小。 它會受到 X 和 Y 的數量影響。<br><br>Keep Ratio 允許你設定受 X 和 Y 數量影響的大小，但兩者之間的 X 和 Y 比例保持不變。<br><br>絕對值讓你設定一個不會受 X 和 Y 影響的絕對大小。<br><br>像素可以設定絕對像素大小，不受 X 和 Y 數量影響。 改變解析度會影響元素的大小。 |
| <b>中型</b> <i>0.0 - 1.0</i> | 以交替的欄位與列方式調整大小。 |
| <b>間隙 X/Y</b> <i>0.0 - 1.0</i> | 僅在普通-間隙尺寸模式中可用。 改變間隙間隙。 影響形狀之間的接縫，允許不像比例</b>那樣的非均勻控制<b>。 |
| <b>尺寸（絕對/像素）</b> <i>0.0 - 1.0</i> | 僅限於普通-間隙尺寸模式之外。 設定的尺寸不均勻，與 <b>比例</b>不同。 |
| <b>規模</b> <i>0.0 - 2.0</i> | 設定全球規模。 |
| <b>量表隨機</b> <i>0.0 - 1.0</i> | 設定每個瓦片的全域比例變化。 |
| <b>隨機種子比例</b> <i>0 - 1000</i> | 偏移量縮放變異種子。 |
| <b>職位</b> |  |
| <b>偏移</b> <i>0.0 - 1.0</i> | 在每連續的每一列或列上，逐步偏移整個模式（行為取決於垂直偏移參數）。 |
| <b>偏移隨機</b> <i>0.0 - 1.0</i> | 隨機化線條偏移。 |
| <b>偏移隨機種子</b> <i>0 - 1000</i> | 改變隨機偏移效果的相對種子。 |
| <b>垂直偏移</b> <i>錯誤/真實</i> | 設定偏移效應發生在列或線上;水平或垂直。 |
| <b>隨機位置</b> <i>0.0 - 1.0</i> | 以非均勻的方式隨機化位置，X 與 Y 分別控制。 |
| <b>全球抵消</b> <i>0.0 - 1.0</i> | 會將整個結果移到X軸和Y軸上。 |
| <b>旋轉</b> |  |
| <b>旋轉</b> <i>0.0 - 1.0</i> | 對所有圖案磚塊進行均勻自由旋轉。 |
| <b>旋轉隨機</b> <i>0.0 - 1.0</i> | 會隨機生成所有格子的自由旋轉。 這個數值越高，可以旋轉的地塊就越多。 |
| <b>顏色</b> |  |
| <b>顏色</b> <i>（灰階）</i> | 定格為純色。 |
| <b>亮度/顏色隨機</b> <i>0.0 - 1.0</i> | 引入每格顏色或亮度的差異。 |
| <b>按數字計算的亮度</b> <i>錯誤/真實</i> | 整個圖案中亮度會逐漸淡化。 |
| <b>按比例的亮度</b> <i>錯誤/真實</i> | 亮度變化會依地塊比例而異。 |
| <b>棋盤面具</b> <i>錯誤/真實</i> | 每隔一格就藏起來。 |
| <b>水平面具</b> <i>錯誤/真實</i> | 每隔一欄就藏起來了。 |
| <b>垂直面罩</b> <i>錯誤/真實</i> | 每隔一排就藏起來。 |
| <b>隨機面具</b> <i>0.0 - 1.0</i> | 隨機隱藏地磚。 這個數值越高，消失的地塊就越多。 |
| <b>反轉面罩</b> <i>錯誤/真實</i> | 反轉本區塊中任何遮罩效果的結果。 |
| <b>混合模式</b> <i>加、最大、加字幕</i> | 設定要使用的混合模式。 |
| <b>背景色</b> <i>（灰階）</i> | 設定純色背景色。 |
| <b>全域不透明度</b> <i>0.0 - 1.0</i> | 設定全域磚塊的不透明度。 |
| <b>反向渲染順序</b> <i>錯誤/真實</i> | 可以將圖塊從前到後或反過來渲染。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="tile-generator.resources/tile-generator-02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-generator.resources/tile-generator-03.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-generator.resources/tile-generator-04.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-generator.resources/tile-generator-05.png" />
        </td>
    </tr>
</table>
