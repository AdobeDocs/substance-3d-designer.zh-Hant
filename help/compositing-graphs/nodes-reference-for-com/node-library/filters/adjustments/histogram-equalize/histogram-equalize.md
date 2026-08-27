---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-equalize.html"
breadcrumb-title: ''
description: 使用直方圖均衡節點重新分配像素強度，提升對比度和亮度。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram equalize
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 直方圖等化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---


# 直方圖等化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![直方圖均衡：圖示](histogram-equalize.resources/histogram_equalize.png "直方圖等化：圖示"){width="200px"}

<b>收錄於：</b> 篩選>調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

它能將灰階影像的直方圖等化，有效地調整灰階值，目標是達到均勻分布。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入</b> <i>灰階</i> 初級 | 直方圖應被均衡化的影像。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>產出</b> <i>灰階</i> | 結果影像已套用直方圖等化。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>直方圖解析度</b> *整數* | 直方圖的寬度。 較高的值能讓更細緻的值分布。   可用解析度以像素為單位：256、512、1024、2048、4096 |
| <b>直方圖平滑</b> *浮標* | 直方圖可透過重新分配影像中的灰階值來平滑，以平衡 *各值間的差異* 。   這個參數會調整平滑的強度。 |

## 範例

<table>
  <tr>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_1_before.jpg" alt="histogram_equalize_example_1_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_1_after.jpg" alt="histogram_equalize_example_1_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>

![直方圖等化：範例 1](histogram-equalize.resources/histogram_equalize_example_3.png "直方圖等化：範例 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_2_before.jpg" alt="histogram_equalize_example_2_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_2_after.jpg" alt="histogram_equalize_example_2_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>

![直方圖等化：範例 2](histogram-equalize.resources/histogram_equalize_example_5.png "直方圖等化：範例 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_4_before.jpg" alt="histogram_equalize_example_4_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_4_after.jpg" alt="histogram_equalize_example_4_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>

![直方圖等化：範例 3](histogram-equalize.resources/histogram_equalize_example_6.png "直方圖等化：範例 3"){zoomable="yes"}
