---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-color.html"
breadcrumb-title: ''
description: 使用擴散色彩節點來套用色彩擴散效果，創造平滑的色彩混合與過渡效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 擴散色
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 2%

---


# 擴散色

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](diffusion-color.resources/diffusion-color-icon.png){width="200px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據提供的&#x200B;**遮罩**&#x200B;影像輸入，對來源&#x200B;**影像輸入的顏色施加擴散處理，使用Substance 3D Designer[&#128279;](https://www.adobe.com/products/substance3d-designer.html)時，**&#x200B;能創造平滑的色彩漸層。

只有與遮罩相符的像素顏色會被擴散;其他像素不參與結果。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>資料來源</b> <i>顏色</i> | 影像要擴散。 |
| <b>面具</b> <i>灰階</i> | 擴散遮罩：在Source</i>中取<i>樣白色像素，並在黑色像素中擴散。圖片應該是黑白的。 若遮罩包含梯度，截止值為 0.5。 |
| <b>強度</b> <i>灰階</i> | 定義局部擴散過程的強度。 這張地圖應該對 <i>比</i> ，才能有明顯效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>迭代</b> <i>0.0 - 64.0</i> | 要執行的擴散迭代次數（越多越好，但越慢）。 有用的數值約為[8， 48]範圍。<br>請注意，如果你不追求數學正確性，低數值也沒問題，甚至更好。 |
| <b>距離</b> <i>0.0 - 1.0</i> | 調整擴散的最大距離。 |
| <b>啟用抖動</b> <i>正確/錯誤</i> | 控制每次掃描的取樣方式。 抖動允許收斂次數較少，但會引入雜訊。<br>沒有它，每次通過速度會更快，但要達到平滑且不產生帶狀偽影的效果，仍需多次通過。 |
| <b>是法線貼圖</b> <i>正確/錯誤</i> | 在每個步驟都對數值進行正規化。 |
| <b>用 Alpha 當作面具</b> <i>正確/錯誤</i> | 使用源輸入的 <i>alpha 通道作為擴散遮罩，而非<i>遮罩</i></i>輸入。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-02-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-02a-after.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-02b-after.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-01-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-uv-01b-after-1.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-uv-01a-after-1.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-normal.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-normal-render.jpg" />
        </td>
    </tr>
</table>
