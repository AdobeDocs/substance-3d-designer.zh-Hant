---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-patch.html"
breadcrumb-title: ''
description: 使用 Make It Tile Patch 節點，從輸入圖片中修補並建立無縫的平鋪貼圖。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 讓它成為瓦片補丁
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# 讓它成為瓦片補丁

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/make-it-tile-patch.png)

![](../../../../../../assets/make-it-tile-patch-grayscale.png)

## Make It Tile Patch（灰階）

**收錄於：***濾波器/磁磚*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

此節點為基於格網的半隨機磁磚。 它會根據你的設定，將輸入音色蓋印，嘗試將它轉換成平鋪影像，且不會重複太多。

當你有一小塊貼圖，想從中製作較大尺度的平鋪貼圖時非常有用。

請注意，這和 [Make-It-Tile Photo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md) 不同，後者主要是修正邊緣。

若要對整個材質進行此操作，請參見 [Smart Auto Tile](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/smart-auto-tile/smart-auto-tile.md)。

## 參數

* **遮罩尺寸**： *0.0 - 1.0*&#x200B;蓋章時所用圓形遮罩尺寸。
* **遮罩精度**： *0.0 - 1.0*&#x200B;遮罩的衰減/平滑度精度。
* **遮罩變形**： *-100.0 - 100.0*&#x200B;在遮罩邊緣引入變形。 有助於避免音色間平滑且未定義的過渡。
* **圖案尺寸寬度**： *0.0 - 1000.0*&#x200B;不均勻地改變徽章寬度。
* **圖案尺寸高度**： *0.0 - 1000.0*&#x200B;不均勻地改變徽章高度。
* **無障礙**： *0.0 - 1.0*\
  引入平移隨機性，稍微移動區域。
* **尺寸變化**： *0.0 - 100.0*&#x200B;引入遮罩尺寸變化。
* **八度**： *0 - 6*&#x200B;這是決定總音長的主要控制鍵。
* **旋轉**： *-360.0 - 360.0*&#x200B;預旋轉補丁。
* **旋轉變體**： *0.0 - 360.0*&#x200B;新增每個徽章印記的隨機旋轉。
* **背景色**：*（色彩值）*設定沒有補丁出現區域的背景色。
* **色彩變化**：*0.0 - 1.0（僅限彩色版本）*每個版本引入顏色變化。
* **亮度變化** *（僅限灰階版本）*每個音色引入亮度變化。

## 範例圖片

![](../../../../../../assets/patch-ex.gif)

</td>
</tr>
</table>
