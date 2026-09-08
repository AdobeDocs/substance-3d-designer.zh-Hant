---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-crop.html"
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
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 4%

---


# 多重作物

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/crop-multi.png){width="128px"}

![](../../../../../../assets/crop-multi-grayscale.png){width="128px"}

<b>收錄於：</b> 《材料濾>掃描處理》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這是多頻道版本的 Crop。 它會從影像中裁切一個區域，主要用於多角度照片，然後 [再結合多角度轉反照](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) 率或 [多角度轉法線](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)。

>[!NOTE]
>
> 更多資訊請參閱原版 [裁剪](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) 。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>輸入計數</b> <i>1 - 8</i> | 設定需平行處理的輸入數量。 |
| <b>輸入大小</b> <i>0 - 8192</i> | 輸入影像的解析度與比例。 對於非方形影像非常重要。 |
| <b>背景</b> <i>（色彩值）/（灰階色值）</i> | 未被裁剪覆蓋區域的背景均勻值。 |
| <b>轉換</b> <i>（變換矩陣）</i> | 旋轉並縮放結果。 結果可透過直接與畫布互動來調整。 |
| <b>偏移</b> <i>0.0 - 1.0</i> | 移動或翻譯結果。 結果可透過直接與畫布互動來調整。 |
| <b>這是正常的（僅限彩色版本）</b> <i>錯誤/真實</i> | 是否應該將輸入視為法線貼圖。 |
