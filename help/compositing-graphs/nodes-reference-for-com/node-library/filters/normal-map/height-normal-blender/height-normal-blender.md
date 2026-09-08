---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-normal-blender.html"
breadcrumb-title: ''
description: 使用高度法線混合器節點來混合高度與法線貼圖，以結合表面細節資訊。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height Normal Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 高度標準攪拌機
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# 高度標準攪拌機

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/height-normal-blender.png){width="128px"}

<b>收錄於：</b> 法線貼圖>濾波器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一個將灰階高度圖混合到法線貼圖上的捷徑節點。 高度輸入會內部轉換成法線貼圖，然後正確地與法線輸入混合。

這比手動用分開節點來快速混合細節，但你可能會覺得某些需求缺乏控制和細膩度。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>高度</b> <i>灰階輸入</i> | 用來混合的灰階高度圖。 |
| <b>正常</b> <i>色彩輸入</i> | 用來混合的基礎法線貼圖。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>正常強度</b> <i>0.0 - 16.0</i> | 高度輸入的正常換算強度。 |
| <b>一般格式</b> <i>DirectX、OpenGL</i> | 切換不同的法線貼圖格式（反轉綠色通道）。 |
