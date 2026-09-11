---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/luminance-highpass.html"
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
source-git-commit: 7f15827b198bfbc133601581dc54ed894e98d89d
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---


# 亮度高通

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](luminance-highpass.resources/luminance-highpass.png){width="128px"}

<b>收錄於：</b> 篩選>調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

透過對輸入的亮度值進行 [高通，](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)抵消照明資訊。 對於修正帶有光照資訊的拍攝紋理非常有用。 可在 Substance 3D Designer[&#128279;](https://www.adobe.com/tw/products/substance3d-designer.html) 中透過多次通過組合，以移除不同頻率的光照細節。

它在保留色彩 [方面比 Lighting Cancel Low Frequencys 稍微好一點。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>半徑</b> <i>0.0 - 64.0</i> | 高通效應的半徑。 較小的半徑會抵消較小的光線，並調整以匹配輸入影像。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="luminance-highpass.resources/luminance-highpass-example.png" />
        </td>
    </tr>
</table>
