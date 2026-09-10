---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/basecolor-metallic-roughness-converter.html"
breadcrumb-title: ''
description: 使用 BaseColor Metallic Roughness Converter 節點來轉換不同的 PBR 材質格式與工作流程。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > BaseColor  Metallic  Roughness converter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: BaseColor 金屬粗糙轉換器
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 1%

---


# BaseColor / 金屬 / 粗糙度轉換器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](basecolor-metallic-roughness-converter.resources/pbr-convert.png){width="128px"}

<b>收錄於：</b> PBR工具>材料過濾器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

此節點將基色、金屬與粗糙度映射轉換為不同的 PBR 模型輸出，例如鏡面/光澤模型。 部分輸出目標是知名的渲染引擎，如 Vray、Corona、Redshift、Renderman 和 Arnold。

如果你的圖表或材質是用一種 PBR 模型製作，而你的目標需要不同模型，這很有用。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>使用 SpecularLevel 輸入</b> <i>錯誤/真實</i> | 會讓 SpecularLevel 輸入多一個輸入槽。 這點在皈依時也會被考慮。 |
| <b>目標</b> <i>PBR 漫反射/鏡面/光澤、Vray（GGX）、Corona、Corona 1.6+、Redshift 1.x、Arnold 4（AiStandard）、Arnold 4（AlSurface）、RenderMan（PxrSurface）</i> | 設定轉換目標模型。 |
