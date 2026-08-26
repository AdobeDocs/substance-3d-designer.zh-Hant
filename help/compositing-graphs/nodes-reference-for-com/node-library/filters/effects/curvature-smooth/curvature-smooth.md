---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-smooth.html"
breadcrumb-title: ''
description: 使用 Curvature Smooth 節點從高度圖產生平滑曲率貼圖，以提取表面細節。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Smooth
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 曲率平滑
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 1%

---


# 曲率平滑

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![曲率平滑節點圖示曲率平滑節點圖示](../../../../../../assets/CurvatureSmooth.png ""){width="200px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

計算由法線貼圖描述的曲率。

曲率圖代表曲面的凹面與凸面。\
平坦區域為50%為灰色。 凸面較亮，凹面較暗。

</td>
</tr>
</table>

凹面與凸面區域也被獨立輸出，方便根據這些特性選擇或遮蔽區域。

>[!TIP]
>
> 可以考慮 [Curvature](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md) 想要更銳利的版本，如果[需要更多選項，也可以考慮 Curvature Sobel](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md) 。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### 輸出連接器

</td>
<td style="border: 0;" valign="top">

### 參數

</td>
</tr>
</table>

## 輸入連接器

|  |  |
| --- | --- |
| <b>正常</b> *色彩 原色* <b></b> | 描述應計算曲率曲率的法線映射。 |

## 輸出連接器

|  |  |
| --- | --- |
| <b>曲率</b> *灰階* | 曲率映射是從輸入法線映射中計算出來的。   平坦區域為50%為灰色。 凸面較亮，凹面較暗。 |
| <b>凸性</b> *灰階* | 由輸入法向映射計算出凸性映射。   一個區域越凸，地圖上就越亮。  平坦或凹陷的區域為黑色。 |
| <b>凹陷</b> *灰階* | 凹面映射是從輸入法線映射中計算出來的。   區域越凹，地圖上越亮。  平坦或凸起的區域則為黑色。 |

## 參數

|  |  |
| --- | --- |
| <b>標準格式</b> *整數* | 輸入法線貼圖的格式。 這有效地將綠色通道反轉。<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX：</b> Y 軸指向上方</li> <li data-preserve-html="true"><b style="">OpenGL：</b> Y 軸指向下方</li> </ul> |

## 範例

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_1_before.jpg" alt="curvature_smooth_example_1_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_1_after.jpg" alt="curvature_smooth_example_1_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![平滑曲率：範例 2](../../../../../../assets/curvature_smooth_example_2.jpg "平滑曲率：範例 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![曲率平滑：範例 3](../../../../../../assets/curvature_smooth_example_3.jpg "曲率平滑：範例 3"){zoomable="yes"}

</td>
</tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_4_before.jpg" alt="curvature_smooth_example_4_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_4_after.jpg" alt="curvature_smooth_example_4_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![平滑曲率：範例4](../../../../../../assets/curvature_smooth_example_5.jpg "平滑曲率：範例4"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![平滑曲率：範例 5](../../../../../../assets/curvature_smooth_example_6.jpg "平滑曲率：範例 5"){zoomable="yes"}

</td>
</tr>
</table>
