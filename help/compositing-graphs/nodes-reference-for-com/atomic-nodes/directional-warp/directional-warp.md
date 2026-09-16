---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/directional-warp.html"
breadcrumb-title: ""
description: 使用方向扭曲節點對貼圖施加方向扭曲，以創造流動與動態效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Directional warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 方向曲速
user-guide-description: ""
user-guide-title: ""
source-git-commit: b2c99a199364ff62b5790b72bcfef02a35d58ca2
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%
---

# 方向曲速

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子節點：方向扭曲](directional-warp.resources/comp_directionalwarp_1.png "原子節點：方向扭曲"){width="20%"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

根據強度圖，將像素沿指定方向位移，這可能導致變形。

將輸入在使用者設定的方向上扭曲，並乘以使用者設定的強度映射。 它的運作方式類似於扭曲空間，但只在特定方向上。

</td>
</tr>
</table>

<div data-preserve-html="true" style="display: block; margin: auto;"><img src="directional-warp.resources/directional-warp-tooltip.gif" alt="方向曲速工具提示" /></div>

扭曲節點是一個相當簡單但實用的節點，是其他更進階效果的良好基礎。 還有更進階的替代方案，例如其他相關節點如 [斜率模糊（Slope Blur](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md) ）和 [向量扭曲（Vector Warp](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md)）。



## 參數

|  |  |
| --- | --- |
| <b>強度</b> *浮標* | 設定扭曲強度。 |
| <b>曲速角</b> *浮標* | 設定扭曲效果的角度，以轉數表示...... |
| <b>輸入過濾模式</b> *布林值* | 控制輸入取樣<b></b>時使用最近濾波還是雙線性濾波。 |
| <b>強度圖偏移</b> *浮標* | 此值會從 <b>強度輸入</b> 影像值中扣除。 |

## 輸入連接器

|  |  |
| --- | --- |
| <b>輸入</b> *灰階/彩色* 原色 | 應該套用變形效果的灰階或彩色輸入影像。 |
| <b>強度輸入</b> *灰階* | 灰階影像定義了輸入影像應該施加<b></b>多少扭曲。 |


## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![方向扭曲 - 範例1](directional-warp.resources/dir-warp.gif "方向扭曲 - 範例1"){width="20%"}{zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![定向曲速 - 範例2](directional-warp.resources/dir-warp02.gif "方向性曲速 - 範例2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![方向扭曲 - 範例 3](directional-warp.resources/dir-warp03.gif "方向扭曲 - 範例 3"){zoomable="yes"}

</td>
</tr>
</table>
