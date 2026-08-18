---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/luminance-highpass.html"
breadcrumb-title: ''
description: 使用亮度高通節點從貼圖中提取高頻亮度細節，以增強表面細節。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Luminance Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 亮度高通
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 1%

---


# 亮度高通

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/luminance-highpass.png){width="128px"}

## 亮度高通

**收錄於：***濾鏡/調整*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

透過對輸入的亮度值進行 [高通，](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)抵消照明資訊。 對於修正帶有光照資訊的拍攝紋理非常有用。 可在 Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) 中透過多次通過組合[，以移除不同頻率的光照細節。

它在保留色彩 [方面比 Lighting Cancel Low Frequencys 稍微好一點。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md)

## 參數

* **半徑**： *0.0 - 64.0*&#x200B;高通效果半徑。 較小的半徑會抵消較小的光線，並調整以匹配輸入影像。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/luminance-highpass-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
