---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/value-processor.html"
breadcrumb-title: ""
description: 使用值處理器節點（Value Processor）來處理並操作貼圖值，並透過數學運算進行自訂調整。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Value processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 價值處理器
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 1%
---

# 價值處理器

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![原子節點：價值處理器](value-processor.resources/comp_valueprocessor_1.png "原子節點：價值處理器"){width="100%"}

<b>收錄於：</b> 原子節點

</td>
<td style="border: 0;" valign="top">

計算一個 [物質函數圖](../../../../function-graphs/the-function-graph/the-function-graph.md) 並輸出結果。

它與像素處理器[&#128279;](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)相當，但不同之處在於它不會為每個像素計算函數，而是計算單一值，並將其呈現[在物質圖](../../../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md)中。

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="value-processor.resources/value-processor-tooltip.gif" alt="價值處理工具提示" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>


>[!TIP]
>
> 這個節點是學習 [Substance 函數圖](../../../../function-graphs/the-function-graph/the-function-graph.md)的好起點。
> 
> 另外要考慮，使用這類圖並執行數學運算是從這個節點取得任何東西的必要條件。


## 參數

|  |  |
| --- | --- |
| <b>價值處理器函數</b> *任何可用的值類型* | [評估物質函數圖](../../../../function-graphs/the-function-graph/the-function-graph.md) 以計算輸出值。 |

## 輸入連接器

|  |  |
| --- | --- |
| <b>輸入影像#</b> *灰階/彩色* | 使用 [樣本色彩](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) 或 [樣本灰階](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) 節點來存取指定索引輸入中的數值。 |


## 範例

*即將推出。*
