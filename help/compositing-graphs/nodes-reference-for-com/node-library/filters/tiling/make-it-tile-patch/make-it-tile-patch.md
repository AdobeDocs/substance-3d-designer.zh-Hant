---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-patch.html"
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
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 8%

---


# 讓它成為瓦片補丁

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](make-it-tile-patch.resources/make-it-tile-patch.png)

![](make-it-tile-patch.resources/make-it-tile-patch-grayscale.png)

<b>收錄於：</b> 濾波器>平鋪

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

此節點為基於格網的半隨機磁磚。 它會根據你的設定，將輸入音色蓋印，嘗試將它轉換成平鋪影像，且不會重複太多。

當你有一小塊貼圖，想從中製作較大尺度的平鋪貼圖時非常有用。

請注意，這和 [Make-It-Tile Photo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md) 不同，後者主要是修正邊緣。

若要對整個材質進行此操作，請參見 [Smart Auto Tile](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/smart-auto-tile/smart-auto-tile.md)。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>面具尺寸</b> <i>0.0 - 1.0</i> | 印章時所用圓形遮罩的尺寸。 |
| <b>遮罩精準度</b> <i>0.0 - 1.0</i> | 遮罩的衰減/平滑度精度。 |
| <b>面罩變形</b> <i>-100.0 - 100.0</i> | 會引入遮罩邊緣的變形現象。 有助於避免音色間平滑且未定義的過渡。 |
| <b>圖案尺寸寬度</b> <i>0.0 - 1000.0</i> | 能不均勻地改變補丁的寬度。 |
| <b>圖案尺寸高度</b> <i>0.0 - 1000.0</i> | 補丁高度變化不均勻。 |
| <b>混亂</b> <i>0.0 - 1.0</i> | 引入平移隨機性，稍微移動區域。 |
| <b>尺寸變化</b> <i>0.0 - 100.0</i> | 引入面罩尺寸變化。 |
| <b>八度</b> <i>0 - 6</i> | 這是決定總尺寸的主要控制項。 |
| <b>旋轉</b> <i>-360.0 - 360.0</i> | 預先旋轉補丁。 |
| <b>旋轉變化</b> <i>0.0 - 360.0</i> | 每個徽章印章都會隨機輪替。 |
| <b>背景色</b> <i>（色彩值）</i> | 設定沒有補丁的區域的背景色。 |
| <b>顏色變化</b> <i>0.0 - 1.0（僅限彩色版本）</i> | 每個補丁引入顏色變化。 |
| <b>亮度變化</b> <i>（僅限灰階版本）</i> | 每個音色都引入亮度變化。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="make-it-tile-patch.resources/patch-ex.gif" />
        </td>
    </tr>
</table>
