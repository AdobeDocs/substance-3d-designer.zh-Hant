---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-simplex-noise.html"
breadcrumb-title: ''
description: 使用 3D 單純形雜訊節點來產生 3D 單純形雜訊圖案，創造平滑且自然的體積紋理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Simplex Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 單純形雜訊
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---


# 3D 單純形雜訊

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-simplex-noise.png){width="128px"}

## 3D 單純形雜訊

**收錄於：***材質產生器**/噪音*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

當烘焙位置圖插入輸入槽時，會產生程序性噪音。 它只設計給 GPU 引擎使用。\
類似 [3D Perlin Noise](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md)，但更快且簡單，適合效能與速度重視的情況。

這種雜訊可以用 Cube 3D GBuffers](https://support.allegorithmic.com/documentation/display/SDDOC/Cube+3D+GBuffers) 作為輸入來測試[，而非實際烘焙的貼圖（如下方範例圖片所示）。

## 參數

* **等級**： *0.0 - 64.0*\
  設定效果的全域尺度。
* **尺寸**： *0.0 - 2.0*&#x200B;分別對 X、Y 和 Z 軸進行非均勻縮放。

## 範例圖片

![](../../../../../../assets/3d-simplex.gif)

</td>
</tr>
</table>
