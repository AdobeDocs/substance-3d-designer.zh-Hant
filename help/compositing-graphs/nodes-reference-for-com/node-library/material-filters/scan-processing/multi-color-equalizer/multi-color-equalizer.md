---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-color-equalizer.html"
breadcrumb-title: ''
description: 使用多色均衡器節點（Multi Color Equalizer）節點，將多個紋理通道的顏色均衡，以實現掃描材質的一致性處理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多色均衡器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---


# 多色均衡器

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer-multi.png){width="128px"}

## 多色均衡器

**收錄於：***材料濾鏡/掃描處理*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

這是多輸入版本 [的色彩均衡器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md)。 它能均勻化色彩差異，並以使用者可選擇的比例去除不需要的色調。 它主要用於多角度照片，然後 [再與多角度轉反照](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) 率或 [多角度轉正常](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)合成。

>[!NOTE]
>
> 更多資訊請參閱原始 [色彩均衡器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md) 。

## 參數

### 輸入

* **輸入 1-8**： *色彩輸入*&#x200B;需處理多個輸入。
* **遮罩輸入**： *灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

### 參數

* **輸入計數**： *1 - 8*&#x200B;設定需平行處理的輸入數量。
* **輸入平鋪：***False/True*，可選擇性地保留邊緣上的平鋪。
* **半徑**： *0.0 - 50.0*&#x200B;設定均衡半徑。 越大半徑只會消除較大的顏色差異。 這需要對每張圖片進行調整。
* **明亮/暗度平衡：*0.0**- 1.0*&#x200B;偏壓設定，用來保留或去除較暗的色調。
* **自訂色彩變化**： *虛假/真實*&#x200B;允許你調整效果，朝向使用者指定的顏色。
* **顏色變化**\
  只有啟用自訂色彩變化時才會啟用。 設定允許你選擇色調偏移來平衡。
  * **色相**： *0.0 - 360.0*
  * **色度**： *0.0 - 1.0*
  * **亮度**： *0.0 - 1.0*
* **遮罩來源**： *無、影像平均值、色彩參數、輸入*&#x200B;設定是否應該進行遮罩。 顏色參數可在下方啟用額外設定，輸入可切換至使用者自訂遮罩輸入。
* **面具**\
  只有在色彩參數遮罩時才會啟用。 包含額外的遮罩參數，可根據影像本身決定遮罩。 以下參數允許你精確地將色調轉換成二元遮罩，並套用均衡效果。 請注意，使用這些設定時，半徑參數的影響可能會變得較不明顯。
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
