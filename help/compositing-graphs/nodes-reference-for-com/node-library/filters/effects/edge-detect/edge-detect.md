---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/edge-detect.html"
breadcrumb-title: ''
description: 使用邊緣偵測節點來偵測材質中的邊緣，以建立輪廓和基於邊緣的遮罩效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Edge Detect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 邊緣偵測
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 7%

---


# 邊緣偵測

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/edge-detect.png){width="128px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

偵測黑白影像中的對比，然後建立黑白遮罩以突出對比。

在許多需要邊緣遮罩的情況下非常有用。 請記得它在高對比度輸入時效果最佳;如果需要，先調整對比度再傳送到這個節點。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>邊寬</b> <i>1.0 - 16.0</i> | 偵測到邊緣區域的寬度。 |
| <b>邊緣圓度</b> <i>0.0 - 16.0</i> | 圓潤、模糊並平滑生成的遮罩。 |
| <b>倒轉</b> <i>錯誤/真實</i> | 結果會被反轉。 |
| <b>耐受性</b> <i>0.0 - 1.0</i> | 邊緣應該出現的位置的容差限制因子。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/edge-detect-ex.png" />
        </td>
    </tr>
</table>
