---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/color-equalizer.html"
breadcrumb-title: ''
description: 使用色彩均衡器節點來平衡掃描材質的色彩變化，以達到貼圖外觀一致。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 色彩均衡器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 6%

---


# 色彩均衡器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](color-equalizer.resources/color-equalizer-01.png){width="128px"}

<b>收錄於：</b> 《材料濾>掃描處理》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這個節點就像高品質的高通[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)器一樣，用於色彩差異。一般高通器會去除飽和度並可能帶來不必要的銳利感，而色彩均衡器則能平衡色彩差異並以使用者可選擇的尺度去除不想要的色調。

如果照片或掃描中有不想要的色彩差異，或是你想去除的色調，這非常有用。 如果你用 [過 Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)，這個節點應該會讓你感到熟悉。

遮罩選項主要用於去除非常特定的色調，或僅在特定明度範圍內運作。 如果你覺得效果太廣泛，就用這些。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入</b> <i>色彩輸入</i> |  |
| <b>遮罩輸入</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 只有當 Mask 設為「輸入」時才會啟動。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>輸入平鋪</b> <i>錯誤/真實</i> | 可選擇性地保留邊緣的瓷磚。 |
| <b>半徑</b> <i>0.0 - 50.0</i> | 設定均衡半徑。 越大半徑只會消除較大的顏色差異。 這需要對每張圖片進行調整。 |
| <b>明暗平衡</b> <i>0.0 - 1.0</i> | 偏壓設定可以保留或去除較深的色調。 |
| <b>自訂色彩變化</b> <i>錯誤/真實</i> | 允許調整效果，朝向使用者指定的顏色。 |
| <b>顏色變化</b> | 只有啟用自訂色彩變化時才會啟用。 設定允許你選擇色調偏移來平衡。 |
| <b>色相</b> <i>0.0 - 360.0</i> |  |
| <b>色彩</b> <i>0.0 - 1.0</i> |  |
| <b>盧瑪</b> <i>0.0 - 1.0</i> |  |
| <b>面罩來源</b> <i>無、影像平均值、色彩參數、輸入</i> | 如果發生任何遮蔽事件，就要設定。 色彩參數啟用以下額外設定，輸入切換至使用者自訂的遮罩輸入。 |
| <b>面具</b> | 這只有在色彩參數遮罩時才會啟用。 額外的遮罩參數，根據影像本身決定遮罩。 以下參數允許您精確地將色調轉換成二元遮罩，並套用均衡效果。 請注意，使用這些設定時，半徑參數的影響可能會變得較不明顯。 |
| <b>顏色</b> <i>（色彩值）</i> |  |
| <b>休伊山脈</b> <i>0.0 - 360.0</i> |  |
| <b>色度範圍</b> <i>0.0 - 1.0</i> |  |
| <b>盧馬山脈</b> <i>0.0 - 1.0</i> |  |
| <b>模糊</b> <i>0.0 - 2.0</i> |  |
| <b>平滑度</b> <i>0.0 - 2.0</i> |  |
