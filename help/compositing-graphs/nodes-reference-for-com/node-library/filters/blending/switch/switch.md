---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/switch.html"
breadcrumb-title: ''
description: 使用 Switch 節點根據遮罩在兩個輸入材質間切換，以選擇條件材質。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 切換
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 1%

---


# 切換

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](switch.resources/switch-01.png){width="128px"}

![](switch.resources/switch-02.png){width="128px"}

<b>收錄於：</b> 濾鏡>混合

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一個簡單的兩位開關節點。 根據開關參數設定，回傳輸入 1 或輸入 2。 結果未經修改。 請參閱 [Multi Switch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md) 以獲得更進階的版本。

它對於在圖中暴露布林（真/假）選項非常有用，因為你只需要一個按鈕，不需要複雜的下拉選單來處理所有選項。

重要：務必使用適合你輸入的版本！ 用「切換」來表示顏色輸入，用「切換灰階」來表示灰階輸入。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入 1（真）</b> <i>彩色或灰階輸入</i> |  |
| <b>輸入 2（錯誤）</b> <i>彩色或灰階輸入</i> |  |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>切換</b> <i>錯誤/真實</i> | 在輸入 1（真）與輸入 2（假）之間切換。 |
