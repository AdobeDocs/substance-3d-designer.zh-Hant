---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-uv.html"
breadcrumb-title: ''
description: 使用 Diffusion UV 節點在 UV 空間中套用擴散效果，創造平滑的色彩過渡和混合效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion UV
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 擴散紫外線
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 1%

---


# 擴散紫外線

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-icon.png){width="200px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據提供的&#x200B;**遮罩**&#x200B;影像輸入，對來源&#x200B;**影像輸入的** UV 座標進行擴散處理，並在來源&#x200B;**值間**&#x200B;插值座標。

只有與遮罩相符的像素所產生的 UV 會被擴散;其他像素不參與結果。

請注意，平鋪的處理方式特殊：當平鋪啟用&#x200B;**（預設情況下）時，可以在 0/1 限制下平均鄰近座標。

例如，若一個像素的 U 座標值為 0.1，另一個像素為 0.8，則平均值將為 0.95 而非 0.45，因為 *假設座標*&#x200B;是鋪磚。 這與實際像素位置無關：座標值在整個影像中以相同方式處理。

這可能導致使用此濾波器進行 *紋理變形*&#x200B;時不良的結果。 如果發生這種情況，請確保你的遮罩定義的「控制曲線/點」間距不超過 *半個貼圖長度*。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>資料來源</b> <i>顏色</i> | 紫外線可以擴散。 請注意，在此篩選器中，平鋪的處理方式特別（見 <i>說明</i>）。 |
| <b>面具</b> <i>灰階</i> | 擴散遮罩：白色像素在 Source</i> 中<i>取樣，並在黑色像素中擴散。圖片應該是黑白的。 若遮罩包含梯度，截止值為 0.5。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>迭代</b> <i>0.0 - 64.0</i> | 要執行的擴散迭代次數（越多越好，但越慢）。 有用的數值約為[8， 48]範圍。<br>請注意，如果你不追求數學正確性，低數值也沒問題，甚至更好。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/diffusion-uv-01a-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/diffusion-uv-01a-after.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/diffusion-uv-01b-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/diffusion-uv-01b-after.jpg" />
        </td>
    </tr>
</table>
