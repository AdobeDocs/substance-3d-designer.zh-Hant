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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---


# 多角度到正常

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-angle-to-normal.png){width="128px"}

## 多角度到正常

**收錄於：***材料濾鏡/掃描處理*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

此節點會根據一組在不同光照條件下拍攝的照片/掃描影像，構建一個法線貼圖。 這比從單一反照率影像中提取法線圖時，能更精確地轉換法線貼圖。

它比 [多角度到反照](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md)率更複雜，因為你需要使用設定且精確的光線角度來操作輸入。 每個取樣的光照角度應該均勻分布，且取樣需要依序輸入。 所以三個取樣時，光線角度應該取在：0、120、240，或任何均勻的偏移量（例如 90、210、330）。

>[!NOTE]
>
> 關於此節點的反照率版本，請參見 [多角度到反照](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) 率。 如果你想預先處理輸入 [，Multi Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md)、 [Multi Crop](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md) 和 [Multi Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md) 都很有用，因為它們是設計來與這些節點結合的。

## 參數

### 輸入

* **輸入 1-8**： *色彩輸入*

### 參數

* **一般格式**： *DirectX、OpenGL*\
  切換不同的法線貼圖格式（反轉綠色通道）。
* **樣本數量**： *2 - 8*&#x200B;組需處理的樣本（輸入）數量。
* **強度**： *0.0 - 1.0*&#x200B;設定法線貼圖強度。
* **第一個取樣光角度**： *0.0 - 360.0*&#x200B;設定第一個輸入的光線角度方向。
* **下一個取樣光源角度**： *逆時針，順*&#x200B;時針設定下一個取樣中光源移動的方向。

## 範例圖片

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
