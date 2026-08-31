---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/threshold.html"
breadcrumb-title: ''
description: 使用 Threshold 節點，根據建立遮罩的閾值，將灰階材質轉換成黑白。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Threshold
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 臨界值
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 5%

---


# 臨界值

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](threshold.resources/threshold-01.png){width="200px"}

<b>收錄於：</b> 篩選>調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

若&#x200B;**&#x200B;輸入像素值相對於&#x200B;**閾值**&#x200B;的比較標準符合模式&#x200B;**參數設定，**&#x200B;則回傳白色。\
類似 [直方圖掃描](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)，但對比度始終維持在最大。 這是一種更精確且快速的方式，能獲得與直方圖掃描相似的結果。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>門檻</b> <i>0.0 - 1.0</i> | 亮度值，用以比較輸入像素值。 |
| <b>模式</b> | 輸入像素值與閾值比較&#x200B;**的標準為：<br><br>- *較大*<br> - *更大或相等*<br>- *較低*<br> - *較低或**相等* |
