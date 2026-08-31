---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/directional-blur.html"
breadcrumb-title: ''
description: 使用方向模糊節點，將模糊效果套用特定方向，以產生動態模糊和條紋效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Directional blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 方向模糊
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 1%

---


# 方向模糊

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子節點：方向模糊](directional-blur.resources/directional-blur-01.png "原子節點：方向模糊"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

根據強度圖，在指定方向施加模糊效果。

此節點執行類似動態模糊的操作。 與一般[「模糊](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)」節點不同，後者在所有方向均勻模糊，「方向模糊」則是依照使用者定義的角度運作。

</td>
</tr>
</table>

與「模糊」類似，它也是一種較快且品質較低的操作。 Anisotropic Blur](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md) 提供了[更長且高品質的替代方案，並在性能上有所取捨

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

## 方向性模糊與各向異性模糊

下方這些圖片展示了方向模糊與[各向異性模糊](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md) 在相同輸入形狀下的影響，參數相似。 各向異性模糊設定為全各向異性且高品質。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>方向模糊</b>

![方向模糊比較](directional-blur.resources/directional-blur-02.png "方向模糊比較"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

<b>各向異性模糊</b>

![各向異性模糊比較](directional-blur.resources/directional-blur-03.png "各向異性模糊比較"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 參數

</td>
<td style="border: 0;" valign="top">

### 輸入連接器

</td>
<td style="border: 0;" valign="top">

### 輸出連接器

</td>
<td style="border: 0;" valign="top">

### 範例

</td>
</tr>
</table>

## 參數

|  |  |
| --- | --- |
| <b>強度</b> *浮標* | 設定模糊半徑以像素為單位。 |
| <b>角度</b> *浮標* | 模糊效果的方向是順時針方向，從水平方向開始——即方向向量（1， 0）。 |

## 輸入連接器

|  |  |
| --- | --- |
| <b>輸入</b> *灰階/彩色* [原色](../../../../glossary/glossary.md) | 要處理的影像。 |

## 輸出連接器

|  |  |
| --- | --- |
| <b>產出</b> *灰階/彩色* |  |

## 範例

*即將推出。*
