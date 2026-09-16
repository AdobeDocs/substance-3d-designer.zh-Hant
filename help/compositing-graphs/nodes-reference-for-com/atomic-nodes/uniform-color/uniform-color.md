---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/uniform-color.html"
breadcrumb-title: ""
description: 使用 Uniform Color 節點來產生均勻的色彩貼圖，以建立純色填充和底層。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Uniform color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 制服顏色
user-guide-description: ""
user-guide-title: ""
source-git-commit: 961ee151245fbc3266574676bd535c374bd0e3ad
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 1%
---

# 制服顏色

<table>
<tr style="border: 0;">
<td style="border: 0; width: 30%; vertical-align: top">

![原子節點：均勻顏色](uniform-color.resources/comp_uniform_1.png "原子節點：均勻顏色"){width="100%"}

</td>
<td style="border: 0; vertical-align: top">

產生平坦的灰階或色彩值。

這是一個簡單的節點，經常用作加入顏色或建立特定值的起點。

</td>
</tr>
</table>

<div data-preserve-html="true" align="center"><img src="uniform-color.resources/uniform-color-tooltip.gif" alt="統一色彩工具提示" /></div>


>[!TIP]
>
> 效能優化
> 
> 這兩種調整都降低了節點的計算時間與記憶體佔用量：
> 
> * 如果需要灰階值，請確保節點的色彩模式](#parameters)切換[為「灰階」。
> * 由於節點輸出是平面色，你可以使用最低解析度。 將節點的「[輸出大小](../../../../compositing-graphs/output-size/output-size.md)」參數設定為使用「絕對」 [繼承法](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) ，解析度為 16x16 像素。


## 參數

|  |  |
| --- | --- |
| <b>彩色模式</b> *布林值* | 在灰階和彩色輸出影像之間切換。 |
| <b>輸出顏色</b> *浮動/漂浮4* | 選擇用於輸出影像的平面顏色。   使用「Color」色彩模式時，Alpha 通道用於不透明度，0 表示完全透明，1 表示完全不透明。 |


## 範例

*即將推出。*
