---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/value-processor.html"
breadcrumb-title: ''
description: 使用值處理器節點（Value Processor）來處理並操作貼圖值，並透過數學運算進行自訂調整。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Value processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 價值處理器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---


# 價值處理器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子節點：價值處理器](value-processor.resources/value-processor-01.png "原子節點：價值處理器"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

計算一個 [物質函數圖](../../../../function-graphs/the-function-graph/the-function-graph.md) 並輸出結果。

它與像素處理器](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)相當[，但不同之處在於它不會為每個像素計算函數，而是計算單一值，並將其呈現[在物質圖](../../../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md)中。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> 這個節點是學習 [Substance 函數圖](../../../../function-graphs/the-function-graph/the-function-graph.md)的好起點。
> 
> 另外要考慮，使用這類圖並執行數學運算是從這個節點取得任何東西的必要條件。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 輸出連接器

</td>
<td style="border: 0;" valign="top">

### 範例

</td>
</tr>
</table>

## 參數

|  |  |
| --- | --- |
| <b>價值處理器函數</b> *任何可用的值類型* | [評估物質函數圖](../../../../function-graphs/the-function-graph/the-function-graph.md) 以計算輸出值。 |

## 輸入連接器

|  |  |
| --- | --- |
| <b>輸入影像#</b> *灰階/彩色* | 使用 [樣本色彩](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) 或 [樣本灰階](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) 節點來存取指定索引輸入中的數值。 |

## 輸出連接器

|  |  |
| --- | --- |
| <b>產出</b> *任何可用的值類型* |  |

## 範例

*即將推出。*
