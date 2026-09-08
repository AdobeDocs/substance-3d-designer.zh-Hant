---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/polygon-1.html"
breadcrumb-title: ''
description: 使用 Polygon 1 節點來產生基本的多邊形圖案，並可自訂邊界和幾何材質屬性。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Polygon 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多邊形 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 7%

---


# 多邊形 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/polygon-1-1.png){width="128px"}

<b>收錄於：</b> 紋理產生器>圖案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

產生多邊形形狀，並提供多種調整選項。 請參見 [Polygon 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/polygon-2/polygon-2.md) 以獲得更簡單的版本。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>側線</b> <i>3 - 32</i> | 設定多邊形應該有的邊數。 |
| <b>爆炸</b> <i>0.0 - 1.0</i> | 將多邊形「切片」移動。 |
| <b>三角形尺寸</b> <i>0.0 - 1.0</i> | 調整切片/三角形的大小。 任何調整都可能讓形狀破裂，只有1,1。 完美連接！ |
| <b>規模</b> <i>0.0 - 1.0</i> | 整個形狀會合而為一。 |
| <b>自動秤</b> <i>錯誤/真實</i> | 調整縮放，讓整個多邊形都能進入視圖，並設定預設參數。 |
| <b>旋轉</b> <i>0.0 - 1.0</i> | 可以旋轉整個形狀。 |
| <b>梯度</b> <i>錯誤/真實</i> | 它會產生漸層切片/三角形，而不是實體切片。 注意：啟用此設定後會類似 Polygon 2。 |
| <b>梯度反轉</b> <i>錯誤/真實</i> | 如果啟用「漸層」，則會將漸變方向反轉。 |
| <b>鋪磚</b> <i>1 - 16</i> | 設定結果應該鋪磚的次數。 |
| <b>非平方展開</b> <i>錯誤/真實</i> | 能以非平方比率補償擠壓與拉伸。 |
| <b>非方形鋪磚</b> <i>錯誤/真實</i> | 啟用非正方形擴展時，會將形狀平鋪而不會被壓扁。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/polygon-1-ex.gif" />
        </td>
    </tr>
</table>
