---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-hbao-filter-node.html"
breadcrumb-title: ''
description: 使用環境遮蔽 HBAO 濾鏡節點，利用基於地平線的演算法生成環境遮蔽貼圖，呈現逼真的陰影效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (HBAO) (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 環境遮蔽（HBAO）（濾波節點）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%

---


# 環境遮蔽（HBAO）（濾波節點）

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hbao.png){width="128px"}

## 環境遮蔽（HBAO）

**收錄於：***濾鏡/效果*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

輸入高度圖，並產生環境遮蔽圖。 它使用基於地平線的環境遮蔽演算法，該演算法最初用於螢幕空間即時 AO 生成。 對於從程序式高度圖製作程序式AO地圖非常有用。

關於另一種更進階但較慢的 AO 版本，請參見 [環境遮蔽（RTAO）](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)

## 參數

* **使用世界單位**： *虛假/真*&#x200B;切換：使用世界或場景空間單位。 能提供額外參數，讓控制更精確。
* **高度深度**： *0.0 - 1.0*&#x200B;僅在世界單位設定為 False 時使用。 控制全域縮放。
* **表面大小**： **0.0 - 1000.0**&#x200B;僅在世界單位設為 True 時使用。 控制全域縮放。
* **身高比例（公分）：***0.0 - 1000.0*&#x200B;僅在世界單位設定為 True 時使用。控制全域縮放。
* **半徑**： *0.0 - 1.0*&#x200B;控制區域的擴散。
* **品質**： *4 個樣本、8 個樣本、16 個樣本*\
  透過計算所用樣本數量來設定品質等級。
* **GPU 優化**： *錯誤/真*&#x200B;啟用內部 GPU 優化，加快處理速度。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/image2021-6-18-11-11-11-1.png" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/image2021-6-18-11-11-22.png" width="300px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
