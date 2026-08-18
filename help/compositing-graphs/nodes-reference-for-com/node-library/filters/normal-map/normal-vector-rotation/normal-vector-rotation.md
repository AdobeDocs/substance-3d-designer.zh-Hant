---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-vector-rotation.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---


# 法向量旋轉

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-vector-rotation.png){width="128px"}

## 法向量旋轉

**收錄於：***濾鏡/法線貼圖*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

一個法線工具節點，能旋轉輸入法線貼圖的所有向量，位於切線空間中。 它其實不是在轉換像素，而是改變像素所代表的數值。 它也可以利用可選的貼圖，為灰階面增加隨機旋轉。

## 輸入

* **一般：***色彩輸入*\
  用來進行旋轉的基底地圖。 必要資訊。
* **旋轉映射（可選）：***灰階輸入*\
  可以調節旋轉強度的灰階地圖。

## 參數

* **旋轉角度**： *0.0 - 1.0*\
  設定旋轉法線貼圖的角度
* **一般格式**： *DirectX、OpenGL*\
  切換不同的法線貼圖格式（反轉綠色通道）

## 範例

</td>
</tr>
</table>
