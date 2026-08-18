---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan-non-uniform.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---


# 直方圖掃描非均勻

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/histogram-scan-non-uniform.png){width="128px"}

## 直方圖掃描非均勻

**收錄於：***濾鏡/調整*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

直方圖掃描](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)的進階版本[，新增控制與輸入，能以每像素層級驅動效果，而非均勻地覆蓋整幅影像。可用來實現更複雜的對比與遮罩過渡。

它比一般 [直方圖掃描](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)複雜得多，所以在嘗試使用非均勻版本前，務必熟悉它。

## 參數

### 輸入

* **輸入**： *灰階輸入*&#x200B;來源，需修改。
* **位置映射**： *灰階輸入*&#x200B;槽，用來驅動位置參數。 當「使用位置輸入」設為 True（真）時會啟動。 有效明暗範圍很小，取決於對比度地圖和設定。
* **對比度圖**： *灰階輸入*&#x200B;槽用於驅動對比度參數。 當「使用對比度輸入」設為 True（真實）時會啟用。 有效價值範圍很小。

### 參數

* **使用 Position Input**： *False/True*&#x200B;切換 使用 Position Map 輸入槽。
* **位置**： *0.0 - 1.0*&#x200B;控制或修改地圖結果以驅動位置設定。
* **使用對比度輸入**： *假/真*&#x200B;切換，使用對比度圖輸入槽。
* **對比**&#x200B;度： *0.0 - 1.0*&#x200B;控制或修改地圖結果以驅動對比度設定。

## 範例圖片

</td>
</tr>
</table>
