---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/transforms-material/material-transform.html"
breadcrumb-title: ''
description: 使用 Material Transform 節點對材質輸出套用轉換，包括旋轉、縮放和偏移。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Transforms (Material) > Material Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材料轉換
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 1%

---


# 材料轉換

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-transforms.png){width="128px"}

## 材料轉換

**收錄於：***材質濾波器/轉換*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

材料轉換就是原子轉換二維節點](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)的[「多通道」材質版本。它能同時轉換輸入材質的所有通道，介面與 Transform 2D 相同。

只要確保頻道設定正確就好！ 預設情況下，金屬/粗糙度和高光/光澤都開啟了，這可能會造成一些混淆。

## 參數

* **轉換**： *（轉換矩陣）*\
  旋轉並縮放結果。 移動/平移是透過 Offset 參數來完成的
* **偏移**&#x200B;量： *-0.5 - 0.5*\
  移動或翻譯結果。 當有變換控制時，可直接與畫布互動來修改結果。
* **一般格式**\
  請選擇 DirectX 或 OpenGL 格式（綠色翻轉）。
* **頻道**\
  在這個群組中切換材質通道，例如使用鏡面/光澤貼圖而非金屬/粗糙度時。

## 範例圖片

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
