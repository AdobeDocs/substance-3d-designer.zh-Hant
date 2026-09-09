---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-grayscale.html"
breadcrumb-title: ''
description: 使用擴散灰階節點來套用灰階擴散效果，以創造平滑的色彩過渡和混合效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 擴散灰階
user-guide-description: ''
user-guide-title: ''
source-git-commit: 07f136ebd89fbe737b6c042f1275bd348b2be514
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 3%

---


# 擴散灰階

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](diffusion-grayscale.resources/diffusion-grayscale-icon.png){width="200px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據提供的&#x200B;**遮罩**&#x200B;影像輸入，對來源&#x200B;**影像輸入的數值**&#x200B;施加擴散處理，創造平滑的數值漸層。

只有與遮罩相符的像素值會被擴散;其他像素不參與結果。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>資料來源</b> <i>灰階</i> | 影像要擴散。 |
| <b>面具</b> <i>灰階</i> | 擴散遮罩：在Source</i>中取<i>樣白色像素，並在黑色像素中擴散。圖片應該是黑白的。 若遮罩包含梯度，截止值為 0.5。 |
| <b>強度</b> <i>灰階</i> | 定義局部擴散過程的強度。 這張地圖應該對 <i>比</i> ，才能有明顯效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>迭代</b> <i>0.0 - 64.0</i> | 要執行的擴散迭代次數（越多越好，但越慢）。 有用的數值約為[8， 48]範圍。<br>請注意，如果你不追求數學正確性，低數值也沒問題，甚至更好。 |
| <b>距離</b> <i>0.0 - 1.0</i> | 調整擴散的最大距離。 |
| <b>啟用抖動</b> <i>正確/錯誤</i> | 控制每次掃描的取樣方式。 抖動允許收斂次數較少，但會引入雜訊。<br>沒有它，每次通過速度會更快，但要達到平滑且不產生帶狀偽影的效果，仍需多次通過。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-01-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-01a-after.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-01b-after.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-02-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-02-after.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-02-render.jpg" />
        </td>
    </tr>
</table>
