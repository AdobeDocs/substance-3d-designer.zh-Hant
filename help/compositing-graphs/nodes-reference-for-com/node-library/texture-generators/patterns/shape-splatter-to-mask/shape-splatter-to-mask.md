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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---


# 形狀濺射到面罩

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-splatter-to-mask.png){width="128px"}

## 形狀濺射到面罩

**收錄於：***貼圖產生器**/圖案*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

將 [形狀濺射](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md) 資料轉換為基於圖案 ID 的黑白遮罩。 例如，可以讓你只建立某種類型 attern 的遮罩。 它有額外選項，可以選擇一系列圖案 ID，並隨機隱藏部分形狀。

## 參數

### 參數

* **圖案 ID 起始範圍**： *1 - 8*&#x200B;將第一個圖案 ID 設在選擇範圍內。
* **圖案 ID 結束範圍**： *1 - 8*&#x200B;將最後一個圖案 ID 設在選擇範圍內。
* **隨機遮罩**： *0.0 - 1.0*&#x200B;設定隨機遮蔽圖案的比例。
* **輸出**： *二元遮罩、整數遮罩、灰階值*&#x200B;決定輸出值的類型。 二元遮罩只回傳黑白，0或1的值，整數遮罩會編碼高達8的HDR格式圖案，灰階值則會將範圍比例分布在0到1之間。

</td>
</tr>
</table>
