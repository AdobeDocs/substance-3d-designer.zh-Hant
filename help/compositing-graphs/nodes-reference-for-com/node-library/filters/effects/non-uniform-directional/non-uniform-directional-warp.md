---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/non-uniform-directional-warp.html"
breadcrumb-title: ''
description: 使用非均勻方向扭曲節點來套用非均勻方向扭曲，創造多樣化的失真效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Non Uniform Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 非均勻方向曲速
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 4%

---


# 非均勻方向曲速

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](non-uniform-directional-warp.resources/non-uniform-directional-warp-color.png)![](non-uniform-directional-warp.resources/non-uniform-directional-warp-grayscale.png)

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

非均勻方向扭曲是方向扭曲[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md)的進階版本，允許透過影像輸入來驅動扭曲的強度與方向。它能提供更多控制，並能產生非常有用且有趣的影像變形，類似 [於斜坡模糊](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md)。

它與 [多向扭曲](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/multi-directional-warp/multi-directional-warp.md) 不同，因為它允許透過自訂地圖輸入控制角度，而多方向扭曲則只能透過參數控制方向。 這表示你可以創造進階的拖曳和彎曲效果，這是其他方法無法做到的。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入</b> <i>灰階輸入</i> | 將套用扭曲的基礎地圖。 |
| <b>強度輸入</b> <i>灰階輸入</i> | 強制性的遮罩貼圖必須是灰階，能控制扭曲效果的強度。 |
| <b>曲速角度輸入</b> <i>灰階輸入</i> | 強制性的遮罩貼圖必須是灰階，因為它驅動扭曲效果的角度。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>強度</b> <i>0.0 - 20.0</i> | 設定扭曲效果的強度，也就是像素要被推出多少。 |
| <b>曲速角</b> <i>0.0 - 1.0</i> | 設定 Warp 效果的角度或方向。 |
| <b>曲速角輸入倍數</b> <i>0.0 - 1.0</i> | 設定扭曲角度輸入貼圖的效果。 曲速角輸入映射將用於從 0 插值到該參數的值。 |
| <b>越野模式</b> <i>最小值、最大值、平均值</i> | 設定軌跡的融合方式。 |
| <b>步道長度</b> <i>0.0 - 1.0</i> | 設定步道長度。 |
| <b>步道消失</b> <i>0.0 - 1.0</i> | 設定每條痕跡應該淡出的程度 |
| <b>步道曲線</b> <i>-1.0 - 1.0</i> | 只有在 Trail Fade i 時才有效，但不是 0。 設定漸入效應的行為方式。 |
