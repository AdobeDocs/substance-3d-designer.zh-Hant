---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/fx-map.html"
breadcrumb-title: ""
description: 使用 FX-Map 節點將函數圖套用到材質上，以建立程序式圖案與效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > FX-Map
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 效果圖
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%
---

# 效果圖

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![原子節點：FX-Map](fx-map.resources/fxmap.png "原子節點：FX-Map"){width="100%"}

<b>收錄於：</b> 原子節點

</td>
<td style="border: 0;" valign="top">

FX-Map 可以反覆複製並細分影像或圖案的輸入，並透過參數與邏輯函數控制每個圖案的分布。

它是最強大的原子節點之一，也是應用程式中最複雜的節點。

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="fx-map.resources/fxmap-tooltip.gif" alt="FX-Map 提示" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

類似 [於 Pixel 處理器](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)，你必須定義並建立決定該節點行為與輸出的函式。


>[!TIP]
>
> 請參考 [專門的指南](../../../../function-graphs/fxmaps/fxmaps.md) ，進一步了解 FX-Map 的流程。

>[!IMPORTANT]
>
> 建議在嘗試使用 FX-Map 節點前，對軟體的各個面向非常熟悉，並且能順利建立 [參數的數學函數](../../../../function-graphs/function-graphs.md) 。


請記住，與其他節點不同，FX-Map 的大部分行為並非由參數決定，而是 [透過編輯其內的 FX-Map 函式](../../../../function-graphs/fxmaps/fxmaps.md) 。

|  |  |
| --- | --- |
| <b>彩色模式</b> *布林值* | 在灰階和彩色輸出影像之間切換。 色彩會比灰階慢很多。 |
| <b>背景</b> *浮動/漂浮4* | 設定背景起始色，合成結果。 |
| <b>渲染區域</b> *Float4* | 讓你設定FX-Map兩側的起始像素範圍，產生拉伸效果。 |
| <b>鋪磚區域</b> *Float4* | 這樣可以讓你偏移 FX-Map 的平鋪距離。 |
| <b>Cull 外面</b> *布林值* | 透過剔除](../../../../glossary/glossary.md)超出正常範圍的模式進行優化[。 |
| <b>粗糙度</b> *浮標* | 功能為深度與不透明度的倍增器。 它對效果貼圖混合過程施加偏壓。 |
| <b>全域不透明度</b> *浮標* | 設定FX-map輸出的全域不透明度。 |

## FX-Map 指南

*即將推出。*

## 輸入連接器

|  |  |
| --- | --- |
| <b>背景</b> *灰階/彩色* 原色 | 輸出影像的背景色。 |
| <b>輸入影像#</b> *灰階/彩色* |  |


## 範例

![](fx-map.resources/image2015-9-10-17-28-32.png)
