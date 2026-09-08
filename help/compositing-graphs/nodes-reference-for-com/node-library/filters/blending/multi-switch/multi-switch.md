---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/multi-switch.html"
breadcrumb-title: ''
description: 使用多重切換節點，根據選擇器在多個輸入貼圖間切換，以選擇條件貼圖。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Multi Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多重交換器
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# 多重交換器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/multi-switch-greyscale.png){width="128px"}

![](../../../../../../assets/multi-switch.png){width="128px"}

<b>收錄於：</b> 濾鏡>混合

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

作為開關盒，僅通過由「輸入選擇」參數定義的輸入。 所以如果連接兩個輸入，只有其中一個會被回傳（未修改），視使用者選擇而定。

在圖表中加入多種選項非常有用。 結合[&#128279;](../../../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)曝光（最好是下拉選單），可以有很大的自訂功能。

重要：務必使用適合你輸入的版本！ 用「多開關」來控制色彩輸入，用「多開關灰階」來表示灰階輸入。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入 1-20</b> <i>色彩輸入</i> |  |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>輸入號碼</b> <i>2 - 20</i> | 需要暴露的輸入數量。 重要提示：當編號減少時，不會移除連接！ |
| <b>輸入選擇</b> <i>1 - 20</i> | 要回傳哪個輸入作為結果。 |
