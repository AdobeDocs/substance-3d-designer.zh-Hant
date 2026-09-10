---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-angle-to-normal.html"
breadcrumb-title: ''
description: 使用多角度到法線節點，從多角度掃描影像產生法線貼圖，以獲得精確的表面細節。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi-Angle to Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多角度到正常
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 3%

---


# 多角度到正常

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-angle-to-normal.resources/multi-angle-to-normal.png){width="128px"}

<b>收錄於：</b> 《材料濾>掃描處理》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

此節點會根據一組在不同光照條件下拍攝的照片/掃描影像，構建一個法線貼圖。 這比從單一反照率影像中提取法線圖時，能更精確地轉換法線貼圖。

它比 [多角度到反照](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md)率更複雜，因為你需要使用設定且精確的光線角度來操作輸入。 每個取樣的光照角度應該均勻分布，且取樣需要依序輸入。 所以三個取樣時，光線角度應該取在：0、120、240，或任何均勻的偏移量（例如 90、210、330）。

>[!NOTE]
>
> 關於此節點的反照率版本，請參見 [多角度到反照](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) 率。 如果你想預先處理輸入 [，Multi Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md)、 [Multi Crop](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md) 和 [Multi Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md) 都很有用，因為它們是設計來與這些節點結合的。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入 1-8</b> <i>色彩輸入</i> |  |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>一般格式</b> <i>DirectX、OpenGL</i> | 切換不同的法線貼圖格式（反轉綠色通道）。 |
| <b>樣本數量</b> <i>2 - 8</i> | 設定要處理的樣本（輸入）數量。 |
| <b>強度</b> <i>0.0 - 1.0</i> | 設定法線貼圖強度。 |
| <b>第一採樣光角度</b> <i>0.0 - 360.0</i> | 設定第一個輸入的光照角度方向。 |
| <b>下一個取樣光線角度</b> <i>逆時針，順時針</i> | 設定下一個取樣中光源的移動方向。 |
