---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/smart-auto-tile.html"
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
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 5%

---


# 智慧自動磁磚

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](smart-auto-tile.resources/smart-auto-tile.png){width="128px"}

<b>收錄於：</b> 《材料濾>掃描處理》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

此節點會根據對輸入的智慧分析，將非平鋪的基色、法線與高度貼圖轉換成平鋪版本。 它類似 [於 Make It Tile Photo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md)，但更進階，因為它利用所有頻道的資訊，以最聰明的方式將內容融合在一起（類似 [Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md) 的做法）。 它也有內建 [的裁切](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) 功能，可以決定鋪磚時該用哪個區域——請務必 [多了解裁切節點](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) 的相關內容，才能正確理解這個功能。

使用這個節點時，先定義你的裁切區域，然後用邊緣設定來決定拼貼邊如何融合到中心。 Treshold 參數對此至關重要！ 請記住，大面積且均勻的區域不太適合這種效果;細節和形狀越多，需要處理的空間就越多。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>面具</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 可以用「使用遮罩」參數切換。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>作物</b> |  |
| <b>輸入大小</b> <i>0 - 8192</i> | 輸入影像的解析度與比例。 對於非方形影像非常重要。 |
| <b>轉換</b> <i>（變換矩陣）</i> | 旋轉並縮放結果。 結果可透過直接與畫布互動來調整。 |
| <b>偏移</b> <i>0.0 - 1.0</i> | 移動或翻譯結果。 結果可透過直接與畫布互動來調整。 |
| <b>Edge</b> |  |
| <b>偵測邊緣</b> <i>錯誤/真實</i> | 開啟或關閉特殊邊緣會偵測到混合。 |
| <b>使用每個通道的閾值</b> <i>錯誤/真實</i> | 在全域限制值或每個通道間切換。 |
| <b>門檻</b> <i>0.0 - 1.0</i> |  |
| <b>閾值底色</b> <i>0.0 - 1.0</i> |  |
| <b>門檻正常</b> <i>0.0 - 1.0</i> |  |
| <b>門檻高度</b> <i>0.0 - 1.0</i> |  |
| <b>切割偏移</b> <i>0.0 - 0.5</i> | 移動切割的主要控制，X軸和Y軸是分開的。 |
| <b>模糊</b> <i>0.0 - 2.0</i> | 模糊了融合的過渡。 |
| <b>平滑度</b> <i>0.0 - 2.0</i> | 控制邊緣分析結果的鋸齒狀。 |
| <b>網格解析</b> <i>1 - 11</i> | 邊緣分析的高品質解析度。 |
| <b>使用底色</b> <i>錯誤/真實</i> | 切換基底色彩處理（進出）。 |
| <b>使用普通難度</b> <i>錯誤/真實</i> | 切換正常處理（進出）。 |
| <b>使用高度</b> <i>錯誤/真實</i> | 切換正常處理（進出）。 |
| <b>使用面具</b> <i>錯誤/真實</i> | 切換 Mask 貼圖的使用，以切換自訂印章遮罩形狀。 |
