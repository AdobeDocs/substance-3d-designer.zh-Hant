---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-vector-rotation.html"
breadcrumb-title: ''
description: 使用法線向量旋轉節點來旋轉法線貼圖向量，以調整表面光照和細節方向。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Vector Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 法向量旋轉
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 4%

---


# 法向量旋轉

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-vector-rotation.resources/normal-vector-rotation.png){width="128px"}

<b>收錄於：</b> 法線貼圖>濾波器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一個法線工具節點，能旋轉輸入法線貼圖的所有向量，位於切線空間中。 它其實不是在轉換像素，而是改變像素所代表的數值。 它也可以利用可選的貼圖，為灰階面增加隨機旋轉。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>正常</b> <i>色彩輸入</i> | 用來進行旋轉的基底地圖。 必要資訊。 |
| <b>旋轉映射（可選）</b> <i>灰階輸入</i> | 可以調節旋轉強度的灰階地圖。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>旋轉角</b> <i>0.0 - 1.0</i> | 設定旋轉法線貼圖的角度 |
| <b>一般格式</b> <i>DirectX、OpenGL</i> | 切換不同的法線貼圖格式（反轉綠色通道） |
