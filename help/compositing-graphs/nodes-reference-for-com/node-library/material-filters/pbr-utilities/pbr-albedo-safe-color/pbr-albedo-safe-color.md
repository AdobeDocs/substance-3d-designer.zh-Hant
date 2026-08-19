---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-albedo-safe-color.html"
breadcrumb-title: ''
description: 使用PBR反照率安全色節點，確保反照率顏色在物理上合理的範圍內，適合PBR材料使用。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Albedo Safe Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR Albedo安全染料
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# PBR Albedo安全染料

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-albedo-safe-color.png){width="128px"}

## PBR Albedo安全染料

**收錄於：***材料過濾器/PBR工具*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

這是一個工具節點，當基色或擴散值超出可接受的 PBR 正確範圍時，會進行修正。 當設定為金屬色時，節點也會嘗試根據金屬色強度修正基色值。

另外請參考 [PBR BaseColor / Metallic Validate](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic/pbr-basecolor-metallic-validate.md) 的視覺回饋，找出可能錯誤的區域。

這對於快速修正工具非常有用，特別是在學習PBR時，但並非絕對且必須永遠正確的度量。

## 參數

* **PBR 工作流程**： *基色 - 金屬色、漫射 - 鏡面*&#x200B;切換兩種不同 PBR 工作流程。
* **容差**： *0.0 - 1.0*&#x200B;對於超出範圍的數值的容忍度。

## 範例圖片

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
