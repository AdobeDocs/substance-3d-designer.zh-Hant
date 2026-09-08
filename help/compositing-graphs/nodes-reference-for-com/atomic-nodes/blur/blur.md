---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blur.html"
breadcrumb-title: ''
description: 用模糊節點對貼圖套用模糊效果，讓細節更平滑並創造柔焦效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 模糊
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca8beeed4bcddc6518237761ba87c319a1624018
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 2%

---


# 模糊

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![模糊節點圖示](blur.resources/blur-9.png){width="200px"}

**收錄於：** 原子節點

**很簡單**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 說明

模糊節點執行「框模糊」操作：將像素值在設定距離內取平均，造成模糊且不銳利的畫面。 它提供了 Substance 3D Designer[&#128279;](https://www.adobe.com/products/substance3d-designer.html) 中最簡單、最快且最基本的模糊操作。

雖然模糊適合快速且簡單的操作，例如稍微柔化邊緣，但在更嚴苛的情境 [下，Blur HQ](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/blur-hq/blur-hq.md) 是更好的選擇，兩者在效能和品質之間取得平衡。

</td>
</tr>
</table>

## 參數

* **強度**：0-無限\
  設定模糊的強度或距離。 這個數字沒有上限，但在高值時，整張影像會變成平均色彩。

以下範例顯示該節點左側的模糊值，右側 [則是模糊總部](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/blur-hq/blur-hq.md) ，當使用高值（此例為50）時。 在約1到2的數值下，差異不明顯。

| 模糊（原子） | 模糊總部 |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="blur.resources/blur-example.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="blur.resources/blur-hq.png"/></div> |
