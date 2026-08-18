---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render-mapping.html"
breadcrumb-title: ''
description: 使用 PBR 渲染映射節點將材質輸出轉換成不同的 PBR 渲染映射格式。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Render Mapping
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR 渲染映射
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# PBR 渲染映射

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-render-mapping-color.png)![](../../../../../../assets/pbr-render-mapping-grayscale.png)

## PBR 渲染映射（彩色/灰階）

**收錄於：***材料過濾器/PBR工具*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

這是 PBR 渲染節點](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)的擴充節點[，允許你將之前 [PBR 渲染](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)的形狀上獨立貼圖。它的主要目標是讓你能從 PBR 渲染](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)中重新映射每個獨立通道[，回到形狀上，從而建立合成的地圖與通道拆解，如下面的範例所示。你可以自由地用 PBR Render Mapping 節點作為元件來建立自己的合成方法和遮罩。

彩色與灰階版本分別適用於兩種資料：漫射地圖使用彩色，粗糙度及金屬及其他灰階地圖使用灰階。

### 輸入

* **材質**： *色彩/灰階輸入*\
  貼圖要映射到形狀上。
* **UV：***色彩輸入* PBR 渲染節點的強制 UV 資料輸入[。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)

## 參數

* **背景色**：*（色彩值）*設定一個純色值作為背景。

## 範例圖片

範例是一個由四個不同 PBR 渲染映射節點組成的合成，使用[線性梯度](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-linear-1/gradient-linear-1.md)上的[直方圖選擇](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-select/histogram-select.md)作為遮罩。

![](../../../../../../assets/pbr-render-mapping-ex.png){width="256px"}

![](../../../../../../assets/pbr-render-mapping-ex-2.png){width="256px"}

</td>
</tr>
</table>
