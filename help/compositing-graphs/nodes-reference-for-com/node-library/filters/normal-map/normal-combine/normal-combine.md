---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-combine.html"
breadcrumb-title: ''
description: 使用 Normal Combine 節點來合併多個法線貼圖，用於分層表面細節和細節。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Combine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 普通聯合測試
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 3%

---


# 普通聯合測試

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-combine.resources/normal-combine.png){width="128px"}

<b>收錄於：</b> 法線貼圖>濾波器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

法線結合術以數學上正確的方式結合兩個法線映射的細節。

它與其他 2D 影像編輯軟體中知名的「疊加」方法相似，但在內部運作方式略有不同（有三種選項）。

</td>
</tr>
</table>

這是將 2D 生成的法線貼圖細節加入烘焙貼圖的最佳且最正確的方法。

如果你想混合兩個法線貼圖而不合併它們的細節（例如使用遮罩），你應該使用 [法線混合](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-blend/normal-blend.md)。

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>普通2</b> <i>顏色</i> | 說明 |
| <b>普通 1</b> <i>顏色</i> | 說明 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>技巧</b> *整數* | 設定採用哪種內部混合技術，以速度換取品質。<br><br>*- 白色調整（低品質）<br>* 通道混音器（高品質）<br>* 細節導向（高品質）* |

## 範例
