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
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 7%

---


# 多色均衡器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer-multi.png){width="128px"}

<b>收錄於：</b> 《材料濾>掃描處理》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這是多輸入版本 [的色彩均衡器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md)。 它能均勻化色彩差異，並以使用者可選擇的比例去除不需要的色調。 它主要用於多角度照片，然後 [再與多角度轉反照](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) 率或 [多角度轉正常](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)合成。

>[!NOTE]
>
> 更多資訊請參閱原始 [色彩均衡器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md) 。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入 1-8</b> <i>色彩輸入</i> | 需要處理多個輸入。 |
| <b>遮罩輸入</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>輸入計數</b> <i>1 - 8</i> | 設定需平行處理的輸入數量。 |
| <b>輸入平鋪</b> <i>錯誤/真實</i> | 可選擇性地保留邊緣的瓷磚。 |
| <b>半徑</b> <i>0.0 - 50.0</i> | 設定均衡半徑。 越大半徑只會消除較大的顏色差異。 這需要對每張圖片進行調整。 |
| <b>明暗平衡</b> <i>0.0 - 1.0</i> | 偏壓設定可以保留或去除較深的色調。 |
| <b>自訂色彩變化</b> <i>錯誤/真實</i> | 讓你可以調整效果，朝向使用者指定的顏色。 |
| <b>顏色變化</b> | 只有啟用自訂色彩變化時才會啟用。 設定允許你選擇色調偏移來平衡。 |
| <b>色相</b> <i>0.0 - 360.0</i> |  |
| <b>色彩</b> <i>0.0 - 1.0</i> |  |
| <b>盧瑪</b> <i>0.0 - 1.0</i> |  |
| <b>面罩來源</b> <i>無、影像平均值、色彩參數、輸入</i> | 決定是否應該進行任何遮蔽。 顏色參數可在下方啟用額外設定，輸入可切換至使用者自訂遮罩輸入。 |
| <b>面具</b> | 只有在色彩參數遮罩時才會啟用。 包含額外的遮罩參數，可根據影像本身決定遮罩。 以下參數允許你精確地將色調轉換成二元遮罩，並套用均衡效果。 請注意，使用這些設定時，半徑參數的影響可能會變得較不明顯。 |
| <b>顏色</b> <i>（色彩值）</i> |  |
| <b>休伊山脈</b> <i>0.0 - 360.0</i> |  |
| <b>色度範圍</b> <i>0.0 - 1.0</i> |  |
| <b>盧馬山脈</b> <i>0.0 - 1.0</i> |  |
| <b>模糊</b> <i>0.0 - 2.0</i> |  |
| <b>平滑度</b> <i>0.0 - 2.0</i> |  |
