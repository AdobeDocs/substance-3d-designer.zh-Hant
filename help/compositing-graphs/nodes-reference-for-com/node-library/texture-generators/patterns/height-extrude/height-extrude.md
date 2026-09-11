---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/height-extrude.html"
breadcrumb-title: ''
description: 使用 Height Extrude 節點根據高度貼圖擠出形狀，創造類似 3D 的深度貼圖效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Height Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 高度突出
user-guide-description: ''
user-guide-title: ''
source-git-commit: 827e738d5db4d64bf366d332a62a7bbd2fa840fc
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 3%

---


# 高度突出

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-extrude.resources/height-extrude.png){width="200px"}

<b>收錄於：</b> 紋理產生器>圖案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

Height Extrude 是從輸入的高度貼圖渲染 3D Z-深度。 就像 [Shape Extrude](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) 和 [Cube 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md) 一樣，它讓你能在 2D 視角中旋轉攝影機。 它的主要目標是作為一個生成器，從平面高度圖中產生 3D 旋轉形狀。 這些形狀接著可以用來搭配 [形狀濺射](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md)。

與 [Shape Extrude](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) 的主要差異在於輸入貼圖不必是二進位「alpha」類型的貼圖，而是全範圍灰階貼圖。 這代表你可以更好地控制擠出高度（有機、複雜形狀），但無法控制斜面剖面（硬表面、簡單形狀）。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>攝影機角度</b> | 相機的歐拉角度，半圈。 請注意，水平旋轉和縮放是直接套用在輸入端。 |
| <b>相機比例</b> <i>0.001 - 3.0</i> | 整體尺度應用於產出。 |
| <b>身高比例</b> <i>0.0 - 2.0</i> | 對輸入高度值套用全局因子。 |
| <b>垂直偏移</b> <i>-1.0 - 1.0</i> | 將最終輸出的結果往上或往下移動。 |
| <b>場地</b> <i>開關</i> | 如果接地關閉，輸入為0而非類似接地平面時，會顯示黑色背景。 |
| <b>一般格式</b> <i>DirectX/OpenGL</i> | <b>法線格式</b>參數會反轉法線貼圖的 y 座標。 |
| <b>正常強度</b> <i>0.0 - 256.0</i> | 和 <b>Normal</b> 節點的<b>強度</b>參數一樣。設定為 256，這樣在旋轉時就能獲得無 Shar 的普通狀態。 |
