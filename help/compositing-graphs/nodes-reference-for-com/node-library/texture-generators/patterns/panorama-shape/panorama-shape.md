---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/panorama-shape.html"
breadcrumb-title: ''
description: 使用 Panorama Shape 節點來建立映射到全景座標的形狀，以便產生環境貼圖。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Panorama Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 全景形狀
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 6%

---


# 全景形狀

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](panorama-shape.resources/panorama-shape-01.png){width="128px"}

<b>收錄於：</b> 紋理產生器>圖案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這是一個很有幫助的節點，可以產生程序式「Studio」類型的全景地圖。 允許你放置和修改聚光燈圖片，並設定它們的 HDR 屬性。 它可以串連成多種形狀。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>形狀矩陣</b> | 移動或平移結果，可透過直接與畫布互動來修改。 |
| <b>形狀</b> <i>方形、圓盤</i> | 集合 形狀類型。 |
| <b>形狀顏色</b> <i>（色彩值）</i> | 設定形狀顏色。 |
| <b>形狀強度</b> <i>0.0 - 100.0</i> | 設定形狀的 HDR 強度。 |
| <b>形狀軟邊界</b> <i>0.0 - 1.0</i> | 改變形狀的邊緣柔軟度。 |
| <b>熱點強度</b> <i>0.0 - 100.0</i> | 設定該形狀熱點的 HDR 強度。 |
| <b>熱點大小</b> <i>0.0 - 1.0</i> | 改變形狀內熱點的大小。 |
| <b>熱點衰減</b> <i>0.0 - 1.0</i> | 改變熱點的衰減和邊緣混合。 |
| <b>熱點位置</b> <i>0.0 - 1.0</i> | 會移動熱點相對於形狀的方向。 |
| <b>啟用 Backgound</b> <i>錯誤/真實</i> | 使背景能以純色填充。 請注意，這表示你無法再透過混合將它們串連起來。 |
| <b>背景色</b> <i>（色彩值）</i> | 設定為純色背景。 |
| <b>啟用貼圖輸入</b> <i>錯誤/真實</i> | 允許自訂輸入，而非預設的形狀類型。 |
