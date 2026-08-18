---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/warp.html"
breadcrumb-title: ''
description: 使用 Warp 節點對貼圖套用失真效果，以創造變形和位移效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 曲速
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---


# 曲速

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子節點：扭曲](../../../../assets/comp_warp_1.png "原子節點：扭曲"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

根據從獨立梯度輸入計算的斜率，將輸入影像中的像素值位移，導致變形。

與方向扭曲不同，此節點均勻地從白色區域推開，方向由梯度輸入的斜率或梯度定義。

</td>
</tr>
</table>

節點操作起來有點棘手，因為效果的結果非常依賴漸層輸入：對漸層做些微調整，在相同的強度值下，視覺上會有很大差異。 記得多調整漸層輸入的對比度、亮度和縮放，還有這個節點上的強度滑桿。

如果你熟悉法線貼圖，可以想像這個節點的運作類似於將漸層輸入轉換成[法線貼圖](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)，然後將基礎輸入扭曲成法線貼圖向量定義的方向。 事實上，這同樣的效果也可以用[向量曲速](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md)實現。 類似的效果也出現在[《斜坡模糊](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md)》中。

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
| <b>強度</b> *浮標* | 設定扭曲強度。 |
| <b>輸入過濾模式</b> *布林值* | 控制輸入取樣時使用最近濾波還是雙線性濾波。 |

## 輸入連接器

|  |  |
| --- | --- |
| <b>輸入</b> *灰階/彩色* 原色 | 彩色或灰階影像。 |
| <b>梯度輸入</b> *灰階* | 灰階輸入影像的漸變斜率決定了輸出影像中的扭曲效應。 |

## 輸出連接器

|  |  |
| --- | --- |
| <b>產出</b> *灰階/彩色* |  |

## 範例

*即將推出。*
