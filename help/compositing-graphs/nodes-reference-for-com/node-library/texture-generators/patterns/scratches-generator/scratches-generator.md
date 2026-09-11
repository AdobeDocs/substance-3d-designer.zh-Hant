---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/scratches-generator.html"
breadcrumb-title: ''
description: 使用刮痕產生器節點來製作程序性刮痕圖案，以增加材料的磨損和損壞。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Scratches Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 刮痕產生器
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 8%

---


# 刮痕產生器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](scratches-generator.resources/scratches-generator.png)

<b>收錄於：</b> 紋理產生器>圖案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這會隨機產生刮痕，並提供多種自訂選項，例如設定方向、擴散和變形。

有一個特別版本的刮痕產生器，叫做刮痕產生法線，會根據刮痕的深度產生法線貼圖。 大多數選項都一樣，但有幾個額外參數明確標示為普通設定（見下文）。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>樣條數</b> <i>1 - 512</i> | 需要放置的刮痕（花鍵）數量。 |
| <b>每個樣條的最大段數</b> <i>2 - 256</i> | 劃痕長度內的段數/細分數量。 這會讓曲線和變形變得更平滑。 失真值越高，效果越明顯。 |
| <b>花鍵旋轉</b> <i>0.0 - 1.0</i> | 所有樣條線均勻旋轉，使其朝向某個方向。 |
| <b>樣條旋轉隨機</b> <i>0.0 - 1.0</i> | 角度變化，隨機旋轉每個樣條。 |
| <b>樣條尺度</b> <i>0.0 - 1.0</i> | 均勻縮放所有樣條曲線。 |
| <b>樣條尺度隨機</b> <i>0.0 - 1.0</i> | 隨機地逐個逐條縮放。 |
| <b>樣鍵失真</b> <i>0.0 - 1.0</i> | 所有樣條曲線的變形水平均勻。 |
| <b>樣條變形隨機</b> <i>0.0 - 1.0</i> | 會個別隨機化每個樣條線的失真程度。 |
| <b>花鍵失真頻率</b> <i>0.0 - 1.0</i> | 設定失真頻率，控制失真細節的尺度。 |
| <b>花鍵寬度</b> <i>0.0 - 2.0</i> | 統一設定所有樣條線的寬度。 |
| <b>樣條寬度隨機</b> <i>0.0 - 1.0</i> | 會隨機化每個樣條線的寬度。 |
| <b>樣條位置隨機</b> <i>0.0 - 1.0</i> | 會隨機化每個樣條的位置。 這個數值越低，越多樣條線會聚集到畫布中心。 可以用來製造刮痕斑點。 |
| <b>設定 px 中的樣條寬度</b> <i>錯誤/真實</i> | 決定花條寬度設定所使用的單位。 |
| <b>亮度隨機（僅限灰階版本）</b> <i>0.0 - 1.0</i> | 會將每個樣條的亮度逐一隨機化。 |
| <b>普通強度（僅限普通版本）</b> <i>0.0 - 1.0</i> | 設定每個樣條曲線的正常效應強度。 |
| <b>普通強度隨機（僅限普通版本）</b> <i>0.0 - 1.0</i> | 會分別隨機化每個樣鍵的正常強度。 |
| <b>一般格式（僅限一般版本）</b> <i>DirectX、OpenGL</i> | 切換不同的法線貼圖格式（反轉綠色通道）。 |
| <b>淡出模式</b> <i>無，開始，結束，開始 + 結束</i> | 設定樣條是否以及以何方向消失。 |
| <b>淡出長度</b> <i>0.0 - 1.0</i> | 設定淡出效果的長度（如上述啟用）。 |
| <b>非平方展開</b> <i>錯誤/真實</i> | 能以非平方比率補償擠壓與拉伸。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="scratches-generator.resources/scratches-ex1.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="scratches-generator.resources/scratches-ex2.png" />
        </td>
    </tr>
</table>
