---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# 法線轉換

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-transform.resources/normal-transform-01.png){width="128px"}

<b>收錄於：</b> 法線貼圖>濾波器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

類似於原子轉換 2D 節點，這允許在不破壞切空間的情況下轉換法線貼圖，而是即時重新計算，導致法線貼圖永遠正確。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>矩陣2x2</b> <i>（轉換矩陣）：</i> | 旋轉或縮放輸入。 |
| <b>偏移</b> <i>-0.5 - 0.5</i> | 移動或翻譯結果。 當有 Transformation 控制時，結果可直接與畫布互動來修改。 |
| <b>一般格式</b> <i>DirectX、OpenGL</i> | 切換不同的法線貼圖格式（反轉綠色通道） |
