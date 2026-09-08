---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-irradiance.html"
breadcrumb-title: ''
description: 使用 RT 輻照度節點從幾何體中即時計算光照度資訊，以實現逼真的光照計算。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Irradiance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: RT 輻射
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 4%

---


# RT 輻射

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-irradiance.png){width="128px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

在由環境圖與發射映射生成的高度圖輸入上產生光線追蹤輻照度。 可以用來「烘焙」光照到圖表中的貼圖中。 用於假全域光暈與發光效果。由於計算時間，此節點不應與 CPU（SSE）引擎搭配使用。 回傳兩張地圖：一張是將輻照度應用於材料輸入的 Irradiance 輸出，另一張僅包含計算出的輻照度值的原始 irradiance map。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>高度</b> <i>灰階輸入</i> | 高度是材料槽唯一需要的輸入。 沒有它，節點將無法良好運作。 |
| <b>發射體</b> <i>色彩輸入</i> | 發射應採用純黑色不發光的格式，其他彩色值則會發光。 Alpha 被忽視了。 需要連接到這個插槽或環境插槽才能看到任何結果。 |
| <b>環境</b> <i>色彩輸入</i> | 利用 HDR 照明環境計算輻射度。 需要連接到此插槽或發射插槽才能看到任何結果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>身高比例</b> <i>0.0 - 1.0</i> | 用比例來解釋高度。 影響整個場景的視覺效果。 |
| <b>品質</b> <i>32 射線，64 射線，128 射線</i> | 決定結果品質，也會影響效能。 光線越少，噪音越多。 |
| <b>計算彈跳</b> <i>錯誤/真實</i> | 切換彈跳計算。 會影響品質和速度。 |
| <b>環境旋轉</b> <i>0.0 - 1.0</i> | 讓環境旋轉。 |
| <b>環境暴露（EV）</b> <i>-4.0 - 4.0</i> | 曝光值對環境的使用影響效果的總亮度。 |
| <b>發射強度</b> <i>0.0 - 20.0</i> | 發射輸入的乘數會影響發射輻射的照射強度。 |
| <b>發光色空間</b> <i>sRGB，線性</i> | 色彩空間曾用來解讀 Enissive 輸入。 |
| <b>IBL Shadows 採用 Raw Irradiance Alpha 版本</b> <i>錯誤/真實</i> | 切換是否要加入陰影到 |
| <b>發射LOD偏壓</b> <i>-1.0 - 1.0</i> | 調校 發射光的品質。 值越低，噪音越多。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/rt-irr-03-1.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/rt-irr-01-1.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/rt-irr-02-1.jpg" />
        </td>
    </tr>
</table>
