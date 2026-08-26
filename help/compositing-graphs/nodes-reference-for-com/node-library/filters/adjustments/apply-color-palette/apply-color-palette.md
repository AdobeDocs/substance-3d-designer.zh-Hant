---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/apply-color-palette.html"
breadcrumb-title: ''
description: 使用 Apply Color Palette 節點，透過色彩調色盤重新映射材質，以產生風格化的色彩效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Apply Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 套用色彩調色盤
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---


# 套用色彩調色盤

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![量化色彩圖示量化色彩圖示](../../../../../../assets/ApplyColorPalette.png ""){width="200px"}

<b>收錄於：</b> 篩選>調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

使用識別映射將有序調色盤中的顏色套用到影像上。

顏色的分配是透過將 ID 映射中的索引與調色盤中顏色的索引匹配來分配的。

例如，調色盤中的顏色 #2 會套用到所有 ID 映射中 ID 值為 2 的像素。

此節點可與以下節點結合使用： [量化顏色](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md)、 [建立色彩調色盤](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md)、 [修改色彩調色盤](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md)、 [檢視色彩調色盤](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md)。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### 輸出連接器

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## 輸入連接器

|  |  |
| --- | --- |
| <b>身分證</b> *灰階* 初級 | 輸入 ID 映射用於分配輸入調色盤中的顏色。   ID 映射是一種影像，其中屬於整體（例如形狀）的像素都擁有相同的唯一識別值。 此時，值為整數。   ID 映射可透過 [量化色彩](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md) 節點產生。 |
| <b>調色盤</b> *顏色* | 一個以像素列編碼的有序 RGB 顏色清單。 調色盤最多可容納256種顏色。 這是節點映射到 ID 映射索引的調色盤。   調色盤可用量化色彩節點產生[，並以修改色彩調色盤](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md)節點進行修改[。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md) |

## 輸出連接器

|  |  |
| --- | --- |
| <b>產出</b> *顏色* | 這是將調色盤中的顏色映射到 ID 映射的索引所產生的結果。 |

## 範例

![套用色彩調色盤：範例 1](../../../../../../assets/apply_color_palette_example_2.png "套用色彩調色盤：範例 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/apply_color_palette_example_1_before.jpg" alt="apply_color_palette_example_1_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/apply_color_palette_example_1_after.jpg" alt="apply_color_palette_example_1_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>

![套用色彩調色盤：範例 3](../../../../../../assets/apply_color_palette_example_4.png "套用色彩調色盤：範例 3"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/apply_color_palette_example_3_before.jpg" alt="apply_color_palette_example_3_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/apply_color_palette_example_3_after.jpg" alt="apply_color_palette_example_3_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>
