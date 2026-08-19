---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-crop.html"
breadcrumb-title: ''
description: 使用多重裁剪節點同時裁切多個紋理通道，以更有效率地處理掃描材質。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多重作物
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---


# 多重作物

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/crop-multi.png){width="128px"}

![](../../../../../../assets/crop-multi-grayscale.png){width="128px"}

## 多重裁切（灰階）

**收錄於：***材料濾鏡/掃描處理*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

這是多頻道版本的 Crop。 它會從影像中裁切一個區域，主要用於多角度照片，然後 [再結合多角度轉反照](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) 率或 [多角度轉法線](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)。

>[!NOTE]
>
> 更多資訊請參閱原版 [裁剪](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) 。

## 參數

### 參數

* **輸入計數**： *1 - 8*&#x200B;設定需平行處理的輸入數量。
* **輸入大小**： *0 - 8192*&#x200B;輸入影像的解析度與比例。 對於非方形影像非常重要。
* **背景**：*（色彩值）/（灰階值）*未被裁切覆蓋區域的背景均勻值。
* **轉換**： *（轉換矩陣）*\
  旋轉並縮放結果。 結果可透過直接與畫布互動來調整。
* **偏移**&#x200B;量： *0.0 - 1.0*\
  移動或翻譯結果。 結果可透過直接與畫布互動來調整。
* **是否正常（僅限色彩版本）：***錯誤/真實*&#x200B;輸入是否應該被視為法線貼圖。

## 範例圖片

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
