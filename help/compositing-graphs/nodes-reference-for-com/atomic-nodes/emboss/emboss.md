---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/emboss.html"
breadcrumb-title: ''
description: 使用 Emboss 節點在材質上製作壓紋效果，為表面細節增加深度與層次感。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 壓印
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca8beeed4bcddc6518237761ba87c319a1624018
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 1%

---


# 壓印

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子節點：Emboss](emboss.resources/comp_emboss_1.png "原子節點：Emboss"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

透過依照指定的光源方向，將影像中形狀的側面打亮，施加壓印效果。

也就是說，節點會根據兩個輸入執行簡單的二維著色，模擬光線落在具有高度與深度變化的表面上。

</td>
</tr>
</table>

這個節點在類似 PBR 的專案中不常用，但在你想要簡單烘焙光照的情況下，它確實能用到。 另外， [Emboss With Gloss](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/emboss-with-gloss/emboss-with-gloss.md) 和 [Uber Emboss](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md) 也提供類似但更廣泛的功能。

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
| <b>強度</b> *浮標* | 調整全域照明強度效果。   設定「高度」貼圖的強度，進而影響光影效果的強度 |
| <b>光角</b> *浮標* | 設定光線模擬的角度。   定義浮雕圖像高光的照明角度 |
| <b>高光色</b> *浮動/漂浮4* | 設定面向光線角度的區域顏色。   如果輸入圖片是彩色，則設定高亮的顏色。 |
| <b>陰影顏色</b> *浮動/漂浮4* | 設定面向遠離光線角度的區域顏色。   設定壓印影像陰影區域的顏色。 |

## 輸入連接器

|  |  |
| --- | --- |
| <b>輸入</b> *灰階/彩色* 原色 | 提供底色、無陰影的顏色。 把它當作一種擴散或底色質感。 |
| <b>強度輸入</b> *灰階* | 代表用來計算表面光照的高度圖。 黑色代表低，白色代表高。 |

## 輸出連接器

|  |  |
| --- | --- |
| <b>產出</b> *灰階/彩色* |  |

## 範例

*即將推出。*
