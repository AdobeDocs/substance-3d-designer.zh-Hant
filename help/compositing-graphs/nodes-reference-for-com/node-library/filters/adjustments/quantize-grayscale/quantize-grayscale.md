---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/quantize-grayscale.html"
breadcrumb-title: ''
description: 使用量化灰階節點來減少灰階層數以產生海報化效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Quantize Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 灰階量化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---


# 灰階量化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![量化灰階圖示 量化灰階圖示](../../../../../../assets/quantize-grayscale.png ""){width="200px"}

<b>收錄於：</b> 篩選>調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

產生一個圓形的單樣條曲線。

</td>
</tr>
</table>

## 參數

<b>步驟</b> *整數*：輸入範圍應近似為多個獨立值。

<b>偏移</b> *浮點*&#x200B;對輸入範圍施加偏移，導致 *結果在該範圍內移動* 。

<b>坡度</b> *浮動*&#x200B;對近似值之間的轉換&#x200B;*（最多可達*&#x200B;整個階&#x200B;*跨度）套用斜率梯度*。

<b>斜坡曲線</b> *整數*&#x200B;設定由斜率</b>參數所設定<b>的斜率曲線取得的方法：
* *線性*：採用線性曲線，形成直坡
* *平滑步*&#x200B;進：套用平滑步進曲線，產生平滑的斜率
* *曲線輸入*：套用由 <b>曲線輸入</b> 映射所描述的曲線。 你可以用[](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)曲線節點來描述這條曲線，並且有很大的控制力。

## 範例

![範例1](../../../../../../assets/quantizegrayscale.gif "範例1")

![範例2](../../../../../../assets/quantizegrayscale.png "範例2")
