---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/uber-emboss.html"
breadcrumb-title: ''
description: 使用 Uber Emboss 節點來製作進階的壓紋效果，並可自訂深度、角度和光影控制。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Uber Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 超級浮雕
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 9%

---


# 超級浮雕

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](uber-emboss.resources/uber-emboss-01.png){width="128px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

Emboss[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md) 的先進且功能豐富的版本。根據高度圖執行複雜的2D假光照效果。

在某些材質風格需要大量控制時，這點很實用。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>顏色</b> <i>色彩輸入</i> | 要修改的基礎圖片。 |
| <b>高度</b> <i>灰階輸入</i> | 高度圖作為效果的驅動力。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>環境色彩</b> <i>（色彩值）</i> | 陰影區域使用的顏色。 |
| <b>漫遊色彩</b> <i>（色彩值）</i> | 光線區域使用的顏色。 |
| <b>鏡面色彩</b> <i>（色彩值）</i> | 鏡面反射所用的顏色 |
| <b>光強</b> <i>0.0 - 1.0</i> | （假）光的強度。 |
| <b>光線角度</b> <i>0.0 - 1.0</i> | （假）光的入射角 |
| <b>鏡面強度</b> <i>0.0 - 1.0</i> | 鏡面反射的強度。 |
| <b>鏡面光澤</b> <i>0.0 - 1.0</i> | 高光的大小。 |
| <b>漫散粗糙度</b> <i>0.0 - 1.0</i> | 計算漫射光的粗糙度。 |
| <b>陰影不透明度</b> <i>0.0 - 1.0</i> | 融合陰影區域的不透明度。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="uber-emboss.resources/uber-emboss-02.png" />
        </td>
    </tr>
</table>
