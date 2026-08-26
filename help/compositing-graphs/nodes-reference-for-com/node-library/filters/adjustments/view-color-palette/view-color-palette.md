---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/view-color-palette.html"
breadcrumb-title: ''
description: 使用「檢視色彩調色盤」節點來視覺化從材質擷取的色彩調色盤資料以供分析。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > View Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 查看色彩調色盤
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---


# 查看色彩調色盤

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![量化色彩圖示量化色彩圖示](../../../../../../assets/ViewColorPalette.png ""){width="200px"}

<b>收錄於：</b> 篩選>調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

將色彩調色盤打包成方形或矩形，方便在圖形檢視或 2D 檢視中視覺化。\
打包的目標是盡量減少空位。

</td>
</tr>
</table>

調色盤中的顏色順序保持不變，顏色從左到右、從上到下流動，類似文字包裝。

此節點可用來視覺化以下節點所產生的調色盤： [量化顏色](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md)、 [建立色彩調色盤](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md)、 [修改色彩調色盤](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md)。

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
| <b>調色盤</b> *色彩 原色* | 一個以像素列編碼的有序 RGB 顏色清單。 調色盤最多可容納256種顏色。   這是節點打包並渲染的調色盤。 |
| <b>調色盤色彩量</b> *整數* | 調色盤中儲存的顏色數量。   如果這個數字與「調色盤」影像輸入中的實際顏色數量不符，視覺化可能不完整，或有比絕對必要的空白欄位還多。 |

## 輸出連接器

|  |  |
| --- | --- |
| <b>產出</b> *顏色* | 是對濃密調色盤的視覺化。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![檢視色彩調色盤：範例1](../../../../../../assets/view_color_palette_example_1.png "查看色彩調色盤：範例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![查看色彩調色盤：範例2](../../../../../../assets/view_color_palette_example_2.png "查看色彩調色盤：範例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![檢視色彩調色盤：範例 3](../../../../../../assets/view_color_palette_example_3.png "查看色彩調色盤：範例 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![查看色彩調色盤：範例 4](../../../../../../assets/view_color_palette_example_4.png "查看色彩調色盤：範例 4"){zoomable="yes"}

</td>
</tr>
</table>
