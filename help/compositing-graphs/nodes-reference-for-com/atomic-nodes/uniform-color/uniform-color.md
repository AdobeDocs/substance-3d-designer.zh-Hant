---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/uniform-color.html"
breadcrumb-title: ''
description: 使用 Uniform Color 節點來產生均勻的色彩貼圖，以建立純色填充和底層。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Uniform color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 制服顏色
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# 制服顏色

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子節點：均勻顏色](../../../../assets/comp_uniform_1.png "原子節點：均勻顏色"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

產生平坦的灰階或色彩值。

這是一個簡單的節點，經常用作加入顏色或建立特定值的起點。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> 效能優化
> 
> 這兩種調整都降低了節點的計算時間與記憶體佔用量：
> 
> * 如果需要灰階值，請確保節點的色彩模式](#parameters)切換[為「灰階」。
> * 由於節點輸出是平面色，你可以使用最低解析度。 將節點的「[輸出大小](../../../../compositing-graphs/output-size/output-size.md)」參數設定為使用「絕對」[繼承法](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) ，解析度為 16x16 像素。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 參數

</td>
<td style="border: 0;" valign="top">

### 輸出連接器

</td>
<td style="border: 0;" valign="top">

### 範例

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## 參數

|  |  |
| --- | --- |
| <b>彩色模式</b> *布林值* | 在灰階和彩色輸出影像之間切換。 |
| <b>輸出顏色</b> *浮動/漂浮4* | 選擇用於輸出影像的平面顏色。 使用「Color」色彩模式時，Alpha 通道用於不透明度，0 表示完全透明，1 表示完全不透明。 |

## 輸出連接器

|  |  |
| --- | --- |
| <b>產出</b> *彩色/灰階* |  |

## 範例

*即將推出。*
