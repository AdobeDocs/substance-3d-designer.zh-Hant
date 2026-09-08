---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter-to-mask.html"
breadcrumb-title: ''
description: 使用形狀濺射到遮罩節點，將形狀濺射圖案轉換成遮罩，用於材質混合和特效。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter to Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形狀濺射到面罩
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 4%

---


# 形狀濺射到面罩

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/shape-splatter-to-mask.png){width="128px"}

<b>收錄於：</b> 紋理產生器>圖案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

將 [形狀濺射](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md) 資料轉換為基於圖案 ID 的黑白遮罩。 例如，可以讓你只建立某種類型 attern 的遮罩。 它有額外選項，可以選擇一系列圖案 ID，並隨機隱藏部分形狀。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>圖案識別碼起始範圍</b> <i>1 - 8</i> | 先將圖案 ID 設在選擇範圍內。 |
| <b>圖案識別碼 結束範圍</b> <i>1 - 8</i> | 將最後一個圖案 ID 設在選擇範圍內。 |
| <b>隨機面具</b> <i>0.0 - 1.0</i> | 設定隨機遮蔽模式的比例。 |
| <b>產出</b> <i>二元遮罩、整數遮罩、灰階值</i> | 決定輸出值的類型。 二元遮罩只回傳黑白，0或1的值，整數遮罩會編碼高達8的HDR格式圖案，灰階值則會將範圍比例分布在0到1之間。 |
