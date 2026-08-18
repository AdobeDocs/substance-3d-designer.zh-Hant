---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-glow.html"
breadcrumb-title: ''
description: 使用 Shape Glow 節點為形狀和材質添加發光效果，創造明亮且具氛圍感的視覺效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形狀光芒
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---


# 形狀光芒

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-glow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-glow.png){width="128px"}

## 形狀光暈（灰階）

**收錄於：***濾鏡/效果*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

在輸入遮罩（灰階版本）或帶有 alpha 通道的形狀（彩色版本）周圍產生柔和的光暈。 與 Glow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/glow/glow.md) 相比[，這種效果更接近其他 2D 影像編輯軟體，因為它是更完整的效果，且控制更多。

## 參數

* **模式**： *柔和、精準*，在兩種精度模式間切換。
* **寬度**： *-1.0 - 1.0*&#x200B;控制光芒的延伸範圍。
* **擴散**： *0.0 - 1.0*&#x200B;模糊效果的截斷/不阻擋，讓光暈在形狀附近看起來很實。
* **不透明度**： *0.0 - 1.0*\
  暈染透明度以產生光暈效果。
* **（陰影）顏色**：*（色彩值）*要加在光暈上的色調。
* **遮罩顏色**：*（色彩值）*（僅限灰階版本）**用於透明映射輸出的純色。
* **輸入是預先乘法**&#x200B;的：*假/真*（僅限彩色版本）**是否應假設輸入為預先乘法。
* **預乘法輸出**： *假/真*&#x200B;輸出是否應預先乘法。

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shapeglow-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
