---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/distance.html"
breadcrumb-title: ''
description: 使用距離節點計算形狀的距離貼圖，用於製作遮罩和程序化效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Distance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 距離
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 1%

---


# 距離

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子節點：距離](distance.resources/comp_distance_1.png "原子節點：距離"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

找出遮罩中最近白色像素的位置，並從該位置輸出漸層，或是來源影像中該位置的顏色。

此節點會從輸入最大值中任意像素在0.5灰階值範圍內產生向外線性漸變（漸層）。

</td>
</tr>
</table>

向外擴展的衰落會在遇到另一個單元時終止：它們永遠不會重疊。 內部操作實際上是計算並顯示到最近像素 >0.5 的距離，距離節點設為夾位/最大值。

可選的來源映射允許將細胞與次級輸入映射的貼圖結合。

距離節點不是一個容易掌握的節點，但它的主要用途包括以可靠的方式擴展現有遮罩（相較於模糊和調整對比度）、產生 Voronoi 類型的噪聲單元，以及以銳利且線性的輪廓斜角現有形狀（這些輪廓可以之後重新映射）。

更多資訊請參考以下 [範例](#examples) 。

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
| <b>彩色模式</b> *布林值* | 在灰階和彩色輸出影像之間切換。 也會改變「來源輸入」的輸入類型。 |
| <b>最大距離</b> *浮標* | 調整遮罩中偵測最近邊界的最大距離（像素數）。 |
| <b>結合來源/距離</b> *布林值* | 判斷可選的「來源輸入」如何與最終單元結合。<ul data-preserve-html="true"> <li data-preserve-html="true"><i>結合：</i> 將「來源輸入」值與漸入微弱的線性遮罩結合。 若「來源輸入」輸入已連接，則其值與計算出的距離結合。</li> <li data-preserve-html="true"><i>僅有來源：</i> 僅從「來源輸入」輸出純色。</li> </ul> |
| <b>距離模式</b> *整數* | 選擇計算擷取遮罩中最近邊界距離的方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><i>歐幾里得：</i> X/Y差的平方總和。</li> <li data-preserve-html="true"><i>曼哈頓：</i> X/Y 差異的絕對值總和。</li> <li data-preserve-html="true"><i>切比雪夫：</i> X/Y 差異的絕對值最大值。</li> </ul>  <div><img alt="距離模式範例" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_copy_copy_copy_row-yj03rtt-column-0i13nfd_image" src="distance.resources/distance-comparison.jpg" title="距離模式範例"/></div> |

## 輸入連接器

|  |  |
| --- | --- |
| <b>遮罩輸入</b> *灰階* 初級 | 灰階遮罩，邊界需計算距離值。   從影像中擷取一個二元遮罩，使用0.5的閾值，該閾值以上為白色，低於此閾值為黑色。 |
| <b>來源輸入</b> *彩色/灰階* | 可選的灰階影像，從中複製「遮罩輸入」最近邊界的像素值。 |

## 輸出連接器

|  |  |
| --- | --- |
| <b>產出</b> *彩色/灰階* |  |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](distance.resources/distance-ex01.gif){width="250px"}

</td>
<td style="border: 0;" valign="top">

![](distance.resources/distance-ex02.gif){width="250px"}

</td>
<td style="border: 0;" valign="top">

![](distance.resources/distance-ex03.gif){width="250px"}

</td>
</tr>
</table>
