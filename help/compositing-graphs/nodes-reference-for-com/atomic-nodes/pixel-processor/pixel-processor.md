---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/pixel-processor.html"
breadcrumb-title: ""
description: 使用 Pixel Processor 節點，透過自訂表達式處理個別像素，進行進階紋理操作。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Pixel processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 像素處理器
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%
---

# 像素處理器

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![原子節點：像素處理器](pixel-processor.resources/comp_pixelprocessor_1.png "原子節點：像素處理器"){width="100%"}

<b>收錄於：</b> 原子節點

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

產生一張影像，每個像素的值是指定 [物質函數圖](../../../../function-graphs/the-function-graph/the-function-graph.md)的結果。

像素處理器允許你對每個輸出回傳的像素執行自訂函式，並以可選輸入方式執行。

它是迄今為止最多功能的節點，因為它允許執行任何數學運算，並在你的圖中回傳結果。

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="pixel-processor.resources/pixel-processor-tooltip.gif" alt="像素處理器工具提示" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>

與 FX-Map[&#128279;](../../../../function-graphs/fxmaps/fxmaps.md) 類似，它需要設定內部功能才能執行任何操作。Pixel 處理器與 FX-Map 的不同之處在於，它不專注於放置圖案，而是有多項功能控制圖案形狀與位置。 取而代之的是，每個像素都以一個函式並行執行，每個像素都不知道鄰近像素的計算結果。

Pixel 處理器類似 [於 Value 處理器](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)，僅使用單一值，且能提供比 Pixel 處理器更好的優化。

對於習慣在節點式編輯器中建立 [著色器](../../../../glossary/glossary.md) 函式的人來說，Pixel 處理器應該能提供熟悉的環境。


>[!TIP]
>
> 本文件的範例物質圖表[&#128279;](../../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md)章節中，有一個帶註解的專案檔案展示了像素處理器節點的簡單使用方法。
> 
> [價值處理器](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)節點是學習 [Substance 函數圖](../../../../function-graphs/the-function-graph/the-function-graph.md)的良好起點。
> 
> 另外要考慮，使用這類圖並執行數學運算是從這個節點取得任何東西的必要條件。
> 
> 我們也建議熟悉 UV、[&#128279;](../../../../glossary/glossary.md) [材質取樣](../../../../glossary/glossary.md)和向量的概念。


## 參數

|  |  |
| --- | --- |
| <b>彩色模式</b> *布林值* | 在灰階和彩色輸出影像之間切換。 |
| <b>每個像素函數</b> *浮動/漂浮4* | [在輸出影像中，每個像素評估的物質函數圖](../../../../function-graphs/the-function-graph/the-function-graph.md) 。   使用[設定為 <b>$pos</b> 變數的 Get Float2](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) 節點，可以存取[目前像素的正規化](../../../../glossary/glossary.md)位置。 |

## 輸入連接器

|  |  |
| --- | --- |
| <b>輸入影像#</b> *灰階/彩色* | 使用 [樣本色彩](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) 或 [樣本灰階](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) 節點來存取指定索引輸入中的數值。 |


## 範例

*即將推出。*
