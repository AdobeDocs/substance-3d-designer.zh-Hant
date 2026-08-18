---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/smart-auto-tile.html"
breadcrumb-title: ''
description: 使用智慧自動圖塊節點，利用智慧模式偵測，自動從掃描的材料中生成無縫的圖塊。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Smart Auto Tile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 智慧自動磁磚
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---


# 智慧自動磁磚

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/smart-auto-tile.png){width="128px"}

## 智慧自動磁磚

**收錄於：***材料濾鏡/掃描處理*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

此節點會根據對輸入的智慧分析，將非平鋪的基色、法線與高度貼圖轉換成平鋪版本。 它類似 [於 Make It Tile Photo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md)，但更進階，因為它利用所有頻道的資訊，以最聰明的方式將內容融合在一起（類似 [Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md) 的做法）。 它也有內建 [的裁切](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) 功能，可以決定鋪磚時該用哪個區域——請務必 [多了解裁切節點](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) 的相關內容，才能正確理解這個功能。

使用這個節點時，先定義你的裁切區域，然後用邊緣設定來決定拼貼邊如何融合到中心。 Treshold 參數對此至關重要！ 請記住，大面積且均勻的區域不太適合這種效果;細節和形狀越多，需要處理的空間就越多。

## 參數

### 輸入

* **遮罩**： *灰階輸入*\
  遮罩槽用於遮蔽節點的效果。 可以用「使用遮罩」參數切換。

### 參數

* **作物**
  * **輸入大小**： *0 - 8192*&#x200B;輸入影像的解析度與比例。 對於非方形影像非常重要。
  * **轉換**： *（轉換矩陣）*\
    旋轉並縮放結果。 結果可透過直接與畫布互動來調整。
  * **偏移**&#x200B;量： *0.0 - 1.0*\
    移動或翻譯結果。 結果可透過直接與畫布互動來調整。
* **Edge**
  * **偵測邊緣**： *假/真*&#x200B;切換開啟或關閉特殊邊緣混合。
  * **使用每個通道**&#x200B;的閾值： *假/真*：在全域限制值或每個通道都切換閾值之間。
  * **門檻**： *0.0 - 1.0*
  * **閾值底色**： *0.0 - 1.0*
  * **閾值正常**： *0.0 - 1.0*
  * **門檻高度**： *0.0 - 1.0*
  * **切割偏移**： *0.0 - 0.5*&#x200B;主要控制移動切割，X 軸與 Y 軸皆分開。
  * **模糊**： *0.0 - 2.0*&#x200B;模糊融合過渡。
  * **平滑度**： *0.0 - 2.0*&#x200B;控制邊緣分析結果的鋸齒狀。
  * **網格解析度**： *1 - 11*&#x200B;邊緣分析的高品質解析度。
  * **使用基底色**： *假/真*&#x200B;切換底色處理（進出）。
  * **使用正常**： *假/真*&#x200B;切換正常處理（進出）。
  * **使用高度**： *假/真*&#x200B;切換正常處理（進出）。
  * **使用面具**： *虛假/真實*\
    切換 Mask 貼圖的使用，以切換自訂印章遮罩形狀。

## 範例圖片

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
