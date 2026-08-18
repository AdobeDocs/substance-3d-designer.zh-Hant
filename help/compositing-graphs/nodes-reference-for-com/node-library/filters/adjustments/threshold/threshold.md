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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---


# 臨界值

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/threshold-2.png){width="200px"}

## 臨界值

**收錄於：***濾鏡/調整*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

若&#x200B;**&#x200B;輸入像素值相對於&#x200B;**閾值**&#x200B;的比較標準符合模式&#x200B;**參數設定，**&#x200B;則回傳白色。\
類似 [直方圖掃描](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)，但對比度始終維持在最大。 這是一種更精確且快速的方式，能獲得與直方圖掃描相似的結果。

### 參數

* **門檻**： *0.0 - 1.0*\
  亮度值，用以比較輸入像素值。
* **模式**：\
  輸入像素值與閾值&#x200B;**比較**&#x200B;的標準：
  * *更偉大*
  * *大或相等*
  * *下層*
  * *較低或相等*

## 範例圖片

</td>
</tr>
</table>
