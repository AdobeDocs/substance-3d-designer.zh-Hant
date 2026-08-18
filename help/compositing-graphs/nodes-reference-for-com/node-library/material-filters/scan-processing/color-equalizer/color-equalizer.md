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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---


# 色彩均衡器

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer.png){width="128px"}

## 色彩均衡器

**收錄於：***材料濾鏡/掃描處理*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

這個節點就像高品質的高通](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)器[一樣，用於色彩差異。一般高通器會去除飽和度並可能帶來不必要的銳利感，而色彩均衡器則能平衡色彩差異並以使用者可選擇的尺度去除不想要的色調。

如果照片或掃描中有不想要的色彩差異，或是你想去除的色調，這非常有用。 如果你用 [過 Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)，這個節點應該會讓你感到熟悉。

遮罩選項主要用於去除非常特定的色調，或僅在特定明度範圍內運作。 如果你覺得效果太廣泛，就用這些。

## 參數

### 輸入

* **輸入**： *彩色輸入*
* **遮罩輸入**： *灰階輸入*\
  遮罩槽用於遮蔽節點的效果。 只有當 Mask 設為「輸入」時才會啟動。

### 參數

* **輸入平鋪：***False/True*，可選擇性地保留邊緣上的平鋪。
* **半徑**： *0.0 - 50.0*&#x200B;設定均衡半徑。 越大半徑只會消除較大的顏色差異。 這需要對每張圖片進行調整。
* **明亮/暗度平衡：*0.0**- 1.0*&#x200B;偏壓設定，用來保留或去除較暗的色調。
* **自訂色彩變化**： *虛假/真實*&#x200B;允許調整效果，朝向使用者指定的顏色。
* **顏色變化**\
  只有啟用自訂色彩變化時才會啟用。 設定允許你選擇色調偏移來平衡。
  * **色相**： *0.0 - 360.0*
  * **色度**： *0.0 - 1.0*
  * **亮度**： *0.0 - 1.0*
* **遮罩來源**： *無，影像平均值，色彩參數，如果需要遮罩，輸入*&#x200B;設定。 色彩參數啟用以下額外設定，輸入切換至使用者自訂的遮罩輸入。
* **面具**\
  這只有在色彩參數遮罩時才會啟用。 額外的遮罩參數，根據影像本身決定遮罩。 以下參數允許您精確地將色調轉換成二元遮罩，並套用均衡效果。 請注意，使用這些設定時，半徑參數的影響可能會變得較不明顯。
  * **顏色**： *（顏色值）*
  * **色相範圍**： *0.0 - 360.0*
  * **色度範圍**： *0.0 - 1.0*
  * **亮度範圍**： *0.0 - 1.0*
  * **模糊**： *0.0 - 2.0*
  * **平滑度**： *0.0 - 2.0*

## 範例圖片

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
