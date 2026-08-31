---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/hsl.html"
breadcrumb-title: ''
description: 使用 HSL 節點調整材質的色調、飽和度和明度，以進行色彩調整與校正。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > HSL
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: HSL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 1%

---


# HSL

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子節點：HSL](hsl.resources/hsl-01.png "原子節點：HSL"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

調整彩色影像的色調、飽和度與明度。

這是一個基本且易於使用的節點，在處理色彩資料時非常有用。

如果你想找其他編輯影像色調的方法，可以參考 [曲線](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)、 [等級](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) 和 [對比度/亮度](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/contrast-luminosity/contrast-luminosity.md)。

</td>
</tr>
</table>

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
| <b>色相</b> *浮標* | 決定輸入影像的顏色。   低於0.5的數值會讓色相呈負向移動，高於0.5的數值則呈正向移動。 |
| <b>飽和度</b> *浮標* | 決定輸入影像色彩的飽和度。   數值低於 0.5 會降低飽和度，高於 0.5 則會增加飽和度。 |
| <b>輕盈</b> *浮標* | 決定輸入影像的亮度，值低於 0.5 會降低亮度，值超過 0.5 則增加亮度。 |

## 輸入連接器

|  |  |
| --- | --- |
| <b>輸入</b> *色彩 原色* | 影像待處理。 |

## 輸出連接器

|  |  |
| --- | --- |
| <b>產出</b> *顏色* |  |

## 範例

*即將推出。*
