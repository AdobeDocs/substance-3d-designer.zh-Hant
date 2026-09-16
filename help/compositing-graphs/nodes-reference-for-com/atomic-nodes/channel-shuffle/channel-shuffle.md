---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/channel-shuffle.html"
breadcrumb-title: ""
description: 使用 Channels Shuffle 節點在材質中重新排列色彩通道，來創造色彩效果和通道切換。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Channels shuffle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 頻道切換
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0cb0df528e7f0eb6f3c2d51e35302744952718d5
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%
---

# 頻道切換

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子節點：頻道洗牌](channel-shuffle.resources/comp_shuffle.png "原子節點：頻道洗牌")

</td>
<td style="border: 0;" valign="top">

將一或兩個輸入影像的色彩通道重新排列成輸出影像。

也就是說，可以接收兩個輸入，並允許你回傳一個輸出，將紅、綠、藍、阿爾法三個通道互換或設為該輸入的任一通道。

基本上它允許你以任何可能的方式打包和交換 RGB 通道。 灰階輸入被視為顏色：紅色、綠色、藍色和 Alpha 都會回傳相同的數值。

</td>
</tr>
</table>

<div data-preserve-html="true" style="text-align: center;"><img src="channel-shuffle.resources/channels-shuffle-tooltip.gif" alt="頻道洗牌工具提示" /></div>

頻道洗牌有基本選項，但在大多數頻道打包或剝離並設定 Alpha 頻道的情況下，使用 [RGBA 合併](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md)、 [RGBA 分割](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-split/rgba-split.md)、 [Alpha 合併](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-merge/alpha-merge.md) 和 [Alpha 分割](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-split/alpha-split.md)會更快。 它們被設定成執行預設動作，不需要更改多個參數，之後再轉換成灰階。 如果你想要更進階、有更多混合選項的版本，可以看看 [Channel Mixer](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/channel-mixer/channel-mixer.md)。



## 參數

|  |  |
| --- | --- |
| <b>紅水道</b> *整數* | 選擇要插入輸出影像紅色通道的來源通道。 |
| <b>綠通道</b> *整數* | 選擇要插入輸出影像綠色通道的來源通道。 |
| <b>藍色通道</b> *整數* | 選擇要插入輸出影像藍色通道的來源通道。 |
| <b>阿爾法通道</b> *整數* | 選擇要插入輸出影像 Alpha 通道的來源通道。 |

## 輸入連接器

|  |  |
| --- | --- |
| <b>輸入 1</b> *彩色/灰階* PRIMARY | 主要輸入影像。 |
| <b>輸入 2</b> *彩色/灰階* | 次要輸入影像。 |


## 範例

*即將推出。*
