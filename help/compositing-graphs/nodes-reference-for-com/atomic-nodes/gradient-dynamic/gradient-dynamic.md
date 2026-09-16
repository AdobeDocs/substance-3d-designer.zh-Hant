---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/gradient-dynamic.html"
breadcrumb-title: ""
description: 使用漸變（動態）節點來建立可由輸入參數和數值控制的動態漸層。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Gradient (Dynamic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 漸變（動態）
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%
---

# 漸變（動態）

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![原子節點：梯度動態](gradient-dynamic.resources/comp_dyngradient_1.png "原子節點：梯度動態"){width="100%"}

<b>收錄於：</b> 原子節點

</td>
<td style="border: 0;" valign="top">

利用另一張影像中由一列或一列像素提供的漸層，重新映射影像中的灰階值。

它作為漸層節點的一個小替代方案，但與漸層節點不同的是，漸層色彩鍵並非內部定義，而是來自外部輸入。

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="gradient-dynamic.resources/gradient-dynamic-tooltip.gif" alt="漸變動態工具提示" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

這主要避免了無法暴露參數的問題，因為顏色參數會移到節點外。 這就是讓它變得「動態」的原因。

雖然 Gradient（動態）本身並非難以使用的節點，但其使用情境較為先進：大多數標準用法都可以由一般的 Gradient 節點涵蓋。

當你被漸層編輯器的鍵系統限制太多，且希望顏色和斜坡位置由其他輸入、參數和圖表部分驅動時，這個節點就會派上用場。

另外，也可用漸層輸入位置滑桿在單一 Ramp 輸入中交替切換多個漸層。



## 參數

|  |  |
| --- | --- |
| <b>梯度尋址</b> *布林值* | 如果梯度重複（磚塊）或夾住，則會被設定。   此參數決定灰階輸入中 [0， 1] 範圍外的 HDR 像素如何處理：是夾住還是摺疊至 [0， 1]。 |
| <b>梯度方向</b> *整數* | 設定「梯度輸入」應沿取樣的軸線：<ul data-preserve-html="true"> <li data-preserve-html="true"><i>水平：</i> 取樣一列 X 軸上的像素。</li> <li data-preserve-html="true"><i>垂直：</i> 在 Y 軸取樣一列像素。</li> </ul> |
| <b>梯度輸入位置</b> *浮標* | 在「梯度輸入」中，要取樣的像素列或列的正規化位置。 |

## 輸入連接器

|  |  |
| --- | --- |
| <b>灰階輸入</b> *灰階* 初級 | 灰階影像要重新映射。 |
| <b>梯度輸入</b> *彩色/灰階* | 梯度取樣自此影像 |


## 範例

*即將推出。*
