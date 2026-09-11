---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/brick-generator.html"
breadcrumb-title: ''
description: 使用 Brick Generator 節點來建立可自訂尺寸、偏移和砂漿屬性的程序化磚塊圖案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Brick Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 磚發電機
user-guide-description: ''
user-guide-title: ''
source-git-commit: 827e738d5db4d64bf366d332a62a7bbd2fa840fc
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 8%

---


# 磚發電機

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](brick-generator.resources/brick-generator.png){width="128px"}

<b>收錄於：</b> 紋理產生器>圖案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

進階磚塊圖案產生器。 有很多專門生成人造磚塊圖案的選項

更多選項請參見 [格子產生器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>磚塊</b> <i>1 - 64</i> | 設定 X 軸和 Y 軸的磚塊數量。 |
| <b>斜面</b> <i>0.0 - 1.0</i> | 改變磚塊的斜角輪廓，允許雙向變換，並設定衰減輪廓和角面圓潤。 |
| <b>保持比例</b> <i>錯誤/真實</i> | 這樣斜角輪廓就和磚塊尺寸綁定了。 |
| <b>差距</b> <i>0.0 - 1.0</i> | 磚塊之間留出一個空隙。 要記得斜角也會帶來縫隙，所以要加上斜角，也必須用這個參數來補償。 |
| <b>中型</b> <i>0.0 - 1.0</i> | 磚塊模式偏移，則每隔一列或一列的大小會改變。 |
| <b>高度</b> <i>-1.0 - 1.0</i> | 修改高度輪廓。 允許引入亮度變化及各種隨機化。 |
| <b>坡度</b> <i>-1.0 - 1.0</i> | 以每塊磚為基礎引入斜率，就像某些磚塊是斜著的。 |
| <b>偏移</b> <i>0.0 - 1.0</i> | 以列為基礎偏移磚塊，會影響每列的間距。 |
| <b>非平方展開</b> <i>錯誤/真實</i> | 能以非平方比率補償擠壓與拉伸。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="brick-generator.resources/brick-generator-ex-01.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="brick-generator.resources/brick-generator-ex-02.gif" />
        </td>
    </tr>
</table>
