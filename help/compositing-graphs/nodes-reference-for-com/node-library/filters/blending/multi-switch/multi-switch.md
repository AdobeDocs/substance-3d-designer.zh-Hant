---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/multi-switch.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 1%

---


# 多重交換器

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-switch-greyscale.png){width="128px"}

![](../../../../../../assets/multi-switch.png){width="128px"}

## 多重開關（灰階）

**收錄於：***濾鏡/混合*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

作為開關盒，僅通過由「輸入選擇」參數定義的輸入。 所以如果連接兩個輸入，只有其中一個會被回傳（未修改），視使用者選擇而定。

在圖表中加入多種選項非常有用。 結合[&#128279;](../../../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)曝光（最好是下拉選單），可以有很大的自訂功能。

重要：務必使用適合你輸入的版本！ 用「多開關」來控制色彩輸入，用「多開關灰階」來表示灰階輸入。

## 參數

### 輸入

* **輸入 1-20**： *色彩輸入*

### 參數

* **輸入編號**： *2 - 20*&#x200B;需要暴露的輸入數量。 重要提示：當編號減少時，不會移除連接！
* **輸入選擇**： *1 - 20*&#x200B;將回傳哪些輸入作為結果。

## 範例圖片

</td>
</tr>
</table>
