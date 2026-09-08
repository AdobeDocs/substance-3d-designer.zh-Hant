---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-albedo-safe-color.html"
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
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# PBR Albedo安全染料

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/pbr-albedo-safe-color.png){width="128px"}

<b>收錄於：</b> PBR工具>材料過濾器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這是一個工具節點，當基色或擴散值超出可接受的 PBR 正確範圍時，會進行修正。 當設定為金屬色時，節點也會嘗試根據金屬色強度修正基色值。

另外請參考 [PBR BaseColor / Metallic Validate](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic/pbr-basecolor-metallic-validate.md) 的視覺回饋，找出可能錯誤的區域。

這對於快速修正工具非常有用，特別是在學習PBR時，但並非絕對且必須永遠正確的度量。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>PBR 工作流程</b> <i>底色 - 金屬色，漫射 - 鏡面色</i> | 可在兩種不同的 PBR 工作流程間切換。 |
| <b>耐受性</b> <i>0.0 - 1.0</i> | 對於超出範圍的數值的容忍度。 |
