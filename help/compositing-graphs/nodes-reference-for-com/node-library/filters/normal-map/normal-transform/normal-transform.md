---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
breadcrumb-title: ''
description: 使用法線轉換節點（Normal Transform）來對法線貼圖套用變換，同時正確保留向量方向。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 法線轉換
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# 法線轉換

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-transform.png){width="128px"}

## 法線轉換

**收錄於：***濾鏡/法線貼圖*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

類似於原子轉換 2D 節點，這允許在不破壞切空間的情況下轉換法線貼圖，而是即時重新計算，導致法線貼圖永遠正確。

## 參數

* **Matrix2x2**： *（變換矩陣）：*\
  旋轉或縮放輸入。
* **偏移**&#x200B;量： *-0.5 - 0.5*\
  移動或翻譯結果。 當有 Transformation 控制時，結果可直接與畫布互動來修改。
* **一般格式**： *DirectX、OpenGL*\
  切換不同的法線貼圖格式（反轉綠色通道）

</td>
</tr>
</table>
