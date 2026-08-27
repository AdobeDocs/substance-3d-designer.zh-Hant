---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-photo.html"
breadcrumb-title: ''
description: 使用「製作圖塊照片」節點，將照片轉換成無縫的平鋪貼圖，方便製作材質。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Photo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 拼圖照片
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 9%

---


# 拼圖照片

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](make-it-tile-photo.resources/make-it-tile-photo.png)

![](make-it-tile-photo.resources/make-it-tile-photo-grayscale.png)

<b>收錄於：</b> 濾波器>平鋪

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

此節點提供邊緣修正功能，適用於因邊緣不連續而無法平鋪的影像。 它只影響輸入影像的邊緣。 如果你想用不同方式調整比例或拼貼，可以看看 [Make It Tile Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-patch/make-it-tile-patch.md)。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>遮罩扭曲H</b> <i>-100.0 - 100.0</i> | 引入水平軸的變形，以避免不明確的過渡。 |
| <b>面具扭曲V</b> <i>-100.0 - 100.0</i> | 引入垂直軸的變形，以避免未定義的轉換。 |
| <b>面具尺寸 H</b> <i>0.0 - 1.0</i> | 設定過渡邊緣水平延伸的距離。 |
| <b>面具尺寸 V</b> <i>0.0 - 1.0</i> | 設定過渡邊緣垂直延伸的距離。 |
| <b>遮罩精度 H</b> <i>0.0 - 1.0</i> | 這樣可以設定橫向過渡的平滑程度。 |
| <b>遮罩精密 V</b> <i>0.0 - 1.0</i> | 設定垂直過渡的平滑程度。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="make-it-tile-photo.resources/mit-photo-ex.png" />
        </td>
    </tr>
</table>
