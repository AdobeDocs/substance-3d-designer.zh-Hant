---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan-non-uniform.html"
breadcrumb-title: ''
description: 使用直方圖掃描非均勻節點進行非均勻直方圖掃描，以進行進階色彩校正。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan Non-Uniform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 直方圖掃描非均勻
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 2%

---


# 直方圖掃描非均勻

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-scan-non-uniform.resources/histogram-scan-non-uniform-01.png){width="128px"}

<b>收錄於：</b> 篩選>調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

直方圖掃描[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)的進階版本，新增控制與輸入，能以每像素層級驅動效果，而非均勻地覆蓋整幅影像。可用來實現更複雜的對比與遮罩過渡。

它比一般 [直方圖掃描](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)複雜得多，所以在嘗試使用非均勻版本前，務必熟悉它。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入</b> <i>灰階輸入</i> | 來源結果需修改。 |
| <b>位置圖</b> <i>灰階輸入</i> | 輸入槽用來驅動位置參數。 當「使用位置輸入」設為 True（真）時會啟動。 有效明暗範圍很小，取決於對比度地圖和設定。 |
| <b>對比圖</b> <i>灰階輸入</i> | 輸入槽用來驅動對比度參數。 當「使用對比度輸入」設為 True（真實）時會啟用。 有效價值範圍很小。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>使用位置輸入</b> <i>錯誤/真實</i> | 切換使用 Position Map 輸入槽。 |
| <b>職位</b> <i>0.0 - 1.0</i> | 控制或修改地圖結果以驅動位置設定。 |
| <b>使用對比度輸入</b> <i>錯誤/真實</i> | 切換使用對比度圖輸入槽。 |
| <b>對比</b> <i>0.0 - 1.0</i> | 控制或修改地圖結果以驅動對比度設定。 |
