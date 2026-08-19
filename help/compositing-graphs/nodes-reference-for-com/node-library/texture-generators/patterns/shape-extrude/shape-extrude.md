---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-extrude.html"
breadcrumb-title: ''
description: 使用 Shape Extrude 節點來擠出形狀，並在 Substance 3D Designer 的貼圖中創造類似 3D 的深度效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形狀擠出
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---


# 形狀擠出

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-extrude.png){width="128px"}

## 形狀擠出

**收錄於：***貼圖產生器**/圖案*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

一個進階節點，允許將 2D 二元「形狀」輸入渲染成 3D 旋轉高度圖。 這類似於 3D 套件中的擠出，沿著軸線擠出一個形狀，形成體積。 結合輪廓漸層遮罩，也能製作 Revolution/車床型的身體。 對於製作複雜的高程圖人工形狀非常有用。

## 參數

### 輸入

* **擠出形狀輸入**： *灰階輸入*&#x200B;如果擠出形狀設為自訂，你就插入你自己的（最好是）二元形狀遮罩。
* **剖面漸層**： *灰階輸入\
  若 Profile Type 設為垂直梯度，可用來定義軸向形狀的縮放，適用於旋轉物體。*
* **輪廓遮罩**： *灰階輸入*\
  遮罩槽用於隱藏或顯示沿軸線的擠壓形狀。 可用來打破形狀沿軸的連續性。 僅以二進位解讀：灰階賣權值會四捨五入為 0 或 1。

### 參數

* **擠出高度**： *0.0 -* 1.0\
  從中心向上擠出形狀。
* **擠出深度**： *0.0 - 1.0*&#x200B;從中心以下壓成形的量。
* **擠出形狀**： *立方體、圓柱體、自訂輸入*&#x200B;使用內建形狀或外部輸入自訂形狀。
* **擠出形狀尺寸**： *0.0 - 1.0*&#x200B;僅用於內建立方體與圓柱體，決定基本形狀大小，可縮放為非均勻。
* **等級**： *0.0 - 1.0*\
  設定效果的全域尺度。 內建形狀則是統一的基礎形狀縮放，不影響高度或深度。\
  透過自訂輸入，這會以統一的方式擴展整個最終結果。
* **設定檔類型**： *直線、垂直漸層、遮罩*&#x200B;主控制以判斷效果行為及可選額外輸入映射的使用。\
  直線是標準的擠出行為，垂直漸層允許沿整個軸線自訂縮放值，遮罩則允許依遮罩隱藏沿軸的區域。
* **斜面高度**： *0.0 - 1.0*&#x200B;設定斜角沿擠出軸的長度。
* **斜角強度**： *0.0 - 1.0*&#x200B;設定斜角從原始形狀回縮的程度。
* **斜面曲線**： *-1.0 - 1.0*&#x200B;設定凸或凹面曲線，以呈現斜面效應。 值為 0 表示直線，沒有曲線。
* **鏡面斜角**： *假/真*&#x200B;切換，可同時在形狀的上下施加斜角。
* **降頻多重器**： *0 - 2*&#x200B;內建輕鬆降階控制。 可用來快速加入抗鋸齒;同時也要提升節點解析度。
* **職位**：\
  旋轉的主要控制會產生三維空間。 在 2D 視圖中與 interavtice Gizmo 對應。
* **輸出範圍**：*[0， 1]， [-1， 1]*設定輸出最小值與最大值。 若範圍設為 [-1,1]，負值則以黑色呈現。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shape-extrude-1.png" width="256px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
