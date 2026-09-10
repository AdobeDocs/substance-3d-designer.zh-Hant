---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-crop.html"
breadcrumb-title: ''
description: 使用材質裁剪節點從掃描的材質中裁剪貼圖區域，以隔離特定感興趣區域。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材料作物
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# 材料作物

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-crop.resources/crop-material.png){width="128px"}

<b>收錄於：</b> 《材料濾>掃描處理》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這個節點是 Crop[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) 的多聲道完整素材版本。它允許你對任何材質通道進行裁切操作並行進行。

>[!NOTE]
>
> [更多資訊請參閱原版](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) [裁剪](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) [。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>頻道</b> | 例如，當使用 Specular/Glossiness 貼圖而非金屬/粗糙度時，可以切換這組材質通道的開關。 |
| <b>輸入大小</b> <i>0 - 8192</i> | 輸入影像的解析度與比例。 對於非方形影像非常重要。 |
| <b>背景</b> <i>（色彩值）/（灰階色值）</i> | 未被裁剪覆蓋區域的背景均勻值。 |
| <b>轉換</b> <i>（變換矩陣）</i> | 旋轉並縮放結果。 結果可透過直接與畫布互動來修改。 |
| <b>偏移</b> <i>0.0 - 1.0</i> | 移動或翻譯結果。 結果可透過直接與畫布互動來修改。 |
